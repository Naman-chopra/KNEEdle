# Project Description

## Input Video
The input video file `input.mp4` is located in the parent directory.

## Output Video
The output video file `untitled.mp4` is located in the parent directory and contains the results of the analysis.

## Instructions
Instructions on how to run the analysis are located in the `instructions.txt` file in the parent directory.

## Analysis
The timer starts as soon as the user bends their knee (at an angle <140), with a buffer of 1 extra second to avoid any accidental knee bend recognition. The user is advised to "keep your knee bent" and the timer restarts to 8 seconds if they straighten their leg before that point.

The stat of bendiness is determined by how far a user can bend their legs. For example, if a user can bend their legs to an angle of 80 degrees, the stat is considered to be positive. If the user doesn't bend their knee more than 120 degrees, the stat is unsatisfactory.

If the angle is measured to be less than 30 due to a visibility issue, the warning "poor visibility" is displayed. The alert "sudden change" is displayed if there is less than 1.5 seconds between two successive states (such as bent or straight) in order to control fluctuations.

## Note
Due to OpenCV's constraints, the timer may run quicker than normal when the window is being captured, and the same is true for the color distortion.
