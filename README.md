# Calibration light scattering - carbon per cell
The goal of the experiment was to calibrate light scattering measured by our BD Influx cell sorter and two SeaFlow instruments into cellular carbon content using phytoplankton cultures of various shapes and sizes. 

We used cultures grown under continuous light and monitored the cultures daily to ensure cells were growing expoentially at the start of the experiments (see [notebook.pdf](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/notebook.pdf) for details). We measured cell abundance using BD Influx cell sorter (see [influx-cultures.csv](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/influx-cultures.csv)) and total particulate organic carbon in triplicate using CHN analyzer (see [poc-data.csv](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/poc-data.csv)). Estimates of carbon cell quotas for each culture (see [Qc-cultures.csv](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/Qc-cultures.csv)) were calculated by normalizing POC by cell number. 

The entire analysis used to generate carbon cell quotas is available in [analysis_influx.R](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/analysis_influx.R). Raw CHN data are available in [UW_Exp_PCPN_DATA_FR.xlsx](https://github.com/armbrustlab/fsc-poc-calibration/blob/master/UW_Exp_PCPN_DATA_FR.xlsx); raw FCM files can be downloaded using [Dat](https://docs.datproject.org/install), to download the files, type in the terminal ```dat clone dat://cdfef982ea4032592e454c1a39b0a3855738b309d7e78ef8b2d0152adc5ffd02```

The light scattering property of each cell (alive, not fixed), normalized by 1 micron beads, was then measured by our BD Influx cell sorter and two SeaFlow instruments (#751 and #740). A linear regression model (type II) was then used to fit normalized forward light scatter to carbon content per cell. The plot below shows the BD influx calibration curve.

![alt text](Influx-Qc-scatter.png "BD Influx calibration of forward scatter normalized by 1 micron beads")

We still have a few extra FCM samples that we will be happy to share. Contact us if you are interested (ribalet@uw.edu) 

François Ribalet, Angelicque White, Katie Watkins-Brandt, Rhonda Morales, Megan Schatz & Virginia Armbrust contributed to this project.
