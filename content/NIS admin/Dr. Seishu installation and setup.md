![[DrSeishu.gif]]

## context

Dr. Seishu is a tool that has several functions related to support and troubleshooting of NIS-Elements and Nikon hardware. This guide explains all the different options and functions. 
>[!warning] N.B.
>Use this tool after instructed by Nikon support or service staff.

> [!NOTE]
> download link to the latest Dr. Seishu here :
> https://www.niwiki.nl/Wiki/index.cgi?topic=3293

After installation DrSeishu can be started from the start menu (Start > Nikon > DrSeishu). 
To start DrSeishu quickly in case of problems, it is best to pin it to the taskbar (right-click | More | Pin to Taskbar). 

<div style="text-align: center;">
  <img src="Seishu General.png" width="400">
</div>
>The main dialog window has buttons corresponding to 8 different functions. The main functions will be described below


## Configure Contact Information
![[Seishu Configure - contact.png|300]]
During installation you will be prompted to enter the contact information. The Nikon Support Team will use this information to reach out to you after submitting a trouble ireport. The information can be modified later by pressing the ‘Configure Contact Information’ button.
![[Seishu Configure - contact - 2.png|300]]
- **Lab Manager** : contact of the facility responsible person or Lab Manager in case the microscope belongs to a single group. 
- **Nikon Representative** : the Nikon Sales or Support Representative in your area that you are in contact with. 
- **System Type / Nickname** : The name you assigned to the system, in order to quickly identify it in case of multiple issues over time. 
- **Institute / Department, Town /City / State, Country** : The information about your institute.

## Configure Diagnostic and Log Options
![[Seishu Configure - diag.png|300]]
To investigate the origin of software and hardware malfunction, the support team needs log files. The ‘Configure Diagnostic and Log Options’ page allows configuring which log files are created. Change these option only when NIS is not running.
![[Seishu Configure - diag - 2.png|300]]

- **Run Dr Seishu on application crashes** : Checking this option will replace for Nikon software the standard WER (windows error reporting) handler by the DrSeishu Report Wizard. When NIS crashes, the Dr Seishu Report Wizard will pop up automatically and allow you to create and submit a trouble report. The report will include the NIS memory dump, which is crucial for the developers to investigate the incident. 
- **Include Services** : By default, Windows does not handle crashes of programs that are invisible. Check this option to invoke DrSeishu also upon NIS crashes when the main NIS windows is not visible. 
- **NIS General Logging** : This option corresponds to the NIS-Elements menu ‘Help | Enable Logging’. In case of problems, this option must be enabled. 
- **NIS Device Communication Logging** : This option will make that NIS records the communication with all devices to the log files. If there is an indication that communication with devices fails, this option should be enabled. 
- **NIS Qt Logging** : NIS uses the Qt library to draw the graphical user interface. If there are problems with how NIS draws the control widgets in the control panels, this option should be enabled. Note: Qt logging is very verbose and will blow up the size of the log files. Enable this option only in case of problems with the graphical user interface. 

All other logging options are dedicated to a certain device brand/model. Only check the logging options that seem to be relevant to the problems you encounter. 

Some logging activities will slow down NIS noticeably. After creating and submitting a trouble report, these logging options can be switched off to restore normal NIS performance.

## Report an Issue
![[Seishu Configure - report.png|300]]
