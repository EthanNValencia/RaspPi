# RaspPi
This is my remote repository for my Raspberry Pi vehicle sensing system. The most current or on-going detection session will be in the run branch. Other branches will be documented sessions and will be numbered accordingly. 

#### Branch: run
The run branch is meant to be the most current or on-going data collection branch. This is the current data collection session. 

#### Branch: Test_Run_1 | [Video](https://youtu.be/_8nmh4hD2vQ)
This was my first data collection session. It lasted around 12 hours between the 10PM - 11AM. The program crashed due to a lack of exception handling for the git push automation script. From my analysis, the cause of the failure was likely due to a brief internet connection problem. 

#### Branch: Test_Run_2 | [Video](https://youtu.be/D95GhDzAvH0)
This was the second data collection session that I ran. It ran over 24 hours from 2022-02-15, 17:44:30 to 2022-02-16, 22:06:36. I terminated it manually to implement changes. 
Problem: Events 334 and 336 was a pedestrian. Solution: Cut new cups to narrow the sensor field. 
Problem: Vehicles that enter and exit the neighborhood at excessive speeds will be detected but the camera will not snap a photo quick enough to capture the speeding vehicles. SOlution: Will place the camera at an angle. 
Todo: I am going to specify the sequence of motion so that only vehicles entering the neighborhood are registered as detection events. 

#### Branch: Test_Run_3 | [Video](https://youtu.be/H0IJAulo1W4)
This was the third data collection session that I ran. It ran for almost 3 days, from 2022-02-17, 18:06:25 to 2022-02-20, 16:30:34. I terminated it manually to implement changes. 
For this run session, I increased the sensitivity of the motion sensors. I cut new sensor housings so that their field of detection would be more narrow. I changed the program so that sequential motion needs to begin from sensor on the left and then proceed to the sensor on the right. This way my detections should be from vehicles traveling into the neighborhood. I also adjusted the timings. 

#### Branch: Test_Run_4 | Video Currently Unavailable
This was the fourth data collection session that I ran. It ran from 2022-02-20, 22:34:49 to 2022-03-01, 20:01:48 (over a week). I terminated it manually due to problems viewing the GitHub repo on my cellphone.  
New features: Implementing an optocoupler to remove the physical electrical connection between the Raspberry Pi and the motion sensors in the trees. Going to make minor changes to the order in which the threads can declare a detection event. Going to change the camera settings to hopefully increase the photo quality at night time. Note: Optocoupler didn't work, so I removed it and ran the session. 
