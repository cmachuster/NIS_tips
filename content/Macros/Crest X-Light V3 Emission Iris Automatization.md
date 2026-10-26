
## Context
For the Spinning-disk scanner X-Light V3 from Crest it is advised to adjust the aprture of the Emission Iris (place before the camera) to the magnification and the N.A. of the objectives.

The Macro described below allow to detect the objective in imaging position and set the aperture of the emission Iris to a set value.
This Macro can be set as Macro on Event (see [[Run Macro on Events]]), usually before perform a Live acquisition.

### objectives Emission Iris chart

Here is a chart (from the X-Light V3 manual) indicating the Iris advised apeture (D), depending of the objectives N.A. and magnification.

| Magnification | N.A. | D (%) |
| ------------- | ---- | ----- |
| 4×            | 0.13 | 65    |
| 4×            | 0.2  | 100   |
| 10×           | 0.3  | 60    |
| 10×           | 0.45 | 90    |
| 20×           | 0.75 | 75    |
| 20×           | 0.8  | 80    |
| 40×           | 1.0  | 100   |
| 40×           | 1.0  | 50    |
| 60×           | 1.3  | 65    |
| 60×           | 1.4  | 47    |
| 60×           | 1.45 | 48    |
| 100×          | 1.4  | 28    |
| 100×          | 1.49 | 30    |

## Full Code
```c
char obj_code[256]; 
int position; 
 
position = Stg_GetNosepiecePosition(); 
Stg_GetNosepieceObjectiveCode(position,obj_code,256); 

if (strcmp(obj_code,"MRD70040") == 0 ) { 
   Stg_SetAperturePosition(3,100); 
}  
  
if (strcmp(obj_code,"MRD70170") == 0 ) { 
   Stg_SetAperturePosition(3,90);
}  

if (strcmp(obj_code,"MRD70270") == 0 ) {  
   Stg_SetAperturePosition(3,80); 
}

if (strcmp(obj_code,"MRD71670") == 0 ) {  
   Stg_SetAperturePosition(3,47); 
}

if (strcmp(obj_code,"MRD71970") == 0 ) {  
   Stg_SetAperturePosition(3,29); 
}

if (strcmp(obj_code,"MRD77400") == 0 ) {  
   Stg_SetAperturePosition(3,62); 
}

if (strcmp(obj_code,"MRD77410") == 0 ) {  
   Stg_SetAperturePosition(3,55); 
}  

if (strcmp(obj_code,"MRD07650") == 0 ) {  
   Stg_SetAperturePosition(3,65); 
}   

```

## Code Explanation

The code consist of the repetition of the sequence :
```c
if (strcmp(obj_code,"MRD70270") == 0 ) {  
   Stg_SetAperturePosition(3,80); 
}
```

Which says that if the objective with the reference MRD70270, here the 20x Plan Apo Lambda D, the Emission Iris must be set at 80 (`Stg_SetAperturePosition(3,80)`). 

To use this Macro, you will have to declare the objectives references and the Iris aperture values.

## Download

The Macro file can be downloaded [here](attachments/mac%20files/Auto_emission_Iris.mac)