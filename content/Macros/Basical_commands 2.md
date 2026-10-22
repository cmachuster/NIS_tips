
This commands and/macros can be used independently or in [macro button](https://github.com/cmachuster/NIS/blob/main/NIS_tips/Macro_buttons.md)
## close all documents

```c
CloseAllDocuments(0);
```

## Enable ROI at startup
> [!NOTE]
> commonly used to force a ROI in Ma

```c
char name[256];
GetCameraName(name,0);

if(strcmp(name,""))
{
   ROISet(512,511,1536,1533);
   ROIEnable(1);
}
```

## Getting in and out of Escape
```c
// Escape
StgZ_Escape();
// getting out of Escape
StgZ_Refocus();
```

## PSF Resetting
```c
Stg_SetPFSLensOffsetPosition(7420);
```

The value ==7420== is the middle of the offset lens range

## Stitching
```c
ND_StitchMultipoint(0,0,0,1,1);
```

## AZ100M Zoom control
```c
char buffer[100];

Set Zoom value Stg_SetZoomPosition(Int_GetValue(, Enter Zoom, 1, 1, 20));

Get Zoom value 
sprintf(buffer, Zoom %.1f, Stg_GetZoomPosition());

WaitText(0, buffer);
```