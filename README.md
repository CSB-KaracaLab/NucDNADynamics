# NucDNADynamics

<img src="logo.png" alt="logo" width="200" />

#### by Ayşe Berçin Barlas, Burcu Özden, Ezgi Karaca

The nucleosomes have been of great interest due to their importance in chromatin function. They are the main template for diverse vital processes, such as transcription, replication, recombination, DNA repair, and cell division. Although there are several molecular dynamics studies on how histone dynamics regulate the nucleosome function, the relevance of nucleosomal DNA dynamics is yet to be determined.

Here, we explored the role of force fields in reproducing the experimentally observed nucleosomal DNA (nucDNA) geometries and compared two state-of-the-art protein-DNA force fields, i.e., AMBER parmbsc1 and CHARMM36. 601 nucleosome, which has stable structure, was used for this study. Then, DNA geometry analysis (such as RMSD, RMSF, Groove Widths and Base Pair Parameters) were performed to understand the effect of different force fields on the nucleosome geometries.

Base pair parameters i.e., roll, twist, shift, slide, rise, tilt and minor and major groove widths were calculated by using 3DNA tool and then, they were analyzed by using Python scripts to visualize and interpret the results. 3DNA generates many files, but the file that relates to DNA geometry has an ".out" extension. (i), (ii), (iii) and (iv) are calculated from this out file with the scripts given here.

Python scripts can be used to (i) extract base pair step parameter results from 3DNA output files, (ii) extract minor and major groove widths from 3DNA output files, (iii) combine desired parameter results in a single file and (iv) find maximum, minimum and mean values of selected parameter to visualize the results. You can find our iPython notebook which includes these scripts under the "test_script" folder.

###### (i) Extracting Base Pair Step Parameters from 3DNA output files: 
This script extracts your base pair step parameters from 3DNA output files. Before running the script, you need to input your output folder name where you see *"your_output_files_directory/"* . The processed file will be saved with a.csv extension.

###### (ii) Extracting Minor and Major Groove Widths from 3DNA output files: 
This script extracts your minor and major groove widths from 3DNA output files. Before running the script, you need to specify your 3DNA output files directory name in the script instead of *"your_output_files_directory/"* locations. Your output files will be saved with the name of each output file. Example output file is given as “output_2.out.csv”.

###### (iii) Combining all extracted files into a single file: 
Your selected 3DNA output results are combined in one single file for the whole trajectory. Before running this script, you need to specify your outputs directory instead of *"our_input_files_directory/"* locations. Output file will be saved with the name of "all_results.csv" and will be an input file of the next script that calculates minimum, maximum and mean values of your dataset.

###### (iv) Finding maximum, minimum and mean values of selected parameters: 
This script calculates minimum, maximum and mean values for every parameter in your dataset. It is required to plot your range and mean value of your trajectory. Example output files are given as  “base_pair_max_min.csv” and “groove_widths_max_min.csv”.

## Simulation Setup

We run molecular dynamics simulations of the 601 nucleosome under the effect of two different force fields, i.e., AMBER parmbsc1 and CHARMM36. 
Molecular dynamics simulations performed on GROMACS 5.1.4. System solvated in a TIP3P water molecules and neutralized with 0.15 M Na+ and Cl- ions. 400 ns simulations performed under 310 K temperature for both cases.




