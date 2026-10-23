---
title: Basic Microscope Commands
---

This commands and/macros can be used independently or as a [[Macro buttons|macro button]]
## close all opened documents

```c
CloseAllDocuments(0);
```

## Enable camera ROI

commonly used to force a camera crop ROI as [[Run Macro on Events|Macro on Event]] on NIS startup when the camera FOV is larger than the microscope

```c
char name[256];
GetCameraName(name,0);

if(strcmp(name,""))
{
   ROISet(512,511,1536,1533);
   ROIEnable(1);
}
```

>[!tip] The `ROISet`command set the size and position of the camera crop with the following arguments being (in there order in the paranthesis):
>- the x-coordinate of the top-left corner of the rectangle
>- the y-coordinate of the top-left corner of the rectangle
>- the x-coordinate of the bottom-right corner of the rectangle
>- the y-coordinate of the bottom-right corner of the rectangle

## Getting in and out of Escape

```c
// Escape
StgZ_Escape();
// getting out of Escape
StgZ_Refocus();
```

## PSF Resetting

This command is commonly used to reset the PFS to the middle of its range when it went too far

```c
Stg_SetPFSLensOffsetPosition(7420);
```

The value ==7420== is the middle of the offset lens range

## AZ100M Zoom control

```c
char buffer[100];

Set Zoom value Stg_SetZoomPosition(Int_GetValue(, Enter Zoom, 1, 1, 20));

Get Zoom value 
sprintf(buffer, Zoom %.1f, Stg_GetZoomPosition());

WaitText(0, buffer);
```