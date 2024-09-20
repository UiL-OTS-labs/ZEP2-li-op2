# Experiment: Text Reading

## Description

Purpose of this experiment is to record a participant's eye-movements
while he/she is reading a short text. For each trial a text is
presented on the screen. Participant's task is to read text and
optionally respond to a true/false statement about the text.
Self-paced. Output: Eye-Tracking data as collected by the eye-tracker.

## Original Author

Theo Veenker <theo.veenker@beexy.nl>

## Client:

Li

## introduction

This experiment is setup for running a reading experiment with zep-2.6. By default
the script is tailored for adult participants, using an Eyelink 1000.

## Using the eyetrackers

There are two eyetracking modules in the test directory. By default the one for
adults is selected in test/task.zm

```
import eyetracker;
// import eyetracker_infant;
```

So if you want to run this with infants, comment the first an uncomment the second.

In the files ```task/eyetracker.zm``` and  ```task/eyetracker_infant.zm``` you can
see the lines:

Select the right eyetracker for your experiment.

Another import is relevant to the type of eyetracker you want to interface. Above
you can see:

```
// Import the module corresponding to the eye-tracker device being used.
// import std_et_dummy;
import std_et_eyelink;
//import std_et_tobii;
```

### Select the right eyetracker.

In order to set the optimal distance you can configure this in the module you have
chosen above. For the eyelink 1000 60 mm is appropriate, for the eyelink portable
duo, 520 mm is best. You can select this in the ```EyeTracker eyetracker``` instance
in the setup

## Running the experiment

For information on running the experiment and extracting the experiment
results please go the the Zep website at http://www.beexy.nl/zep and check 
out the documentation section. There you'll also find explanations and 
instructions that help you understand and modify a Zep experiment.


### DISCLAIMER

This experiment script is released under the terms of the GNU General Public
License (see http://www.gnu.org/licenses/gpl-2.0.html). It is distributed in
the hope that it will be useful, but with absolutely no warranty. It is your
responsibility to carefully study and test the script before using it with 
real participants.
