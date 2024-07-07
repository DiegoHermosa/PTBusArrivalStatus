# Capstone: Bus Arrival Status to Stop 
### Business Understanding: ### 
Can the Public Tranportation Bus Arrival to Stop be predicted as On Time, Early Or Late?

### Data: ### 
The data comes from the Public Trasportation History database that the company I work for has developed for a Public Transportation Company. 


The data can be found in this link

[pt_bus_stop.csv](https://github.com/DiegoHermosa/PTBusArrivalStatus/tree/main/data/pt_bus_stop.csv)

### Notebook Link ###
The following notebook contains all the development of the analysis carried out.

[PTBusStopArrivalStatus.ipynb](https://github.com/DiegoHermosa/PTBusArrivalStatus/tree/main/PTBusStopArrivalStatus.ipynb)

### The techniques and Analysis ###
1. Extract the bus arrival to stop data from the Public Trasportation History database filtering a single Stop and for a date range of 3 months (April-2024 to June-2024).
2. Perform a cleaning of the information in order to eliminate redundant data and outliers.
3. Train KNN, Logistic regression, Decision tree and SVM models in search of the best one.
4. Because of the dataset is imbalanced the SMOTE oversampling techniques will be used.
   
### Dataset Understading ###
#### The dataset contains the next featues:
- ID: record unique ID
- UnitID: Unique ID assigned to the Bus unit.
- StopID: Unique ID assigned to a Bus Stop.
- StopNumber: Friendly name assigned to Stop, in general this is define by the Bus Company.
- DateIN: Date time when the Bus arrived to the Stop.
- DateOUT: Date time when Bus left the Stop.
- WeekDay: Day name of the arrival date time.
- PrevWeekDay: Day name of the previous arrival date time.
- PeakHour: (Yes/No) flag to mark the if traffic is at its worst between 7 a.m. and 9 a.m. and 4 p.m. and 7 p.m.
- StopDuration: time spent by the bus within the Stop.
- PrevDateIn: Date time when the previous bus arrived to the current stop.
- DifferencePrevBusIn: Time difference between PrevDateIn and DateIN.
- TripDuration: Time spent by the bus to complete a trip.
- Odometer: Bus odometer when it arrived to stop at DateIn.
- PrevStopOdometer: Bus odometer when it arrived to stop at PrevDateIn.
- PrevStopNumber: Previous stop.
- DistanceLastStop: Distance between the last stop visited and the current stop.
- Speed: Bus speed when it arrived to stop.
- OTPMode: Mode of calculation of the Stop status: 2 means Headway
- OnTimeStatus: Status assigned to the bus arrival (ObTime, Early, Late). This status is assigned according to Route Bus Frequency. Each 15 minutes a bus expected to arrive to each stop.
- TripDistance: Distance of the trip.
- TripSpeedAvg: Bus speed average within the trip.

### Data Preparation and Cleaning ###
1. The missing value for some feature were removed. <br/>
![image](https://github.com/DiegoHermosa/PTBusArrivalStatus/assets/160977826/2a21aa20-39b1-4098-90f3-5cea2661c515)
<br/>
3. Features with no relevant information were removed. <br/>
4. Categorical features like PeakHour and WeekDay were transformed to numerical values. <br/>

#### Correlations and Imbalance: ####
The dataset is imbalance: <br/>
![image](https://github.com/DiegoHermosa/PTBusArrivalStatus/assets/160977826/6fc415a4-eeb5-45a8-9a34-f394a7b47e96)

<br/>
The correlation allowed to identified some featues with a high correlation between them:<br/>
![image](https://github.com/DiegoHermosa/PTBusArrivalStatus/assets/160977826/116b8a4a-d532-4b06-8c57-9752b4893c8d)



<br/>





 
