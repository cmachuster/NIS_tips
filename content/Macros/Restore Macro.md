
## Context
This Macro is design to reload silently (without questions from NIS) backup files of the stored Layouts and Optical Configurations (see [[How to backup Layouts and OCs]]).
It is often used at NIS startup or shutdown via the [[Run Macro on Events]] option

## Code
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

## explanation of the commands

### RestoreLayouts and RestoreOptConf

RestoreLayoutsEx and RestoreOptConfEx will reload the `.xml` files containing the backups of respectively the Layouts and the Optical configurations.

The "Ex" versions of this command unlock argument choices that can be useful, such as the "1" argument that bypass the confirmation prompt when reloading backup files.

Below are the explanation of the arguments
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
### Emptying the "ND Acquisition" tabs
The commands :
```c
ND_ResetMultipointExp;
ND_ResetTimeExp;
ND_ResetZSeriesExp;
ND_ResetLambdaExp;
```
Will respectively reset the XY, Time, Z and Lambda tabs of the "ND Acquisition" panel.
If this behavior is not required this lines can be deleted or commented out by adding `//` at the beginning of each lines as such:
```c
//ND_ResetMultipointExp;
//ND_ResetTimeExp;
//ND_ResetZSeriesExp;
//ND_ResetLambdaExp;
```