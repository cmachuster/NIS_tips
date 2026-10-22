
> [!NOTE]
>This macro will get the current X, Y, Z coordinates of the stage and create a position in the XY tab of "ND Acquisition".
>If the PFS is locked, the PFS offset will be added to the list.

### code
```c
// this macro get the X, Y, Z and PFS (if locked) coordinates and create a position in XY Tab in ND Acquisition
// this macro is usually linked to a Fn Button on the Ti2E
double x;
double y;
double z;
double pfs;

// Get Coordinates
StgGetPosXY(&x, &y);
StgGetAbsPosZ(&z);
pfs = Stg_GetPFSLensOffsetPosition();

// Create a ND "point"
ND_AppendMultipointPointPFS(x,y,z,pfs,"");
```

### use case
This macro is especially suited to one of the Ti2E function button. 
The user can then register position to NIS while looking for the sample through the eyepiece.
The most commonly used Fn button is the "FnL" button and the bottom left part of the microscope.

> [!IMPORTANT] 
> .mac file can be downloaded [here](https://github.com/cmachuster/NIS/blob/main/attachments/Add_position_2_ND.mac) 

