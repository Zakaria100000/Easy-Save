# Introduction to Easy-Save

Easysave is a back up folder software. It's a school project created by a team of 4 students.

Context
Our team has just integrated the software publisher ProSoft.   Under the responsibility of the CIO, we are in charge of managing the "EasySave" project which consists in developing a backup software.  As any software of the ProSoft Suite, the software will be integrated into the pricing policy.

Unit price : 200 €HT
Annual maintenance contract 5/7 8-17h (updates included): 12% purchase price (Annual contract tacitly renewed with revaluation based on the SYNTEC index) During this project, we will have to ensure the development, the management of major and minor versions, but also the documentation (user and customer support).  To ensure that our work can be taken over by other teams, we must work within certain constraints such as the tools used. 
Built with
Visual Studio 2019 (enterprise version)
Visual Pardigm (for diagram)
Azure Repos
Version 1.0
The specifications of the first version of the software are as follows : 

The software is a Console application using .Net Core. It must allow the creation of up to 5 backup jobs.

A backup job is defined by :

An appellation
A source directory
A target directory
One type
Full
Differential
the software have to be understandable by english person
The user may request the execution of one of the backup jobs or the sequential execution of the jobs. The directories (sources and targets) can be on local, external or network drives. All the elements of the source directory are concerned by the backup.

Daily Log File :

The software must write in real time in a daily log file the history of the actions of the backup jobs. The minimum expected information is :

Timestamp  
Naming the backup job
Full address of the Source file (UNC format)
Full address of the destination file (UNC format)
File Size 
File transfer time in ms (negative if error)    
Status File The software must record in real time, in a single file, the progress of the backup jobs.  The minimum expected information is :  

Timestamp  
Naming the backup job
Backup job status (e.g. Active, Not Active...) If the job is active
The total number of eligible files
The size of the files to be transferred 
The progression         
Number of remaining files  
Size of remaining files  
Full address of the Source file being backed up
Complete address of the destination file
The locations of the two files described above (daily log and status) will have to be studied to work on the clients' servers. As a result, "c:\temp" type locations are to be avoided.
The files (daily log and status) and any configuration files will be in XML or JSON format. In order to allow fast reading via Notepad, it is necessary to put line feeds between the XML (or JSON) elements. A pagination would be a plus.

Version 2.0
EasySave 1.0 has been distributed to many customers. 

Following a customer survey, the management decided to create a version 2.0 with the following improvements: 

Graphic Interface
Abandoning Console mode. The application must now be developed in WPF under .Net Core.

Unlimited number of jobs
The number of backup jobs is now unlimited. 

Encryption via CryptoSoft software
The software will have to be able to encrypt the files using CryptoSoft software (made during prosit 5). Only the files with extensions defined by the user in the general settings should be encrypted.

Evolution of the Daily Log file
The daily log file must contain additional information: Time needed to encrypt the file (in ms)  

Business software
If the presence of business software is detected, the software must prohibit the launch of a backup job. In the case of sequential jobs, the software must complete the current job and stop before launching the next job. The user will be able to define the business software in the general settings of the software. (Note: the calculator application can substitute the business software during demonstrations). #Getting Started To get a local copy up and running follow these simple example steps. But before anything else you should be sure to have Visual Studio 2019 in order to run the program.

Once you will have set up your computer You will have to clone this project.

With Git: 
https://github.com/Zakaria100000/Easy-Save.git
