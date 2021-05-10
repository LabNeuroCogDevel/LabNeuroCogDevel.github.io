# Drawing a mask with AFNI by hand

## Step by step
1. The **Define Data Mode** panel in afni has a **Plugins** drawer with an option for **Draw Dataset**.
2. Within the Draw Dataset modal, use **Copy Dataset** to pick the dataset to use as a refernce (FOV, pixel dims, matrix size)
3. In the image viewer window, use the mouse **middle button click and drag** to draw shapes that will be filled *per slice*
  1. Draw to fill on the first (most top/left/front) slice
  2. Move display to the last (most bottom/right/back) slice and draw to fill again
4. Back in the Draw Dataset modal, select a direction from the **Linear Fillin** dropdown and click the **\*Do the Fill\*** button. 
  * A-P for coronal
6. Repeat for each dimension (sagitial, axial, coronal).

## Notes


### Missing plugin button

If the "plugin" button does not exist, there might be a problem with paths. AFNI complains

> Plugins       = 0 libraries read
> ** Your Unix path must include the AFNI binary directory
> ** OR you must setenv AFNI_PLUGINPATH to that directory!

A fix is explicilty setting `AFNI_PLUGINPATH` to the same directory as the afni binary (for the case of a local/non-system install, e.g. afni is in `~/abin`)
```
AFNI_PLUGINPATH="$(dirname $(which afni))" afni
```

## Screenshots
<img src="https://user-images.githubusercontent.com/680742/117687031-6187f980-b185-11eb-8dee-e7e36e633e9d.png" width=500/>

![drawing on slice](https://user-images.githubusercontent.com/680742/117687066-68167100-b185-11eb-8803-6116966e007e.png)

![filling slice](https://user-images.githubusercontent.com/680742/117687095-71074280-b185-11eb-8398-5230e201fc72.png)
