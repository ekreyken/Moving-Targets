# Moving Targets Code
Matlab project code designed to move 4 coloured (equiluminus on experimental display) placeholdors (empty boxes) within a central location on-screen.

This project was designed to run an experiment that determined whether reaction times differed significantly (statistically) between a target presented in the same location, one of two adjacent locations, or opposite location to a cue. This presents with 16 "valid" trial combinations, plus another 4 "invalid" trial combinations in which a cue is present but a target is not.

Upon beginning the program, a participant would enter their participant ID and then read instructions relating to their experimental performance.

Each experimental block (blocks of trials presented to a participant in one set, separated by a short break) is preceeded by instruction text.

Each trial shows 4 coloured square placeholders (equidistant from center) around a diamond fixation point. These and all objects (cues, target) were created within Matlab using PsychToolBox (http://psychtoolbox.org/) 


Each trial is constructed within initializeBlocksAndTrials.m. Each relative position of Cue and Target is identified and created (including invalid trials), then multiplied by the number of required trials and blocks (varies per experiment). The trial order for each block is then randomized.

Each trial begins with the presentation of the 4 placeholders and central diamond. A fixed radius circle apears in one of the placeholders. After a fixed time, it is removed from the display. 
The boxes then turn white, and are randomly flung around the screen. There are several versions of this experiment (fast movement, slow movement, random movement, non-random movement, etc.), but if you get this working on your computer it's hilarious.

Finally, either a square target appears in one of the placeholders and requires a response from the participant (else an error tone will sound after 1500ms and the program will move to the next trial), or nothing appears and requires the participant to withhold their response (else an error tone will sound after 1000ms and the program will move to the next trial). Participants will be prompted 

Trials are recorded for experimental display, accuracy, and participant timing throughout the trial and exported as .mat files for later analysis.

Participant demographics are collected following the experiment via Matlab-created form and exported as .mat for later analysis.

Programming Data Reduction for this project includes:
a) Identifying valid and invalid reaction time data (i.e. responding on invalid trials, failure to respond on valid trials)
b) Identifying the proportion of valid and invalid trials per participant and determining each participants' contribution to the final results
c) Computing reaction time medians, averages, and variances for each of 16 possible trial combinations.
