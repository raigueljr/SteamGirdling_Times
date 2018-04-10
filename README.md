# SteamGirdling_Times

### Background
  Fine root turnover is the annual replacement of roots with a diameter of 2 mm or less. This process is a vital component of carbon and nitrogen cycling. To have a complete understanding of these nutrient cycles, researchers must develop a better understanding of fine root senescence—the aging and eventual death of fine roots. It is very difficult to determine if a root is dead, so a reliable method of inducing root senescence would be beneficial to this field of study.  
  
Girdling kills the sugar conducting cells of the plant, called the phloem.  This can be accomplished through exposing cells to high heat using steam.  This method has been practiced on leaf petioles and reproductive pedicels, but not on roots.  The vitality of cells can be measured using a triphenyltetrazolium chloride (TTC) assay.  If the cells are alive and, therefore, respiring, clear TTC is reduced to red tetraformazan (TF).  This assay has been used on many plant parts, including roots.
  
### Project Objectives
- Determine whether steaming kills root cells
- Determine how long a root must be steamed to achieve cell death
- Determine whether the diameter of the root affects the necessary length of steaming

### Methods and Metadata
  Roots of *Pisum sativum* seedlings were left alone for live controls, boiled for 15 minutes for dead controls, or exposed to steam for various steam times.  Sections of tap root and lateral roots were taken from each plant.  After sitting in TTC solution, absorbance (at 490 nm) was measured on a microplate reader.  After drying, masses of root samples were measured.
  
   In the data folder of this repo, you will find a CSV file called "FinalDataPeas".  This dataset has the following columns:
1. **Date**- the date on which the plants were placed in TTC (whether alive, boiled, or steamed)
2. **Plant**- the plant identity number for each individual
3. **Smp**- the sample number 
	- Each plant number has a pair of sample numbers because one sample was the tap root and one was lateral roots.
4. **Trmt**- the treatment
	- "L" = live controls
	- "B" = dead (boiled) controls
	- Numbers = number of seconds steamed
5. **Tap_Lat**- indicates whether the sample was from tap or lateral roots
6. **Diam**- diameter of tap root or diameter of one representative lateral root from sample in millimeters
7. **Tube_Mass**- mass of the tube prior to the addition of the sample in milligrams
8. **Tube_Smp**- mass of the tube containing the sample in milligrams
9. **Smp_Mass**- dry mass of the sample in milligrams
10. **Plate**- position of the sample on the plate used in the microplate reader
11. **Raw_Abs**- absorbance as measured by the plate reader with a 490 nm filter
12. **Abs_Blk**- absorbance after subtracting out the mean of the blank wells
13. **Abs_Mass**- absorbance corrected for sample size by dividing by dry mass
 
 ### Structure of the Code and How to Run It
  This repo contains three folders you will need to run the code:
  
 1. **data**- contains the CSV file described above
 2. **figs**- will contain three pdfs of the three main figures once code is run
 3. **scripts**- contains 2 markdown files with code
    - SteamGirdlingExploratoryAnalysis
    - SteamGirdlingTimesFinalAnalysis
	    
#### To recreate my results, you will need a directory containing all three of these folders.  The exploratory markdown file contains relatively unorganized code where I originally determined which data to use, what types of models I needed, etc.  The final 	analysis markdown file contains the code for the best models and the figures and statistics I will be using for my paper.

  If you only run the final analysis file, please be aware that the mass corrected absorbance was decided to be unusable because of unreliability of the scale used.  
  
### Acknowledgements
Coauthors of this research include Dr Bridget Piculell, Dr. Seth Pritchard, and Dr. Allan Strand.

Thanks to Dr. Daniel McGlinn for help with this analysis and to Dr. Courtney Murren for making her lab available for massing samples.
