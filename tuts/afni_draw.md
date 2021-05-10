# Drawing a mask with AFNI
1. The **Define Data Mode** panel in afni has a **Plugins** drawer with an option for **Draw Dataset**.
2. Within the Draw Dataset modal, use **Copy Dataset** to pick the dataset to use as a refernce (FOV, pixel dims, matrix size)
3. In the image viewer window, use the mouse **middle button click and drag** to draw shapes that will be filled *per slice*
  1. Draw to fill on the first (most top/left/front) slice
  2. Move display to the last (most bottom/right/back) slice and draw to fill again
4. Back in the Draw Dataset modal, select a direction from the **Linear Fillin** dropdown and click the **\*Do the Fill\*** button. 
  * A-P for coronal
6. Repeat for each dimension (sagitial, axial, coronal).

## Screenshots
<img src="https://user-images.githubusercontent.com/680742/117687031-6187f980-b185-11eb-8dee-e7e36e633e9d.png" width=500/>

![drawing on slice](https://user-images.githubusercontent.com/680742/117687066-68167100-b185-11eb-8803-6116966e007e.png)

![filling slice](https://user-images.githubusercontent.com/680742/117687095-71074280-b185-11eb-8398-5230e201fc72.png)
