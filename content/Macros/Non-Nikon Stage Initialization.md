---
tags:
  - macro
---

## Context
when using a non-Nikon motorized stage, it can be useful to perform a stage initialization.
This operation guarantees that :
- the stage motion will be as precise as possible during Large Image Acquisition
- the coordinates of the positions saved will correspond between 2 sessions

The initialization reset the 0,0 position of the stage.
## Code
```c
// Forces objective Escape
StgZ_Escape();

// Stage Initiatlization
StgInitiateXY(0,0.00000,0.00000,1,0);

// Exit from Escape
StgZ_Refocus();
```

>[!info] Use Case
> This Macro can be used as a Macro Panel button (see, [[Macro buttons]]) or at NIS startup (see, [[Run Macro on Events]])

## Download

The Macro file can be downloaded [here](attachments/mac%20files/stage_init.mac)

