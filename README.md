# Data & Analysis Code
Aberrant Sensory Encoding in Patients with Autism  
Jean-Paul Noel*, Ling-Qi Zhang*, Alan A. Stocker, and Dora E. Angelaki  
https://www.biorxiv.org/content/10.1101/2020.03.04.976191v1  

## Dependencies
- [MATLAB cbrewer](https://www.mathworks.com/matlabcentral/fileexchange/34087-cbrewer-colorbrewer-schemes-for-matlab)
- [MATLAB circular statistics toolbox](https://www.mathworks.com/matlabcentral/fileexchange/10676-circular-statistics-toolbox-directional-statistics)
- We have already included them here (`cbrewer`) and (`CircStat`), but would like to explicitly acknowledge the use of these two packages.

## Data
- For most of the analysis, we use the `.mat` files in the root directory are data for the combined subject across conditions; Data for each indivudal subject can be found in `./woFB` (without feedback), `./wFB1` (with feedback 1), and `./wFB2` (with feedback 2).

## Code Usage
- **Set the current directory of MATLAB to the root directory of this project.** See special instructions below for reproducing Figure S5 and S6.  
- Each folder contains one or more matlab script(s) (and other helper function files) that produce the corresponding figure in the paper, as indicated by its name.
- Run the "addpath" section first with the "Run Section" function in MATLAB (to include libraries and other helper functions), and then run the entire script.
- Here is a short summary of the structure of this repo:
```
...
├── *.mat                   # Data file for the combined subject
├── woFB                    # Individual data in the no feedback block    
├── wFB1                    # Individual data in the first feedback block
├── wFB2                    # Individual data in the second feedback block
├── Figure_1_S7_S8
    ├── fig1_fisher.m       # Simulation for Figure 1D-F
    ├── figS7.m             # Simulation for Figure S7        
    ├── figS8.m             # Simulation for Figure S8
    ├── ...
├── Figure_2
    ├── fig2_subject.m      # Plot data for individual subject (Figure 2)
    ├── ...
├── Figure_3
    ├── fig3_combined.m     # Plot and analysis for the combined subject (Figure 3, Figure 4A, B)
    ├── ...
├── Figure_4
    ├── fig4_parameter.m    # Extract parameter from the combined subject (Figure 4D, E)
    ├── ...
├── Figure_5_S3_S4          # Analysis related to extracting parameter from individual subjects
    ├── Fig5_corr.m         # Plot and analysis for Figure 5
    ├── FigS3_S4.m          # Plot data for Figure S3, S4
    ├── ...
├── Figure_S1_S2          
    ├── figS1_S2.m          # Plot data for all individual subject (Figure S1, S2)
    ├── ...
├── Figure_S5_S6            # See special instructions below for running these analysis 
    ├── figS5_rt.m          # Plot reaction time data 
    ├── slidingAnalysis
        ├── figS6_fb.m      # Sliding window analysis for Figure S6
    ├── ...
```

- For Figure S5 and S6, we reformatted the data file so it contains the reaction time. To run the analysis, set MATLAB's current directory to `./Figure_S5_S6`. Run `figS5_rt.m` for the reaction time analysis, and `figS6_fb.m` for the sliding window analysis.


## Contact 
Please address any questions you have to **lingqiz at sas dot upenn dot edu**
