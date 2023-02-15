# Supercapacitor array performance visualization
This code is used to visualize the performance parameters (capacitance, voltage, energy, and power) of a supercapacitor array with various array configurations.

## How to use
Install pandas, plotly, and numpy library (cmd: pip install plotly pandas numpy).
Change the AL_mass and Area_two_elec according to the measured value.
Place CV, GCD, and EIS data files in the "Input_data" folder.
Run the script to generate the plots and summarizing table.

## Functions
The code provides the following functions:

read_file_CV(filename, headerline): imports CV data file, cleans it, and extracts primary parameters.\
calculate_sec_param_CV(data, scan_rate, Vmax, AL_mass, Area_two_elec): calculates performance parameters from a CV curve.\
read_file_GCD(filename, headerline): imports GCD data file, cleans it, and extracts primary parameters.\
calculate_sec_param_GCD(data, I_gcd, Q_disc, Vmax, AL_mass, Area_two_elec): calculates performance parameters from a GCD curve.\

## Note
The headerline argument of the read_file_CV, read_file_GCD, and filtering_EIS functions may need to be changed depending on the file condition.
Their default values are 52, 48, 58, respectively.
If an error still occurs, also change the numbers of # at the headerline-# parts.
