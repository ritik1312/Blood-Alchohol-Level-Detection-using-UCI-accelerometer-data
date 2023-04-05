# Blood-Alchohol-Level-Detection-using-UCI-accelerometer-data

Link to the [UCI Bar Crawl accelerometer dataset](https://archive.ics.uci.edu/ml/datasets/Bar+Crawl%3A+Detecting+Heavy+Drinking#)

## Dataset Description


Data was originally collected from 19 participants, but the TAC readings of 6 participants were deemed unusable by SCRAM [1]. The data included is from the remaining 13 participants.

Accelerometer data was collected from smartphones at a sampling rate of 40Hz (file: all_accelerometer_data_pids_13.csv). The file contains 5 columns: a timestamp, a participant ID, and a sample from each axis of the accelerometer. Data was collected from a mix of 11 iPhones and 2 Android phones as noted in phone_types.csv. TAC data was collected using SCRAM [2] ankle bracelets and was collected at 30 minute intervals. The raw TAC readings are in the raw_tac directory. TAC readings which are more readily usable for processing are in clean_tac directory and have two columns: a timestamp and TAC reading. The cleaned TAC readings: (1) were processed with a zero-phase low-pass filter to smooth noise without shifting phase; (2) were shifted backwards by 45 minutes so the labels more closely match the true intoxication of the participant (since alcohol takes about 45 minutes to exit through the skin.) Please see the above referenced study for more details on how the data was processed

Number of Instances:
Accelerometer readings: 14,057,567
TAC readings: 715
Participants: 13

Number of Attributes:
- Time series: 3 axes of accelerometer data (columns x, y, z in all_accelerometer_data_pids_13.csv)
- Static: 1 phone-type feature (in phone_types.csv)
- Target: 1 time series of TAC for each of the 13 participants (in clean_tac directory).

For Each Attribute:
(Main)
all_accelerometer_data_pids_13.csv:
time: integer, unix timestamp, milliseconds
pid: symbolic, 13 categories listed in pids.txt
x: continuous, time-series
y: continuous, time-series
z: continuous, time-series
clean_tac/*.csv:
timestamp: integer, unix timestamp, seconds
TAC_Reading: continuous, time-series
phone_type.csv:
pid: symbolic, 13 categories listed in pids.txt
phonetype: symbolic, 2 categories (iPhone, Android)

(Other)
raw/*.xlsx:
TAC Level: continuous, time-series
IR Voltage: continuous, time-series
Temperature: continuous, time-series
Time: datetime
Date: datetime

Missing Attribute Values:
None

Target Distribution:
TAC is measured in g/dl where 0.08 is the legal limit for intoxication while driving
Mean TAC: 0.065 +/- 0.182
Max TAC: 0.443
TAC Inner Quartiles: 0.002, 0.029, 0.092
Mean Time-to-last-drink: 16.1 +/- 6.9 hrs
