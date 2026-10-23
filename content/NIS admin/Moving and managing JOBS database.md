### JOBS database introduction

For NIS installation with the JOBS plugin it is worth paying attention to where the JOBS database is located.

By default all the JOBS scripts and the images acquired by them will be saved in a JOBS database folder located in `C:\ProgramData\Laboratory Imaging\Jobs\jobsdb.dat`.

<img src="JOBS_explorer-35.png" width="300">
>_Example of database containing folder with the_ _.datfile and the image/scripts containing Project folder_

<img src="JOBS_explorer-4.png" width="300">
>_Example of image containing folder named by date_time of the acquisition_ 

>[!note] JOBS database structure
>- the JOBS scripts (without images) and the database structure are contained in the `.dat` file (here `jobsdb.dat`)
>- all the images acquired through a JOBS script will be stored in the xxx Project folder (here `jobsdb` folder) and will be ordered :
>	- by project then,
>	- by JOBS script used and,
>	- by the day and time at which the JOBS script has been launched

### database manipulation

To avoid the C Drive to be quickly filled and slowing down the workstation the database has to be moved to another drive (usually the big **Data Drive**) :

1. Open the JOBS Explorer
<img src="JOBS_explorer.png" width="200">

2. in the database folder filed click the 🔽
<img src="JOBS_explorer-2.png" width="350">

3. From here you have multiple choices but the main ones are :
<img src="JOBS_explorer-3.png" width="300">

-  Create New Empty... -> it is the most convenient option at install. It will create a new empty database with no scripts and no images
- Create New Based on Current... -> will move the full database structure meaning the Projects and JOBS scripts but ==not the images==
>[!info] image folders will have to be moved manually if acqisitions already exist
- Open Existing... -> most convenient when transferring a full database (scripts and images) to another drive for example when a new PC is installed
	- copy the full folder in which the `.dat` is present, in this exemple it would be `C:\ProgramData\Laboratory Imaging\Jobs\` paste it to the new drive or new computer
	- from NIS open the `.dat` file. All the scripts and link to the images should be restored.

