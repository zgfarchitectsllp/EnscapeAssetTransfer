# EnscapeAssetTransfer

This tool moves Enscape Assets from Rhino to Revit
Authors: Jonah Hawk and Andrew Schiffer, ZGF Architects
Plugins Required: RhinoInsideRevit, Human, Elefront.

Follow these steps :)
1) Download the enscape library for offline use. This can be done from any platform and instructions can be found here: https://enscape3d.com/community/blog/knowledgebase/asset-library-2/
2) Run the UpdateEnscapeAssetCSV.exe file included here. This will parse the entire Enscape library by reading the Json files to create a .csv that includes every asset name, ID, and discription. This .csv is used in the Grasshopper definition. 
3) Install RhinoInside and the related plugins, if necessary. 
4) Open the desired Revit Model, Use RhinoInside to open the desired Rhino model containing the assets you wish to transfer to revit. Ensure that the assets are on a consistant layer in Rhino. Do not start Enscape yet. Disable the Grasshopper solver.
5) Open the EnscapeAssetTransferTool.gh file using grasshopper in RhinoInside, WITH THE SOLVER LOCKED.
6) Set the layer name input in GH to the correct layer with your assets in Rhino. 
7) Download the Enscape-Asset-Template.rft included here and set the file path component in GH to its location. This is an empty enscape asset revit family with the correct parameters. 
8) Enable the GH solver to run the script. This may take several minutes, depending on how many assets you are transfereing.  
9) The transfered assets will appear as simple boxes in revit. We are still working on displaying the proxy geometry correctly. 
10) Lock the GH solver, or close out of all GH & Rhino files, then start enscape and enjoy your transfered assets.  

Warning: Running Rhino.Inside and Enscape at the same time will make Revit VERY unstable and prone to crashing. Save all your work before you do this. Try to run the script, then start enscape. 
