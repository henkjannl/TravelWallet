# How the assembly instructions were created

I thought it would be a cool idea to make IKEA style assembly instructions. Creating the assembly instructions actually took more time than building the 3D model.

I documented the workflow since this can be useful for more serious purposes.

All files used to compile the manual are in a separate directory named `manual`. The assembly instructions are in one Inkscape file named `_User Manual.svg`. All images are vector based which translates well to pdf. The pdf file `User Manual.pdf` was created by simply saving this Inkscape file as pdf.

<p align="center">
  <img src="themakingof.png" alt="overview" width="600">
</p>

## A. The images of the wallet
The workflow for each little 3D image of the model started in FreeCAD:
* For each image of the wallet, a dedicated FreeCAD assembly of the depicted situation was created (8 in total). These assemblies were created using the `A2plus` workbench. Each assembly is saved as `/manual/UserManualImageX.FCStd`
* After creating the assembly, all parts were grouped together using the `Compound` command in the `Part` workbench
* While watching the 3D model from the top, the `Compound` was rotated by right-clicking `Transform` in the model tree.  
* Then, a blank A4 page was created by using `Insert Page using Template` in the `TechDraw` workbench
* A view of the model was inserted by selecting the `Compound` in the model tree and clicking `Insert View` from the toolbar
* The `Smooth Visible` property of the view was switched off
* Then, the drawing was exported to SVG Export using `Page as SVG` (can be found under `/manual/UserManualImageX.svg`)

The workflow continues in Inkscape:
* Each vector image was imported in the main `_User Manual.svg` file
* The vector image was initially imported outside the margin of the main image
* The image was completely ungrouped by using `Object > Ungroup` (or `ctrl-shift-G`) three times
* Superfluous lines were removed manually.
* The result was again grouped using `Object > Group` (or `ctrl-G`)
* The default linestyle was applied to the group using `Copy` (`ctrl-C`) on an existing group, and `Paste Style` (`ctrl-shift-V`) on the new group
* The new image was then dragged to the final location and scaled down. Ensure all scaling options <img src="scale_options.png" alt="options" height="20"> (right hand side of the toolbar) are switched off to prevent scaling of the the line thickness while adjusting the size of the image. The little lock <img src="little_lock.png" alt="options" height="20"> needs to be activated to ensure proportional scaling.

## B. The IKEA key
I googled an image of an IKEA allen key and manually traced it in Inkscape to create a simple vector image.

## C. The hammer
* The "Ikea Billy assembly instructions" were downloaded as pdf file
* The file was opened in Inkscape using `File > Open` and selecting page 10
* The hammer was copied to the main Inkscape file

## D. The 'call IKEA' icon
* The "Ikea Billy assembly instructions" were downloaded as pdf file
* The file was opened in Inkscape using `File > Open` and selecting page 5
* The call IKEA icon was copied to the main Inkscape file

## E. The rubber bands
The rubber bands can be drawn as follows:

1. Draw a closed spline with stroke width of 0.75 mm
1. Choose `Path > Stroke to path`. Change stoke width to 0.15 mm
1. Draw the missing lines using the same linestyle. Group all items together using `Object > Group` (`ctrl-G`)

<p align="left">
  <img src="rubberband.png" alt="step 3" width="600">
</p>  

## F. The folded paper
The folded paper was simply drawn in Inkscape.

## G. The two euro coins
The two euro coin was downloaded as STEP file and imported into the model.

## H. The five euro bills
The five euro bill was downloaded as bitmap and converted to a vector image using the Inkscape command `Path > Trace bitmap...`

## I. The little plastic bag
The plastic bag was also drawn in Inkscape.
