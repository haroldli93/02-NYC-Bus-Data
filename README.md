# Exploratory Analysis of NYC Bus Data

<p align="center">
![alt tag](https://github.com/haroldli93/02-NYC-Bus-Data/blob/master/MTA%20M5%20Bus%20Hairline%20Chart.png)
</p>

The MTA Bus Time App currently does a great job providing real-time information on bus locations and arrival estimates. However, I have noticed that the app has seemed to consistently underestimate the time it takes for buses to arrive. As a result, this project seeks to explore the real-time bus data provided by the Bus Time API and examine if there are any systematic errors and patterns that we can exploit to create better bus time predictions.

The image above is a visualization of the M5 southbound bus line on February 23rd 2016. Each hairline represents a particular bus's arrival to a particular bus stop and how the prediction error varies with its distance from the stop. Looking at other bus lines, we were able to model the prediction error (or lateness) given a certain distance as a Gaussian process where the mean is proportional to the distance and the standard deviation is proportion to the square root of the distance.

Furthermore, we were also able to notice significantly different lateness distributions at different times of the day. See [this graph](https://github.com/haroldli93/02-NYC-Bus-Data/blob/master/MTA%20Bus%20Lateness%20Distribution.png) for details.

If I were to invest more time on this project, I would modify my analysis to retrieve and update lateness distributions in real time, and use this information to build an app that rivals the MTA Bus Time App.
