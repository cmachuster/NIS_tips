
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

## explaination of the commands
#### `RestoreLayoutsEx(« C:\Nikon Service\xxx », 1);`
>[!quote] details on the option (last value)
>- 0 - Opens a dialog window and asks the user what to do
>- 1 - Overwrites the old layout with the new one
>- 2 - Does not import the new layout
>- 3 - Imports the new layout and renames it automatically (appends an index numbers)
### `RestoreOptConfEx(« C:\Nikon Service\xxx », 1);`
>[!quote] details on the option (last value)
>- 0 - Opens a dialog window and asks the user what to do
>- 1 - Overwrites the old layout with the new one
>- 2 - Does not import the new configuration
>- 3 - Imports the new configuration and renames it automatically (appends an index numbers)
>- 4 - Deletes the current configuration and then loads the new configuration

