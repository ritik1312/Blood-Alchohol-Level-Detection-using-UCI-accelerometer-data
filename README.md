# Blood-Alchohol-Level-Detection-using-UCI-accelerometer-data

Link to the [UCI Bar Crawl accelerometer dataset](https://archive.ics.uci.edu/ml/datasets/Bar+Crawl%3A+Detecting+Heavy+Drinking#)

## Dataset Description


Data was originally collected from 19 participants, but the TAC readings of 6 participants were deemed unusable by SCRAM [1]. The data included is from the remaining 13 participants.

Accelerometer data was collected from smartphones at a sampling rate of 40Hz (file: all_accelerometer_data_pids_13.csv). The file contains 5 columns: a timestamp, a participant ID, and a sample from each axis of the accelerometer. Data was collected from a mix of 11 iPhones and 2 Android phones as noted in phone_types.csv. TAC data was collected using SCRAM [2] ankle bracelets and was collected at 30 minute intervals. The raw TAC readings are in the raw_tac directory. TAC readings which are more readily usable for processing are in clean_tac directory and have two columns: a timestamp and TAC reading. The cleaned TAC readings: (1) were processed with a zero-phase low-pass filter to smooth noise without shifting phase; (2) were shifted backwards by 45 minutes so the labels more closely match the true intoxication of the participant (since alcohol takes about 45 minutes to exit through the skin.) Please see the above referenced study for more details on how the data was processed
