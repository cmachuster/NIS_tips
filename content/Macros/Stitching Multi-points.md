
This command exist in two "flavors" with different options depending if your NIS is able to use General Analysis 3 (GA3).
If not a general command can be used

## Stitching without GA3
```c
ND_StitchMultipoint(0,0,2,0,1);
```
### explanation of the command arguments
Arguments in order after the command `ND_StitchMultipoint(`
- **int  StitchNDMethod,**
	- 0 -> Blending - images will be blended into each other.
	- 1 -> Optimal path - the algorithm computes a path between the images where both images are least different and removes the outer areas.
- **int  StitchNDPostProcess,**
	- 0 -> No post-processing.
	- 1 -> Apply at least the shading correction.
- **int  StitchNDShadingType,**
	- 0 -> Brightfield
	- 1 -> DIC-like
	- 2 -> Fluorescence (with offset)
- **int  StitchNDShadingOffset,**
Set the offset value to be subtracted from the image before applying the fluorescence correction.
- **int  StitchNDRegistration**
	- 0 -> Image registration OFF.
	- 1 -> Image registration ON.
## Stitching with GA3
```c
ND_StitchMultipointGa3(0,1,0,0,15);
```
### explanation of the command arguments
Arguments in order after the command `ND_StitchMultipointGa3(`
- **int  iStitchingMethod,**
	- 0 -> Blending
	- 1 -> Optimal Path
- **int  iRegistration,**
	- 0 -> Off
	- 1 -> On
- **int  iAutoShadingCorrection,**
	- 0 -> Off
	- 1 -> On
- **int  iType,**
- **int  NDDimension**
	- 0 -> Current frame
	- 1 -> Time dimension
	- 2 -> Multipoint dimension
	- 4 -> Z dimension
	- 15 -> All frames (the whole ND document).
	- 16 -> Selection - the frames/dimensions selected by mouse within the ND control bar will be affected.
