
MQP_Documents
[Project Name] User Guide
Fusion 360 CAM - User Guide
Overview
This guide outlines a precise parametric workflow for preparing 3D models for desktop CNC machining within Fusion 360. By utilizing a specialized "Machine Vise" template and defined parameters like Stock_Offset, users can accurately synchronize their digital design with physical stock dimensions and workholding fixtures. The process transitions from assembly constraints to the "Manufacture" workspace, where users apply machine-specific profiles and standard tool libraries to ensure optimal feeds and speeds. Ultimately, this workflow streamlines the path from raw CAD data to a production-ready G-code file tailored for the HL Mill.

User Guide Steps
Step-by-step instructions on how to set up the environment.

G-Code Creation in Fusion CAM
Import your part model or create it in Fusion.

Open the data panel (3x3 square icon in the top left corner) and insert the model named "Machine Vise" into your current design. Right click on the machine vise tab on the left side of your screen and click "Break Link". (you may need to repeat this step twice to use this workflow. The new part will have a new set of parameters that end with "_1". Use these).

Go to [Modify > Change Parameters], and change the values of Stock_X, Stock_Y, and Stock_Z to match the X, Y, and Z dimensions of your stock.

Change the value of Parallel Height to match the height of your machining parallels.

Change the value of Stock_Offset to match the desired distance between the top of the stock and the top plane of your part.

Select "Assembly" in the top row of Fusion. Use the "Constrain Components" tool to mate the translucent green stock box such that it is centered in the vise jaws and sitting on the parallels. Constrain your cad model so it is centered in the stock box. Constrain the top face of your part such that its distance to the top of the stock box uses the parameter "Stock_Offset".

Change your workspace in the top left corner from "Design" to "Manufacture"

Click "New Setup" in the top left corner.
a. A new pop-up window will open and the first choice will be "Machine". Click select and chose the HL Mill profile from the class hub.
b. Click the stock tab (yellow box in top row of the new window). Change the mode to "From Solid". Select the green translucent stock box.
c. Return to the setup tab (white and blue boxes in top row of new window). Find the section named "Model", and select your cad model that you would like to machine.
d. Find the section named "Fixture", and select both vise jaws using ctrl+click.
e. Open the Part "Position" Tab (white 4-pointed arrow in top row of new window), and use the arrows to move the vice to where it will be fastened to the machine.

Once you are finished, click ok.

At this point, your machine is set up and you will begin defining your machining operations to cut your part. Common operations include clearing, pocketing, facing, boring, and chamfering. For any operation you will need to select the part geometry that you would like the operation to create, For a facing operation, this might be a flat surface, or for a chamfer operatio, it might be an edge. You will also need to select a tool from the "HL CNC Standard Tools" Library and select the material you are using to automatically program your feeds and speeds.

Once your toolpaths have been completed, use the "NC Program" feature to generate and download a G-Code file for your part.

Select a repo
Table of Contents

