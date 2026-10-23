
>[!info] NVIDIA drivers have to be downloaded and installed
>
>download link : [https://www.nvidia.com/en-us/drivers/](https://www.nvidia.com/en-us/drivers/)

Once it is done, it is important to make sure NIS can exploit the full ressource of the graphic card other.

### optimizing GPU usage for NIS

By default NIS is considered as standard software and an exception has to be made.

1. Go to « _Panneau de configuration NVIDIA_ »
<img src="NVIDIA panel.png" width="200">


2. Manage 3D settings 
<img src="NVIDIA panel - 2.png" width="400">


3. Program Settings and,

4. chick if NIS is in the "Select a program to customize" list, 
<img src="NVIDIA panel - 3.png" width="400">


5. if not add it.
	For that you need to point the `nis_ar.exe` in `C:/Program Files/NIS-Elements/`
<img src="NVIDIA panel - 4.png" width="400">


6. and finally ensure that NIS uses by default the full power of the NVIDIA graphix card
<img src="NVIDIA panel - 5.png" width="400">

