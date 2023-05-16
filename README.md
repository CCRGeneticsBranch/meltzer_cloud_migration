# meltzer_cloud_migration


From: Kadalli, Shiv (NIH/NCI) [C] <shiv.kadalli@nih.gov>
Date: Wednesday, May 10, 2023 at 3:26 PM
To: Zhu, Jack (NIH/NCI) [E] <zhujack@mail.nih.gov>, Seshadri, Krish (NIH/NCI) [E] <krish.seshadri@nih.gov>, Shaikh, Sajid (NIH/NCI) [C] <sajid.shaikh@nih.gov>, Salih, Karwan (NIH/NCI) [C] <karwan.salih@nih.gov>, Vanam, Giri (NIH/NCI) [C] <venkatavarahalagiri.vanam@nih.gov>, Meltzer, Paul (NIH/NCI) [E] <pmeltzer@mail.nih.gov>, Desai, Avni (NIH/NCI) [C] <avni.desai@nih.gov>
Cc: Zhao, Patrick (NIH/NCI) [C] <patrick.zhao@nih.gov>, Osman, Waleed (NIH/NCI) [C] <waleed.osman@nih.gov>, Shaikh, Sajid <sajidshaikh@deloitte.com>
Subject: Review Cloud Architecture with Dr Zhu - (Dr Meltzers Lab)
Hi all,
 
Thanks for attending the call. Following are the notes from our discussion today. Please add any other important considerations that I have missed.
 
1)	Concern about data transfer between on-prem and cloud server
2)	Address performance issues with s3 and EFS volume ( synching data between on-prem and cloud storage will be helpful)
3)	How do we address the old applications that are built 6 years ago that need to be re-deployed on a new VM? Is containerization a solution?
4)	CBIIT supports containerization but will have to check how the container will be created using old OS or new OS? Needs separate discussion.
5)	How to address scaling on processing server? How to process using multiple nodes? Current architecture assumes one single large node but if we must take advantage of cloud, we can think of multiple options. Needs separate discussion.
6)	Krish will discuss funding part with Dr Paul and Jason
7)	Everyone agreed to test on non-prod and find out what works and what doesn’t.
 
Next Steps
 
1)	Set up Non-Prod Account
2)	Instantiate Dev Processing server( Centos 7 or OEL8)
3)	Test mounting of NFS storage on the box and record performance
4)	Set up processing software on Ec2 and test processing performance using S3/ EFS volume and NFS mount.
5)	Set up separate deep dive discussions to understand the application deployments and Ec2 scaling.
![image](https://github.com/CCRGeneticsBranch/meltzer_cloud_migration/assets/129963942/5184c414-6c4b-4963-b511-16a6175a81d0)
