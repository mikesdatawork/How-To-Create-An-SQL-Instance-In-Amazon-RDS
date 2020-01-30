![MIKES DATA WORK GIT REPO](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_01.png "Mikes Data Work")        

# How To Create An SQL Instance In Amazon RDS
**Post Date: May 4, 2015**        



## Contents    
- [About Process](##About-Process)  
- [SQL Logic](#SQL-Logic)  
- [Build Info](#Build-Info)  
- [Author](#Author)  
- [License](#License)       

## About-Process

<p>How to create an SQL Server Database Instance in Amazon RDS.
Login to AWS: Amazon Web Services</p>

1.
Supply your Amazon AWS Account name, Username, and Password, and click 'Sign in'.

![Sign In To AWS]( https://mikesdatawork.files.wordpress.com/2015/05/image0011.jpg "Sign In To Amazan AWS")
 
2.
Select 'RDS'.

![Select Amazon RDS]( https://mikesdatawork.files.wordpress.com/2015/05/image002.jpg "Select Amazon RDS")
 
3.
Select 'Instances'.

![Select RDS Instances]( https://mikesdatawork.files.wordpress.com/2015/05/image003.jpg "Select RDS Instances")
 
4.
Select 'Launch DB Instance'.

![Select Launch DB Instance]( https://mikesdatawork.files.wordpress.com/2015/05/image004.jpg "Select Launch DB Instance")
 
5.
Complete the following actions:
a. Select 'SQL Server'.
b. Click the 'Enterprise Edition' option ( sqlserver-ee ).

![Select SQL Engine]( https://mikesdatawork.files.wordpress.com/2015/05/image005.jpg "Select SQL Engine")
 
6.
For the Dev-Cloud environment select the following options.
a. DB Engine: sqlserver-ee
b. License Model: bring-your-own-license
c. DB Engine Version: 11.00.2100.60.v1 (RTM)
Note: This is pre SP1, SP2, so updates will need to be applied following creation.
d. DB Instance Class: db.m3.medium – 1 vCpu, 3.75
e. Multi-AZ Deployment:
f. Storage Type: General Purpose SSD
There are 3 types of Storage, but 'General Purpose SSD' should be sufficient for most standard workloads.
![Select Amazon RDS General Purpose SSD Storage]( https://mikesdatawork.files.wordpress.com/2015/05/image006.png "Select General Purpose For Amazon Allocated Storage")
 
1. General Purpose (SSD): Suitable for a broad range of database workloads. Provides baseline of 3 IOPS/GB and the ability to burst to 3,000 IOPS.
2. Provisioned IOPS (SSD): Suitable for I/O-Intensive database workloads. Provides flexibility to provision I/O ranging form 1,000 to 30,000 IOPS.
3. Magnetic Storage: Used for small database workloads where data is accessed less frequently.
Note:
Make sure to select the Storage type that best fits your database environment. The storage type CANNOT be changed once the instance is created. 'Scaling Storage' is not supported for SQL Server in Amazon RDS.
g. Allocated Storage*:
Note1:
If you are selecting storage greator than 20 GB, this will disqualify the instance from being supported on the 'free tier'.
Note2:
If you select a medium storage type; you must select a VPC on the following Step3 Configure Advanced Settings. Storage is dependent on the VPC.

![Select Amazon Not In VPC Storage Type]( https://mikesdatawork.files.wordpress.com/2015/05/image008.jpg "Select Amazon Not In VPC Storage")
 
h. DB Instance Identifier: MyInstanceName
Note: Instance Name must be under 15 characters.
i. Master Username: MySaUserName
Note: This represents the 'sa' account in SQL Server.
j. Master Password: MyNewPassword
k. Confirm Password: MyNewPassword
Click 'Next Step' after the correct selections have been made.

![Specify Database Details In Amazon RDS]( https://mikesdatawork.files.wordpress.com/2015/05/image009.jpg "Specify Database Details In Amazon RDS")
 
7.
Click 'Launch DB Instance'.

![Configure Advanced Settings In Amazon RDS]( https://mikesdatawork.files.wordpress.com/2015/05/image010.jpg "Configure Advanced Settings In Amazon RDS")
 
8.
The Wizard will proceed to create the instance at this point. No more selections need to be made.

![Launching]( https://mikesdatawork.files.wordpress.com/2015/05/image011.jpg "Launching")
 


[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

[![Gist](https://img.shields.io/badge/Gist-MikesDataWork-<COLOR>.svg)](https://gist.github.com/mikesdatawork)
[![Twitter](https://img.shields.io/badge/Twitter-MikesDataWork-<COLOR>.svg)](https://twitter.com/mikesdatawork)
[![Wordpress](https://img.shields.io/badge/Wordpress-MikesDataWork-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

    
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Mikes Data Work](https://raw.githubusercontent.com/mikesdatawork/images/master/git_mikes_data_work_banner_02.png "Mikes Data Work")

