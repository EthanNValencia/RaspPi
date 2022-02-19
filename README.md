# RaspPi
This is my remote repository for my Raspberry Pi vehicle sensing system. The most current or on-going detection session will be in the run branch. Other branches will be documented sessions and will be numbered accordingly. 

#### Branch: run
The run branch is meant to be the most current or on-going data collection branch. This is the current data collection session. 
For this run session, I increased the sensitivity of the motion sensors. I cut new sensor housings so that their field of detection would be more narrow. I changed the program so that sequential motion needs to begin on the entrance side of the neighborhood. This way my detections should be from vehicles traveling into the neighborhood. I also adjusted the timings. 

#### Branch: Test_Run_1 | [Video](https://youtu.be/_8nmh4hD2vQ)
This was my first data collection session. It lasted around 12 hours between the 10PM - 11AM. The program crashed due to a lack of exception handling for the git push automation script. From my analysis, the cause of the failure was likely due to a brief internet connection problem. 

#### Branch: Test_Run_2 | [Video](https://youtu.be/D95GhDzAvH0)
This was the second data collection session that I ran. It ran over 24 hours from 2022-02-15, 17:44:30 to 2022-02-16, 22:06:36. 
Problem: Events 334 and 336 was a pedestrian. Solution: Cut new cups to narrow the sensor field. 
Problem: Vehicles that enter and exit the neighborhood at excessive speeds will be detected but the camera will not snap a photo quick enough to capture the speeding vehicles. SOlution: Will place the camera at an angle. 
Todo: I am going to specify the sequence of motion so that only vehicles entering the neighborhood are registered as detection events. 
