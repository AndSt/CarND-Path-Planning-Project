#  Reflection

I began by copying the code provided in the QA. Summarized, code is provided to
hold the line, drive in the middle of the line and not drive against the
frontal car.
Unfortunately I wasn't able to get that code running properly because it always
hit a car in the front at some point. I got rid of the problem by decreasing the
 speed strongly if our car is 15 meters behind another car.

Afterwards I added a lane switching logic. Basically it looks if we're to
close to a frontal car and looks if a lane next to the current one is free for
a lane switch.
If so, it chooses one of the lines and makes the line switch.

This logic makes heavy use of the code provided by Udacity. We check whether the
left or right side is reachable as we don't want to change to the opposite
direction. Additionally we can use already provided code to check whether the
 cars on the left or right are too close. A simple lane=lane+1 allows the
translation logic (human high level thinking to machine commands
written to the simulator) to do the job. 
