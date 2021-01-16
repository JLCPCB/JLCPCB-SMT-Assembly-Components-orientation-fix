# SMT-Assembly-Components-orientation-fix
This guide has the basic requirments to place a SMT Assembly order with some tips on how to fix the misplacement and orientation of SMD parts.

If you are reading this article description then you are searching for a method to fix the SMT assembly online viewer of JLCPCB, following the steps of this article you will be capable to fix some mismatch generated data and you get a clear view on how it will look like your board after the assembly.

Notes :

* If you are not willing to fix the components placement and orientation by yourself then there is no problem on this because the engineers at JLCPCB will handle your generated files and sort out the uploaded data to make sure that everything will be well produced.
* In case our engineers encountered a problem with the files that your have prepared, then you will immediately receive a notification Email from the JLCPCB support team.

# Starting with the necessary Steps
If you already know how to place an SMT assembly order then move to the next section, if you don’t like to read long descriptions about how to proparly place an SMT order then maybe a video is good for you. [Click here to watch it](https://www.youtube.com/watch?v=jS4zB5Xmdrw&feature=emb_title&ab_channel=JLCPCB)
Across this example we will use a basic circuit that has one chip, one capacitor and some resistors as SMD parts and some screw terminals as Through-Hole parts.
Please note that JLCPCB can assemble only Surface Mounted Devices available at JLCPCB Parts Library that you could check through this [link](https://jlcpcb.com/parts).

In order to have a PCB manufactured all what it takes is the production files [GERBER files](https://en.wikipedia.org/wiki/Gerber_format) these files are generated from your design tool and it should match the requirments of JLCPCB production process so we suggest to check this [link](https://support.jlcpcb.com/article/22-how-to-generate-the-gerber-files) to learn how to properly generate the appropriate files depending on the design tool that you are using.
Kindly check this [link](https://support.jlcpcb.com/article/21-how-do-i-place-an-order) as well to learn how to place a PCB manufacturing order in the proper way.
Moving to the SMT Assembly order, after uploading the GERBER files to JLCPCB ordering webpage you will have the below view.
<p align="center">
  <img src="rootImages/NE555 JLCPCB SMT Assembly.png" width="100%"></p>
In addtion to the GERBER Files the customer needs to activate the SMT Assembly option as it shows the below image in step one.
Once the SMT Assembly is activated the customer needs to set the Assembly side as it is in step two  (top or bottom sides) and it has to be only one side because JLCPCB doesn’t currently accept assembly for both sides of the board.
<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB steps.png" width="100%"></p>
The final step is to confirm the settings to move to the next Webpage that will take you to finalize the SMT assembly data handling as it shows the below image.
<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB files.png" width="100%"></p>
  
  Now it comes the necessary files for the SMT Order, in addition to the **GERBER files** that we have provided in the previous Webpage we need to prepare the **BOM file** and the **CPL file** (aka Pick and Place file or P&P file), these two files are also generated from your PCB design tool and it should be under the following possible extension formats (XLS,XLSX,CSV).
  
  
* BOM file (Bill Of Materials) is the container that has all the necessary information related to the used components and it must contain some specific data for each component, check this [link](https://support.jlcpcb.com/article/80-bill-of-materialsbom-file-for-smt-assembly) to learn what are the defined necessary information for a BOM file.
* Using the CPL file JLCPCB automatically superimpose the components listed in the BOM to the PCB, allowing the verify the component placement on the PCB, it is all obvious that the CPL file has the X and Y position for each component and its orientation as well, check this [link](https://support.jlcpcb.com/article/79-pick-place-file-for-smt-assembly) to learn what are the defined necessary information for a CPL file.

After uploading the files as it shows step one in the below image you need to cilck on « NEXT » as it shows step two to move to the next Webpage.
<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB files1.png" width="100%"></p>
Only one more step before finalizing the order is the parts confirmation, since we have uploaded a BOM file that has multiple components then we need to confirm which parts has to be assembled.
The missed parts in the SMT Parts Library will not be supported and the Through-Hole parts as well.
Our system will automatically detects the available parts and the customer needs to confirm which parts to assemble as it shows step one.
<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB parts confirmation.png" width="100%"></p>  
Once all the needed parts has been confirmed then click next to get quoted for your order.

# Parts orientation and position fix
The final step of the process has a Assembly viewer that combines all the uploaded files, the GERBER files will show up the PCB, the BOM file will tell which parts to set for assembly and the CPL file will show up the selected parts on the board as an estimated View of the final produced board.
In some case you will notice that some parts are missing them right orientation on the baord which is the case for the chip U1 of the example and some parts has missed their right position which is the case for resistor R2 as it shows the below image.
<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB orientation and position.png" width="100%"></p> 

In order to fix this, you need to run the CPL file (Pick and Place file) and move to the parts that showed some wrong view, you will find them by them labels (Designator), in our case we are having the chip U1 and the resistor R2 to fix as it shows the below image.

<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB orientation and position1.png" width="100%"></p> 
  
 For U1 it showed a wrong orientation by 90 degrees so we need to rotate the part by changing the orientation from 90 degrees to 0 degrees and for the Resistor R2 it appears that it was slightly moved on the X axis so we need to center it similar to R1 from the Mid X column by changing it from 32mm to 28.96mm.
 
 <p align="center">
  <img src="rootImages/SMT Assembly JLCPCB orientation and position2.png" width="100%"></p>
  
  Then save the file and get back to where we have stopped in our ordering final step, click on « Go back » until you reach the file uploading webpage and re-uplaod the new CPL file that has the new setup. 
Click on next until you reach the final ordering step where you can verify the SMT Assembly view.
As it shows the below image, everything seems to be fine now and all components are in the right orientation and position.

<p align="center">
  <img src="rootImages/SMT Assembly JLCPCB orientation and position3.png" width="100%"></p>
  
<p align="center">
  <img src="rootImages/SMT Assembly results.png" width="100%"></p>
  
**For further guidance you can send an Email to [support@jlcpcb.com](https://support.jlcpcb.com/article/45-contact-jlcpcb?_ga=2.89705115.1061450305.1610705485-1865388022.1590056196) and you will have a quick reply to your technical questions.**

