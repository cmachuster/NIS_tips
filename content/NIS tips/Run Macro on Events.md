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

One of the most commonly used function is the one launching a Macro/commands during when NIS starts or stops. It is often used to load default layouts and/OCs

<img src="Macro-on-event-3.png" width="400">


Next to one of this event you can click the 🔽 where you can choose to run a Macro (that has to be saved somewhere on the hard drive) or a command (from the Command List window)

You can as well directly type (or copy/paste) multiple commands

ex : `RestoreOptConfEx(« C:\Nikon Service\xxx », 1); RestoreLayoutsEx(« C:\Nikon Service\xxx », 1);`

<img src="Macro-on-event-4.png" width="400">

This two commands will loads the `.xml` files for the layouts and OCs (see [[How to backup Layouts and OCs]]) overwriting the actual ones without asking any questions (because of the 1argument at the end)

>[!note] the details of this command can be found in the [[Restore Macro]] page



