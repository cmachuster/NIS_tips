
## Context
Prior to acquire a Large Image, it is advised to perform a stage calibration.
This calibration will "synchronize" the motion of the stage with the field of view of the camera, its pixel calibration, its orientation and its angle of rotation.
It will make sure that the fields of view acquired are will oriented and it will help a lot for the stitching.

This calibration is stable, but in case some mechanical motion (slight motion of the camera) or thermal difference occur it might make sense to perform it once in a while.

## How to perform the calibration

1. A sample has to be mounted on the microscope and the focus been made.

>[!note] The sample can be imaged in transmitted light or in fluorescence

>[!warning] the contrast of the image has to be good enough otherwise the following automated calibration might fail

2. go Live and right-click on the image to find : ***Calibrate Automatically objectiveXXX***
![[stage_calibration_1_annotated.png|400]]

==OR== go to the menu ***Calibration > Calibrate Automatically objectiveXXX***

![[stage_calibration_2_annotated.png|300]]

and choose the ***Auto*** mode and press ***OK***

![[stage_calibration_3.png|300]]

The stage will now move around the sample and detect the differences in orientation, angle and distances.

At the end of the calibration, you will receive a message confirming the calibration went well 🎉.