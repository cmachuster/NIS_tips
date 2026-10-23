### use case : Incorporate diascopic lightpaths into episcopic lights 

Many users (especially those with Elements experience pre 5.30) find it frustrating to 2 click between brightfield and epi when setting up their experiments (lightpath + OC), this removes that hurdle so a single click (OC) is needed.

<img src="lightpath-EPI - annotated.png" width="300">

In order to get access to brightfield you will need to open the device manager, and in the EPI light path :

1. right click on the DIA light and 

<img src="Device-Manager - Rule 1 - annotated.png" width="200">

2. set rules so that the on/off and power is controlled within the OC.

<img src="Device-Manager - Rule 2 - annotated.png" width="250">

The EPI lighpath will then have access to the DIA shutter and its intensity

<img src="lightpath-EPI-updated - annotated.png" width="300">



>[!note] N.B. : 
If there is a motorised condenser turret you will also need to right click on this and again to select to set rules so its position is set in the OC. This will then allow you access to the DIA light and condenser position in the Ti2/NiE pad.