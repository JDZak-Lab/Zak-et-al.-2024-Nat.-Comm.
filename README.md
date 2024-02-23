**README ZAK ET AL 2024 NAT COMM **

All imaging datasets are provided as a mean z-scored value of five seconds after the onset of odorant delivery. 

Datasets will open as a cell array where each cell is an imaging field organized in a matrix with the following dimensions, region of interest x odorant x trial. Missing observations are padded with NaN. 
An exception is made for “glomeruli_concentrations. This data is provided as a single matrix organized as: region of interest x odorant.

For concentration-related data, odorants are interleaved. An index of ascending odorant order is provided for each dataset. Position 1 in each index corresponds to a blank odorant trial.
Figure 6 index: 1 16 14 12 10 8 6 4 2
Supplementary Figure 6 index: 1 17 15 13 11 9 7 5 3
Note: Indices 18-25 are not used in this publication. 

For single odorant data, the odorant in position 1 corresponds to a blank odorant. The following odorant indices are provided in the publication. 

For mixture experiments, for both bouton datasets, the blank odorant index is position 8. The remaining 100 odorants follow the index in supplementary table 3. 

Data extraction code uses a modified version of the CaImAn CMNFe pipeline (https://github.com/flatironinstitute/CaImAn) and NoRMCorre for motion correction and denoising (https://github.com/flatironinstitute/NoRMCorre). To execute run the function “extract_imaging_data.m”. Input requires an integer “frame_rate” and a logical for running motion correction. Data must exist in a directory containing.tiff files.
