
## What are OCs

Optical Configurations (OCs) are "shortcuts" used by NIS to set the different components of the microscopes in a certain way.
It defines the optical path and the associated hardware settings required for a particular imaging condition, allowing the user to switch reproducibly between different observation modes.

Depending on the microscope and the installed hardware, an optical configuration may include:
- **Illumination mode** : transmitted light, fluorescence, DIC, or other available techniques.
- **Optical path selection** : excitation and emission filters, dichroic mirrors, shutters, and light-path routing.
- **Optical components** : selected objective, magnification, or other motorized optical elements.
- **Acquisition settings** : camera port or detector path and other hardware parameters associated with the selected imaging mode.

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
![[OC - creation - annotated_numbered.png|500]]

This window is very important to make sure the OC behave the way you want it. 
It basically gives the choice to set what part of microscope should move when you click on it and/or how the resulting image should look like.
Here are some descriptions of this window :
1. Name of the OC : gives the name of the OC itself
2. Camera Settings : If clicked the OC will remember the settings of the camera, such as the binning or the readout mode. If the "Use Stored ROI" box is ticked, the OC will also remember the crop of the camera (if you want to force it)
3. Channel Setup : If clicked the OC will integrate channel information, it will recall a channel name (see below in 4.) and an associated false color (see in 5.)
4. Name of the channel: gives the name of the channel that will be recorded in the metadata and displayed in the acquired image
![[NIS_image_window_annotated_zoomed.png]]
5. Channel false color : the channel will be linked to a false color. The false color can be set "Automatically" (NIS will use the color associated with the used emission filter) or "Manually"
6. Microscope setting : If clicked NIS will remember to set the designated microscope component (in 7.) in a specific postions

## Assign Parameters when OC changes
If while using an OC a parameter is changed (filter, light source used,...) NIS will detect that something is different and a "❗" will appear next to the name of the OC.
### looking for differences
If faced with a "❗" not knowing its origin, it is possible to right-click on the OC and go to "Show differences". NIS will show when changed from the registered.
### assigning the changes
If what caused the "❗" is the desired effect, then you can update the OC by as well right-click on it and go to "Assign microscope settings" or "Assign camera settings" depending on which setting has been changed.

## recommanded settings when creating an OC
Here are some recommended parameters to set when creating new OCs to make NIS use smoother :

<img src="OC - annotated.png" width="500">

1. uncheck light source « xxx Power » used devices → it applies to every light sources linked to the OCs : Lasers, AOTF, LEDs (transmission and EPI)
2. Set an Active Shutter (Shutter that switches ON during acquisition and OFF when not acquiring) for the OC → should the main shutter for the light source -> it will minimize the chances to bleach the sample when not in "Live"
>[!warning] make sure that the chosen Active Shutter is not a mechanical one
3. uncheck "Objective" -> Minimize the risks of "accidents" with immersion.

### also
- Always check the box for camera settings, this is often needed for use in ND Acquisition
- The channel name can be different from the OC name, and should only refer to the colour / wavelength of the emission light
## extra parameters to take into account with OCs
Global OC settings exist when it comes to automatically save values.

As they are global (will apply to all **OCs**) they are found in the « Options » window (found in the menu Edit > Options), in the « General » section.

<img src="Option-general - annotated.png" width="400">

The most important to know are the « Save changes to optical configuration automatically ».

For the following parameters, changes done by the user will not generate an «❗» in the OCs button as this setting(s) will be automatically saved.
- **Exposure Only** -> only the exposure time will be saved (not the camera settings : speed, bit depth…)
>[!note] This is the default setting
- **All Camera Settings** -> all changes done in the camera tab will be saved (exposure + speed + bit depth…)
- **All Brightness Settings** -> all the camera settings **AND** the other settings such as light source chosen and their power, filter cubes…
