This program takes data fromm the LDMX HCal prototype and deconvolves (through reverse-convolution) the noise function from the signal function.

For a full understanding, please read [the report.](https://docs.google.com/document/d/1-FgOJHY-Og2vCMAz9AdPcSCgeD4munGIvt0CJ_cmqzI/edit?usp=sharing)
 

To run the program you will need:
1. An installation of ldmx-sw with the libDetDescr module installed and configured to run on python (not provided)
2. Detector data from a run (not provided)
3. A Landau signal function modulated by Birk's law (provided)
4. A pedestal file (provided)
5. A calibration file (provided)

Once you have acquired the detector data, ensure that both halves of the detector are cross-correlated. 
Place the correlated file into the 'reconstructions' folder (you might have to create it manually).

In order to run the program:
1. Process the data file using `ldmx python3 PulseHeightExtractor.py`. Use command line arguments or edit the file directly to select the bars you want to extract. Each bar takes a few minutes, so run the script in parallel for each bar on a supercomputer to make it economical. The two bash scripts can help.

2. Analyse the extracted data files using `ldmx python3 PulseHeightAnalyser.py`. By default, it analyses layers 3-15, providing a plot of the three functions and also summary analysis plots of the whole detector. Edit the file directly to select the bars you want to analyse.





