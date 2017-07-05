================================================================================================================================
C#
================================================================================================================================

Creating services by Command promt
================================================================================================================================

1) Create: SC CREATE shortservicename binPath= "c:\nitin.sharma\job.exe" DisplayName= "ServicesName" start= auto
2) STOP: SC STOP shortservicename
3) DELETE: SC DELETE shortservicename

Note: You need to run the command prompt as an administrator
================================================================================================================================



================================================================================================================================
SQL
================================================================================================================================

#TempDB
================================================================================================================================
SQL db had following databases by default.
	1) Master
	2) model. ...
	3) msdb. ...
	4) Resource database. ...
	5) tempdb. ...
	
TempDB:
	Many operation of SQL is handeled by TempDB 
	Example: Cursor, Temp tables, Temp variable, connection Object, version control.
	TempDB uses data files to do any work. 
	As microsoft suggested you should have 1 data file per CPU or you can have 1 data file per 2/3 CPU. But in this case SQL server performence may go on toss.
	So you should keep 1/CPU or keep 2/CPU and monitor for performance.
	
	Data files writting work is done using HandClock algorithm, It check data file size and availablity. 
	and choose the file to update. It always try to keep every file as same in size.
	If it is grown it will increase the size of file if setting in SYS table is ON.
	
	
	FORMULA to calculate Data files and log files
	


================================================================================================================================