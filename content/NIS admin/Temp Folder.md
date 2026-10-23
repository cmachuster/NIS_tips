
>[!note]
By default the temp folder get installed on the C drive. 
When NIS is dealing with a lot of data it will store them in the temporary folder. Sometimes the folder doesn't get emptied correctly (after crashes) or NIS is manipulating huge files. In this cases the C drive might get to filled slowing down the workstation

The address of the temporary folder can be found in NIS in Edit > Options...

![[Option-general.png]]

To avoid to slow the workstation make sure that the temp folder, is located on one of the SSD drive of the workstation for fast storage by clicking the ==…== box , like the `D:\FastSSD`

>[!Note] N.B. 
>If NIS seems slow handling operations have a look at the size of the temp folder and delete its content if needed.

>[!info] Macro command 
>To change the location of the temp folder a macro command can be used 
>```c
>// Move the temp folder automatically to D:\temp\
>SetTempFilesPathForNextSession("D:\temp\");
>```

