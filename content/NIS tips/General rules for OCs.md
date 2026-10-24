
## What are OCs

Optical Configurations (OCs) are "shortcuts" used by NIS to set the different components of the microscopes in a certain way.
It defines the optical path and the associated hardware settings required for a particular imaging condition, allowing the user to switch reproducibly between different observation modes.

Depending on the microscope and the installed hardware, an optical configuration may include:
- **Illumination mode** : transmitted light, fluorescence, DIC, or other available techniques.
- **Optical path selection** : excitation and emission filters, dichroic mirrors, shutters, and light-path routing.
- **Optical components** : selected objective, magnification, or other motorized optical elements.
- **Acquisition-related settings** : camera port or detector path and other hardware parameters associated with the selected imaging mode.

>[!note] N.B.
>This OCs can be saved as an `.xml` file to be restored in the future or shared, see [[How to backup Layouts and OCs]]
## Creating an OC
Here are the recommended steps to create a new OC:
### Select the desired imaging mode
Define the observation conditions, such as :
- fluorescence filter and filter cubes, 
- lightpath selector (light going to the eyepiece or camera port), 
- used light source (DIA lamp, excitation light sources), 
- opened/closed shutters in the lightpath 
- other motorized devices available
by setting them manually on the microscope or the Acquisition Panel.    
### making a new OC
 To create an OC you can either go to :
 - the menu Calibration >> New Optical Configuration...
 ![[OC_saving_1_annotated.png|300]]
 - click on the "+" button on top right corner of the Acquisition Panel
 ![[Acquisition_panel_top_annotated.png|300]]

### Optical configuration window

The "Optical configuration" Window should pop out:
![[OC - creation - annotated.png|600]]

This window is very important to make sure the OC behave the way you want it. 
It basically gives the choice to set what part of microscope should move when you click on it and/or how the resulting image should look like.
Here are some descriptions of this window :
1. ==🔴Name== : gives the name of the OC itself
2. ==🔴Name== : gives the name


3. Configure the optical hardware.
Set the relevant optical components to the required positions, including excitation and emission filters, dichroic mirrors, shutters, light-path selectors, and other motorized devices available in the system.    
3. Configure the associated acquisition hardware.
Select the appropriate detector or camera path and any hardware settings that need to be associated with the imaging mode.    
4. Verify the optical path.
Check that the selected components are correctly positioned and that the resulting image is consistent with the intended imaging conditions.    
5. Save the Optical Configuration.
Store the current optical state as an OC with a meaningful name, typically identifying the channel or imaging mode.    
6. Validate recall and reproducibility.
Switch to another configuration, then recall the new OC and verify that the microscope returns to the expected optical state.





## recommanded settings when creating an OC
Here are some recommended parameters to set when creating new OCs

<img src="OC - annotated.png" width="500">

1. uncheck light source « xxx Power » used devices → it applies to every light sources linked to the OCs : Lasers, AOTF, LEDs (transmission and EPI)
2. Set an Active Shutter (Shutter that switches ON during acquisition and OFF when not acquiring) for the OC → should the main shutter for the light source
>[!warning] make sure that the chosen Active Shutter is not a mechanical one
3. uncheck "Objective"

### also
- Always check the box for camera settings, this is often needed for use in ND Acquisition
- The channel name can be different from the OC name, and should only refer to the colour / wavelength of the emission light
### extra parameters to take into account with OCs
Global OC settings exist when it comes to automatically save values.

As they are global (will apply to all **OCs**) they are found in the « Options » window, in the « General » section.

<img src="Option-general - annotated.png" width="400">

The most important to know are the « Save changes to optical configuration automatically ».

For the following parameters, changes done by the user will not generate an «❗» in the OCs button as this setting(s) will be automatically saved.
- **Exposure Only** -> only the exposure time will be saved (not the camera settings : speed, bit depth…)
>[!note] This is the default setting
- **All Camera Settings** -> all changes done in the camera tab will be saved (exposure + speed + bit depth…)
- **All Brightness Settings** -> all the camera settings **AND** the other settings such as light source chosen and their power, filter cubes…
