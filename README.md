# 4-Color-Spot-Counter
Nikon Elements code to count valency of nanoparticles up to 4 channels

Written to analyze data for Yang et al. 2024. Mosaic quadrivalent influenza vaccine single nanoparticle characterization.

Based on code written by Sara Parker of Nikon Instruments.

###   ************* NOTES FOR USE / README ******************

First, ensure your images have all been properly denoised. I recommend the Elements
Advanced Denoising with a power of 10/20/20/20 for B/G/Y/R.
Also, ensure that your images are in the order B-G-Y-R.
Next, put all the images you want analyzed into a separate folder.
Make one subfolder in this folder and label it "Processed."
Next, open Elements. Go to Edit / Options, Data Export in left menu, Data Export in tab
(not Global Settings).
In the Dropdown menu, choose "Automated Measurement Results."
Next, highlight "Field Meas."
Check the following boxes:  Source, BinaryID, NumberObjects, NumberObjectsRestrict...
Push "OK."
Close any open Excel documents and the Excel program; the macro will open a new document
for you.
Now you are ready to run the macro.

In Elements, go to Macro / Run on Files in Folder.
In the first dropdown menu, choose this 4 channels macro.
In the second dropdown menu, choose the folder with the images to be analyzed.
Under "Saving Documents," choose "Save Into Different Folder" and choose the "Processed"
folder that you created earlier.
Under "Closing Documents," choose "Close all documents after each step."
Now push "Run." The macro will run calculations on each image in the folder
that you specified, and save the analyzed images in the "Processed" folder.

The results for each individual image will be appended to an Excel file. You will need to
consolidate the results using whatever data analysis tool you are most
comfortable with.  Make sure you are using the "NumberObjectsRestrict" column
for the final analysis (see below paragraph for explanation).

Note that the way the macro is coded means that all multivalent particles will be counted
regardless of intensity; however, *** all monovalent particles will be restricted based on a
threshold value *** chosen in the last coding section.  The restricted counts can be found 
in the NumberObjectsRestrict column.  The NumberObjects column has the unrestricted counts
if you need to compare. If you want to change the threshold level, go to the last section
of the code and read the instructions there.
