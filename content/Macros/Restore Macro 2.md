
> [!INOTE]
> This Macro is design to reload silently (without questions from NIS) backup files of the stored Layouts and Optical Configurations

```c
// Restore Layout
RestoreLayoutsEx(« C:\Nikon Service\xxx », 1);
// Restore Optical configuration
RestoreOptConfEx(« C:\Nikon Service\xxx », 1);

// empty tabs of ND Acquisition (everyting but the Large Image tab)
ND_ResetMultipointExp;
ND_ResetTimeExp;
ND_ResetZSeriesExp;
ND_ResetLambdaExp;
```

> [!IMPORTANT] 
> .mac file can be downloaded [here](https://github.com/cmachuster/NIS/blob/main/attachments/Restore_Macro.mac) 
