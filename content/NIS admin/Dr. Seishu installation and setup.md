![[DrSeishu.gif]]

## context

Dr. Seishu is a tool that has several functions related to support and troubleshooting of NIS-Elements and Nikon hardware. This guide explains most of the different options and functions. 
>[!warning] Use this tool after instructed by Nikon support or service staff.

> [!NOTE] download link to the latest Dr. Seishu here : https://www.niwiki.nl/Wiki/index.cgi?topic=3293

After installation Dr. Seishu can be started from the start menu (Start > Nikon > DrSeishu). 
![[Seishu General.png|400]]
>The main dialog window has buttons corresponding to 8 different functions. The main functions will be described below


## Configure Contact Information
![[Seishu Configure - contact.png|300]]
During installation you will be prompted to enter the contact information. 
The Nikon Support Team will use this information to reach out to you after submitting a trouble ireport. The information can be modified later by pressing the ‘Configure Contact Information’ button.
![[Seishu Configure - contact - 2.png|300]]
- **Lab Manager** : contact of the facility responsible person or Lab Manager in case the microscope belongs to a single group. 
- **Nikon Representative** : the Nikon Sales or Support Representative in your area that you are in contact with. 
- **System Type / Nickname** : The name you assigned to the system, in order to quickly identify it in case of multiple issues over time. 
- **Institute / Department, Town /City / State, Country** : The information about your institute.

## Configure Diagnostic and Log Options
![[Seishu Configure - diag.png|300]]
To investigate the origin of software and hardware malfunction, the support team needs log files. 
The ‘Configure Diagnostic and Log Options’ page allows configuring which log files are created. Change these option only when NIS is not running.
![[Seishu Configure - diag - 2.png|300]]

- **Run Dr Seishu on application crashes** : Checking this option will replace for Nikon software the standard WER (windows error reporting) handler by the Dr. Seishu Report Wizard. When NIS crashes, the Dr. Seishu Report Wizard will pop up automatically and allow you to create and submit a trouble report. The report will include the NIS memory dump, which is crucial for the developers to investigate the incident. 
- **Include Services** : By default, Windows does not handle crashes of programs that are invisible. Check this option to invoke Dr. Seishu also upon NIS crashes when the main NIS windows is not visible. 
- **NIS General Logging** : This option corresponds to the NIS-Elements menu ‘Help | Enable Logging’. In case of problems, this option must be enabled. 
- **NIS Device Communication Logging** : This option will make that NIS records the communication with all devices to the log files. If there is an indication that communication with devices fails, this option should be enabled. 
- **NIS Qt Logging** : NIS uses the Qt library to draw the graphical user interface. If there are problems with how NIS draws the control widgets in the control panels, this option should be enabled. Note: Qt logging is very verbose and will blow up the size of the log files. Enable this option only in case of problems with the graphical user interface. 

>[!warning] All other logging options are dedicated to a certain device brand/model. Only check the logging options that seem to be relevant to the problems you encounter. 

Some logging activities will slow down NIS noticeably. After creating and submitting a trouble report, these logging options can be switched off to restore normal NIS performance.

## Report an Issue
![[Seishu Configure - report.png|300]]
The report wizard allows you to enter information about an incident; collects log and configurations files that Nikon support needs to investigate the problem and finally allows you to upload the report to the NiWiKi server.
![[Seishu Configure - report - 2.png|300]]
- **Issue Summary** : a short summary of the problem (for example, camera crashed during multi point acquisition). 
- **Reported to the Lab Manager ?** : It is important to check with the lab manager if the problem has been reported before and a work-around or solution is already available. 
- **Exact Steps to reproduce the problem** : Try to describe the problem in a detailed way, defining the ongoing experiment and the user settings. If possible include the exact time on which the problem occurred, that allows the support staff to locate the relevant lines in the log files. 
- **Is the problem also happening after restarting all hardware ?** : Some issues only occur when the system was up- and-running for some time. Please try if restarting all system devices resolves the issue. 
- **Other recent unusual observations** : Fill in in case you noticed some glitches during the microscope usage prior to the issue. 
- **List of device in use** : List of all the relevant devices, such as camera, light source, modules, etc. 
- **Date and time of earlier problems** : Mention if the system suffered from this or other issues in the recent past

In the bottom part of the window, click on **Screenshot** to attach a picture of NIS elements displaying the issue (make sure NIS Elements is visible before clicking on the button, otherwise it will make a screenshot of your desktop). You can also attach to the report some files containing additional information if needed and a video in case it helps to clarify the problem.
![[Seishu Configure - report - 4.png|300]]
After filling in all fields, click the **Next** >> button.
![[Seishu Configure - report - 3.png|300]]
Verify that contact information is still correct and press **Start** to start the report creation. When the report information is collected, you will be presented with these options: 
- **Review the collected information** : to browse all information that will be included in the report. 
- **Upload the report >>**:  to upload the report to NiWiKi. 
- **Create a self-uploading report >>** : that can be moved to an online PC and will upload itself when double clicked. 
- **Create a simple report for sending by email** : to create a .zip file that must be shared manually with the Nikon Support Team. 

Dr. Seishu generates report zip files with the extension `.srtr`. 
The .srtr files can be opened using the 7-zip file manager 7zFM.exe (https://www.7-zip.org).