# Metabolic Cage Analysis
- Takes a .csv file from the CLAMS metabolic cage monitoring software (CLAX) and cleans, averages, and plots group data
- Allows users to specify whether cages contain experimental or control mice.
- Allows users to screen for and exclude system artifacts
- Consolidates and graphs key data by group, including respiratory exchange ratio (RER), oxygen, movement, and food and water intake.
- Plots experimental vs. control groups and allows customizable smoothing and time window selection.
- Saves .mat matrix of all individual ("full_graphing_variables.mat") and averaged ("full_metabolic_matrix.mat") data
- Also saves parameters used in session ("RERParameters.mat")

1. Export a .csv of the metabolic data from CLAX software (click data, check "all", click export and save as "all.csv")
2. Open "full_metabolic_analysis.m"
3. Follow the intructions in the comments to specify your desired parameters. You can select certain cages to exclude, the time frame to examine, and downsampling and smoothing options.
4. Run "full_metabolic_analysis.m" from the same folder as your "all.csv" experiment information.
5. On the first run, you will have the option to scan your data for artifacts from the system. The CLAMS metabolic cages often are influenced by electrical noise that will be visible across all cage sensors. This program will display all cage RER data in discrete windows. If you see artifacts that are present across all cages, click to the left, then the right boundary of where you see the artifacts. If you see no artifacts, press enter to continue.
6. The program will then graph individual mouse data and group average data, saving all figures and extracted data.
