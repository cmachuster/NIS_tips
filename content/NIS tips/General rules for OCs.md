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
