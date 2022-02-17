# RaspPi
This is my remote repository for my Raspberry Pi vehicle sensing system. The most current or on-going detection session will be in the run branch. Other branches will be documented sessions and will be numbered accordingly. 

#### Branch: run
The run branch is meant to be the most current or on-going data collection branch. This is the current data collection session. 

#### Branch: Test_Run_1 
This was my first data collection session. It lasted around 12 hours between the 10PM - 11AM. The program crashed due to a lack of exception handling for the git push automation script. From my analysis, the cause of the failure was likely due to a brief internet connection problem. 

#### Branch: Test_Run_2
Problem: Events 334 and 336 was a pedestrian. Problem: Vehicles that enter and exit the neighborhood at excessive speeds will be detected but the camera will not snap a photo quick enough to capture the speeding vehicles. Todo: I am going to specify the sequence of motion so that only vehicles entering the neighborhood are registered at detection events. 
