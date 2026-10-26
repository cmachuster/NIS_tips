
## context
Lighpath have been introduced in NIS 5.30 and are aiming at rationalizing the way microscopes are configured and how it should interact with its devices depending on the user application.

Per default NIS will suggest some lightpaths from the devices that are declared in the Device Manager (see [[Administrating Device Manager - basics]])

The following section aims at help you understand the logic and what can be done to adapt them to your needs
## use case : Incorporate diascopic lightpaths into episcopic lights 

Per default, if a fluorescence light source is declared, NIS will ceate two lightpaths for EPI fluorescence and Diascopic imaging (for the Eye or the camera)
Some users prefer to avoid having to 2 click between DIA and EPI when setting up their experiments (lightpath + OC), this removes that hurdle so a single click (OC) is needed within one lightpath.

<img src="lightpath-EPI - annotated.png" width="300">

In order to get access to brightfield you will need to open the Device Manager, and in the EPI light path :

1. right click on the DIA light and 

<img src="Device-Manager - Rule 1 - annotated.png" width="200">

2. set rules so that the on/off and power is controlled within the OC (see [[General rules for OCs]]). It means that now the tatus of the DIA shutter will be controlled via the how you set your OC, the lightpath won't force its status anymore.

<img src="Device-Manager - Rule 2 - annotated.png" width="250">

The EPI lighpath will then have access to the DIA shutter and its intensity

<img src="lightpath-EPI-updated - annotated.png" width="300">

>[!note] N.B. : 
If there is a motorised condenser turret you will also need to right click on this and again to select to set rules so its position is set in the OC. This will then allow you access to the DIA light and condenser position in the Ti2/NiE pad.