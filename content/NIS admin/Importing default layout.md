
A macro has been developped to speed up the setup of NIS after the installation.

A folder « NIS_install » is available on the common « SAS Service Training » folder and has to be copy/pasted to the « Nikon Service » folder.

>[!danger] the « Nikon Service » spelling is important

<img src="Install macro.png" width="300">

The « NIS_install » folder contains :
-  a default layout that will be loaded when the macro will be launched
- a macro that will install the layout and set different NIS settings
- a readme.txtfile explaining the launch of the macro

## launching the Macro

in NIS go to Macro > Run Macro From Files... and open the file `C:\Nikon Service\NIS_install\Layout configuration.mac`

Here is the macro in details :
```c
////////NIS Windows Management

//Force the Live image to Fit the screen, not being in 1:1 per default
SetMultiWindowLiveZoom100(0);
//Make that the image frame deosn't change size when zooming
KeepPicWndAspect(0);
//Layout installation
RestoreLayoutsEx("C:\Nikon Service\NIS_install\default_layout.xml", 1);
//Move the temp folder automatically to D:\temp\

_SetTempFilesPathForNextSession("D:\temp\");

//Change the rescaling method to spline
SetRescalingMethod(2);
//Uncheck parallel device movement for JOBs
Jobs_SetParallelDeviceMovement(0);
```
### what it does

1.    it makes sure that the image is displayed with a 100% zoom when the acquisition is launched
2.    makes that the image window size doesn’t change when zooming in/out
3.    load the default_layout.xmlfile
4.    move the temp folder to the D drive
5.    adjust the image rescaling to Spline
6.    de-activate the parallel device movement in JOBS (not critical but convenient to do)

>[!important] It is always possible to comment out commands in this macro.
>For example, you can remove (by deleting the line) the command for moving the temp folder or add "//" in front of it to "deactivate" it



