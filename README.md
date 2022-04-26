# Small Data Collection Project
This is my remote repository for my Raspberry Pi vehicle sensing system. The most current or on-going detection session will be in the run branch. Other branches will be documented sessions and will be numbered accordingly. 

#### Software and Hardware
Hardware and Materials: Raspberry Pi, 2 PIR infrared sensors, 100+ ft of copper wire, plastic straps, electrical tape, scrap wood, cotter pins, and (Dollar Store) lunch containers. </br>
Software: Raspberry Pi OS, Shotcut (video editing), Thonny IDE, Notepad++, Python, Jupyter Notebook, Pandas, numpy, pandas, matplotlib, and Seaborn. 

#### Vehicle Orientation <br />
If the vehicle is facing towards the right, then this means the vehicle is entering the neighborhood. <br />
If the vehicle is facing towards the left, then this means the vehicle is exiting the neighborhood. <br />

#### Helpful Videos
Video showing the setup: [Video](https://youtu.be/AtLLw0zP6xo) </br>
Video of the system in action: [Video](https://youtube.com/shorts/4ZKKAbR_2Y0) </br>
Video about how I drilled holes in cheap plastics: [Video](https://youtu.be/wgfiUo_gUog) </br>
Video touching on how to access the Raspberry Pi without a physical connection: [Video](https://youtu.be/GoeHuRcHIoU) </br>

#### Project Presentations
[Full Version](https://youtu.be/-CiQISIRM7Q) | [Shorter Version](https://youtu.be/-CiQISIRM7Q)

#### Sensor 4 Photos
![Sensor 4](https://github.com/EthanNValencia/RaspPi/blob/master/images/Sensor4.png?raw=true)

#### Sensor 17 Photos
![Sensor 17](https://github.com/EthanNValencia/RaspPi/blob/master/images/Sensor17.png?raw=true)

#### Branch: run
The run branch is meant to be the most current or on-going data collection branch. This is the current data collection session. Status: Not Running.

#### Branch: Test_Run_1 | [Video](https://youtu.be/_8nmh4hD2vQ)
This was my first data collection session. It lasted around 12 hours between the 10PM - 11AM. The program crashed due to a lack of exception handling for the git push automation script. From my analysis, the cause of the failure was likely due to a brief internet connection problem. 

#### Branch: Test_Run_2 | [Video](https://youtu.be/D95GhDzAvH0)
This was the second data collection session that I ran. It ran over 24 hours from 2022-02-15, 17:44:30 to 2022-02-16, 22:06:36. I terminated it manually to implement changes. 
Problem: Events 334 and 336 was a pedestrian. Solution: Cut new cups to narrow the sensor field. 
Problem: Vehicles that enter and exit the neighborhood at excessive speeds will be detected but the camera will not snap a photo quick enough to capture the speeding vehicles. Solution: Will place the camera at an angle. 
Todo: I am going to specify the sequence of motion so that only vehicles entering the neighborhood are registered as detection events. 

#### Branch: Test_Run_3 | [Video](https://youtu.be/H0IJAulo1W4)
This was the third data collection session that I ran. It ran for almost 3 days, from 2022-02-17, 18:06:25 to 2022-02-20, 16:30:34. There were 722 detection events. I terminated the session manually to implement changes. 
For this run session, I increased the sensitivity of the motion sensors. I cut new sensor housings so that their field of detection would be more narrow. I changed the program so that sequential motion needs to begin from sensor on the left and then proceed to the sensor on the right. This way my detections should be from vehicles traveling into the neighborhood. I also adjusted the timings. 

#### Branch: Test_Run_4 | [Video](https://youtu.be/6Qu4zs0RW2E)
This was the fourth data collection session that I ran. It ran from 2022-02-20, 22:34:49 to 2022-03-01, 20:01:48 (over a week). There were 1123 detection events. I terminated it manually due to problems viewing the GitHub repo on my cellphone.  
New features: Implementing an optocoupler to remove the physical electrical connection between the Raspberry Pi and the motion sensors in the trees. Made minor changes to the order in which the threads can declare a detection event. Going to change the camera settings to hopefully increase the photo quality at night time. Note: Optocoupler didn't work, so I removed it and ran the session. 

#### Branch: Test_Run_5 | [Video](https://youtu.be/8f5Uv7pZ_gE)
This was the fifth data collection session that I ran. It ran from 2022-03-02, 08:21:22 to 2022-03-09, 17:12:38 (about a week). I adjusted the thread timings. Attempting to get better vehicle placement in my photos. There were 845 detection events. Session was manually terminated. 

#### Branch: Test_Run_6 | [Video](https://youtu.be/4wf57RXZXks)
This was the sixth data collection session that I ran. It ran from 2022-04-04, 19:34:27 to 2022-04-10, 19:16:30. There were 1013 detection events. Session was manually terminated. Note: There were false detection events due to the tree branches. I had to trim the branches during this session. 

# Seaborn Charts
These charts are derrived from 3 seperate data collection sessions. These individual sessions can be viewed in greater detail on these branches: Test_Run_3, Test_Run_4, and Test_Run_5. It is important to understand that the sessions took place from: 2022-02-17 to 2022-02-20 (3 days), 2022-02-20 to 2022-03-01 (9 days), and from 2022-03-02 to 2022-03-09 (7 days). Non-precisely speaking, this is 19 days of data collection. 

#### Total Occurences Per Hour
This chart shows the total number of occurences that occured on an hourly basis. For example, every detection event that the system processed in the hour of 15 (3 PM) is charted.</br>
![chart 1](https://github.com/EthanNValencia/RaspPi/blob/master/images/SeabornChart1.png?raw=true)

#### Event Detections By Hour and Minute
This chart shows occurences by hour and minute. This chart might not be particularly useful, however, I think it does tell a story. The story that is told by this chart is that at certain times of the day it is possible for a vehicle to be detected entering the neighborhood at any time. It is important to understand that the data collection period is around 19 days. </br>
![chart 2](https://github.com/EthanNValencia/RaspPi/blob/master/images/SeabornChart2.png?raw=true)

#### Event Detections Per Day
This chart shows the total occurences per day. The significant amount of vehicle detections on 2022-02-18 and 2022-02-19 are a little strange. I reviewed the footage of those days and they appear to be mostly accurate detection events. I'm not sure why there were so many vehicles passing the house that day. It could have been due to a a few solar panel installs that took place around that time. 
Speculation: The huge bumb makes me think there was something wrong with my data collection. It makes me think that my system wasn't correctly detecting as many vehicles as it should have. </br>
![chart 2](https://github.com/EthanNValencia/RaspPi/blob/master/images/SeabornChart3.png?raw=true)

#### Average Detections Per Hour
This chart shows the average amount of vehicles that enter the neighborhood per hour. It can be observed that there isn't a lot of activity per hour. 16 vehicles per hour is the highest average rate. Note: The data could be a little skewed because I didn't necessarily begin data collection sessions at the beginning of an hour. 
</br>
![chart 2](https://github.com/EthanNValencia/RaspPi/blob/master/images/SeabornChart4.png?raw=true)

