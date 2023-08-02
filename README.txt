1. ANOMALY DETECTION AND TIME SERIES ANALYSIS:

In this part, i have written a code in which first i take only important data from the datset and then visually represent the performance of the sensor hourly and daily. After checking the behaviour of the some of the sensors such as Eng. speed, Acc. Pedal Position, Eng. Total Fuel Used and many other we can see that at day 6th of july and 29th of july we have the highest anomaly in which the data gathered from the sensors are having a big difference with the rest of the data. 
Between 1st of may 2023 until 10th of jun 2023 the values are having similar trend for most of the sensors data.
The anomaly detection model used is Isolation Forest which is a powerful model for time series data. Although the data was gathered at an average of 6 hours and 3 minutes and 9 seconds, the model well performed and with a contamination hyperparameter of 0.02, most of the anomalies can be detected.

2. Prediction

In this part, XGBOOST algorithm was used to perform forcasting of behaviors of the sensors. for this part i made features as hours and days. and after training the model as it can be seen from the plot, eventhough the data was very less for such a training the performance was acceptable and the values of 14.65 RMSE was achieved.
Overall, for training a good model for prediction we need to have a very large dataset for each sensor and the time of observations should be at least every 10 mins or 30 mins.

3. Condition Monitoring

In this part i first found all of the anomaly points in all of the sensors and then i ploted all of them with their corrosponding data. There are 66 sensors. Lastly i developed a simple algorithm for condition monitoring since the plots and the frequencies are not too many. The algorithm is based on the anomaies found previously in which i make a threshhold range for the sensor (i only calculated it for 5 sensors since there were 66 and just for the purpuse of illustration and performance of the algorithm) using the anomalies i find in each sensor.And in case of passing the threshhold i print out an Alert massage and if its between the range i print a stable massage.