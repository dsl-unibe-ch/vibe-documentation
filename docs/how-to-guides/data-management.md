# Overview

In this section you will have an overview of how the data is located and managed in your VIBE session. As well as how you can move and transfer data from and to your VIBE desktop.

# Data organization

Since VIBE is running on the UBELIX cluster, it uses the same file system and data organization scheme as that of UBELIX. 

That includes:

 - [x] User `$HOME`.
 - [x] Workspace (research storage)
 - [x] Capacity storage
 - [x] Network scratch 
 - [x] Local scratch
    
That means that your `$HOME` directory as well as all the folders and data present in your UBELIX session will be by default available in the VIBE desktop. Similarly, the data storage quota that you currently have in your UBELIX account as well as snapshot or backup services applies for your VIBE session.
Find more information on the different data storage service options offered by UBELIX [here](https://hpc-unibe-ch.github.io/storage/).

!!! note
    We encourage researchers to use the **Research Storage Service** offered by the University, since offers centralized, cost effective, daily backup and seamlessly connectivity and data transfer for UBELIX and the VIBE environment.


May your project require special needs for data storage or you are not sure if you need extra storage for your project? [Get in touch with us](../contact.md) or  ask for a [quote](https://intern.unibe.ch/dienstleistungen/informatik/dienstleistungen_der_informatikdienste/dienstleistungen___ressourcen/research_storage/index_ger.html) on the IT services site of the University. 


# Data transfer

Data can be moved from/to your VIBE environment in a number of ways. Here we describe the recommended ways to do so.

## 1. Via UBELIX OnDemand

You can take advantage of the UBELIX OnDemand tool to transfer data.

 - Click on **"Files"** in the menu bar at the top left of the UBELIX OnDemand portal (see arrow).
 - Your sessions' `$HOME` directory will be displayed with all the content.
 - use the **"Upload"** button to load files from your host machine to any location you whish in your VIBE session.
 - use the **"Download"** button to copy files from your VIBE session to your host machine.


![](../assets/images/transfer_data_via_ood.png)


## 2. Via Command line (Advanced)

If you are comfortable using the command line, you can move data from/to your VIBE environment using tools such as `scp` and `rsync`.

Take a look at the documentation in UBELIX on how to use the command line for transferring data [here](https://hpc-unibe-ch.github.io/firststeps/movingdata/).


## 3. Connecting to a cloud service

If you have your data storage in a claud service, for instance, OneDrive, GoogleDrive, DropBox, etc, you can connect using the internet browser from VIBE and login with your credential as you normally would do from any other system.