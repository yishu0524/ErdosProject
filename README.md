# ErdosProject
CNN-LTSM model for sleep stages classification using byteflies EEG data

File 1: extract into csv.ipynb 

This contains code to complete the alignment of PSG and Byteflies data according to the details given in supporting_documents.

Basically, the annotation is done with PSG and then the PSG is started later than Byteflies and stops before bytefiles.
Therefore one needs to find the common time and align them.


extract into csv uses the annoatation given using PSG, align with EEG, ACC, GRY data from byteflies, then extract all data into csv file for all patients.

the resulting files from extract into csv.ipynb is saved in byteflies.zip

File 2: reform data.ipynb

This contains code to read all csv files from byteflies.zip, processed the input (moving median filter, filter out over 200 microV and flat signals) and put them together into corresponding x an y data.
This file will generate the data SleepySignals_X.npy and SleepySignals_y.npy
Note that the processed npy files are saved in SleepSignals_data.zip
