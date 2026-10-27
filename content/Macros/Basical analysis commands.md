---
title: Basic Image Analysis Commands
---
## Stitching a Multi-point image into a Large Image

This command exist in two version depending of the presence of the General Analysis 3 (GA3), see [[Stitching Multi-points]].
Here is the generic version of this command :
```c
ND_StitchMultipoint(0,0,0,1,1);
```

For further explanation of the arguments, please refer to this section : [[Stitching Multi-points#explanation of the command arguments|explanation of the command arguments without GA3]]

>[!info] The Macro file can be downloaded [here](attachments/mac%20files/Stitch_MultiPoints.mac)
## MaxIP

This command will generate a new ND file as the Z maximum intensity projection or MIP / MaxIP[^1].
The operation will take place even in multi-dimension files (with time and/or multi-positions)

```c
ND_CreateMaxIntProjectionImageZ()
```

>[!info] The Macro file can be downloaded [here](attachments/mac%20files/MaxIP.mac)
## Combining singles images into a Multi-point ND file
![[Merging opened documents into a multipoint ND#^d668ad]]
![[Merging opened documents into a multipoint ND#^6df04b]]

[^1]: https://en.wikipedia.org/wiki/Maximum_intensity_projection
