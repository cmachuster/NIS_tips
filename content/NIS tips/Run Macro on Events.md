Function to be fund in the Menu Macro > Run Macro on Events…

The window that opens give the choice to launch Macro or commands during or before/after different events such as :
- when opening images
- before/after capturing an image
- when starting/closing NIS
- at the start/finish of a ND experiment run
- when clicking the Capture Button

>[!info] 
>- A command is a line of text that activate a function (ex: starting live)
>- A Macro is a file with the `.mac` extension containing one or multiple commands and can be coded

The most commonly used function is the one launching a Macro/commands during when NIS starts or stops. It is often used to load default layouts and/OCs

<img src="Macro-on-event-3.png" width="400">


Next to one of this event you can click the 🔽 where you can choose to run a Macro (that has to be saved somewhere on the hard drive) or a command (from the Command List window)

You can as well directly type (or copy/paste) multiple commands

ex : `RestoreOptConfEx(« C:\Nikon Service\xxx », 1); RestoreLayoutsEx(« C:\Nikon Service\xxx », 1);`

<img src="Macro-on-event-4.png" width="400">

This two commands will loads the .xmlfiles for the layouts and OCs overwriting the actual ones without asking any questions (because of the 1argument at the end)

#### explaination of the commands
##### `RestoreLayoutsEx(« C:\Nikon Service\xxx », 1);`
>[!quote] details on the option (last value)
>- 0 - Opens a dialog window and asks the user what to do
>- 1 - Overwrites the old layout with the new one
>- 2 - Does not import the new layout
>- 3 - Imports the new layout and renames it automatically (appends an index numbers)

##### `RestoreOptConfEx(« C:\Nikon Service\xxx », 1);`
>[!quote] details on the option (last value)
>- 0 - Opens a dialog window and asks the user what to do
>- 1 - Overwrites the old layout with the new one
>- 2 - Does not import the new configuration
>- 3 - Imports the new configuration and renames it automatically (appends an index numbers)
>- 4 - Deletes the current configuration and then loads the new configuration

