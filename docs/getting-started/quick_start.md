# Overview

The VIBE desktop is an interactive application running in your web browser using the OpenOndemand abstraction layer. In simple terms, it works by connecting the VIBE desktop (or any other application) to the UBELIX HPC cluster via slurm scheduled jobs.

This guide will walk you through the first steps to use VIBE desktop.

!!! warning 
    The following description is base on the form currently in use. The content here may change as the form evolves..

Outline:

- [x] Description of the VIBE open ondemand app.
- [x] Requirements
- [x] Defining your system configuration
    - [x] describe the form and its parameters
- [x] launching the desktop
- [x] interacting with the VIBE desktop, check properties, menu, navigate the file system, look up at the research storage, open an image
- [x] launching an application
- [x] Closing your session
    - [x] Note on persistent session

## What do you need?

To use the VIBE desktop you are required to:

- **Be connected to the campus network**. You must be connected to the university network via EduRoam or use the forticlient VPN to connect remotely. Instructions on how to setup your VPN client can be found in the IT services on [Internet and Uninetwork documentation.](https://www.unibe.ch/universitaet/campus__und__infrastruktur/rund_um_computer/internetzugang/index_ger.html)
- **An active UBELIX account**. You need an UBELIX account to be able to access the VIBE desktop. Please follow the steps described in the UBELIX documentation on [How to Access UBELIX](ubelix-doc-access-ubelix).
- **A VIBE project Account**. To get full access to the computational resources offered by VIBE desktop you will need to have a VIBE project account. Get in touch with us or read more about our current [pricing model](). You could still access the VIBE desktop with a free account for limited access according to the [current UBELIX usage model](https://hpc-unibe-ch.github.io/costs/overview/).


## Defining your system configuration

- Firstly, Go to the UBELIX OpenOndemand website: [https://ondemand.hpc.unibe.ch](https://ondemand.hpc.unibe.ch) and click on **"My interactive section"** on the navigation bar. You will see at the left side the interactive apps available for you such as VS Code server, Jupyter Notebook, etc and also the VIBE desktop. Select the VIBE desktop. You will land now on the VIBE system configuration form. To know more about the different configuration visit the [VIBE system configuration form](vibe_configuration_form.md) documentation.

- On the VIBE system configuration form select: 
    - **Time limit**: 3 hour
    - **Accounts**: gratis
    - **Partition**: gpu-invest
    - **QoS**: job_gpu_preemptable
    - **GPU type**: RTX 4090 
    - **Number of GPUs**: 1
    - **Instance size**: Large
    - Optionally: click email on start and type your email address.



!!! note 
    Show the "launch the VIBE desktop" form screenshot.

![vibe_configuration_form](../assets/images/VIBE_submission_form_quick_start.png)

- Click on "**Launch**" blue button and wait for your session to start. This may take few minutes.

## Interact with VIBE

VIBE behave as an usual desktop in a linux environment. You can browse files, open files and navigate the internet. However, the power of VIBE relies in its dedicated applications for Bioimage analysis already preinstalled and ready to use. In addition, VIBE has an integrated terminal emulator where more advanced users can run commands or scripts via the command line.

!!! note 
    show  screenshot showing the VIBE desktop menu, etc

VIBE, as a service attached to the UBELIX cluster, is connected directly to the Research storage. You can explore your research storage folder and open dataset from there.

Let's open an example image and visualize it in napari for instance.



## Closing your session

There exist few ways to close your VIBE session.

1. Using the **VIBE graphical user interface**. Go to the menu bar and click on Applications -> Log out. A new window will appears prompting you to confirm to log out. Click "Log Out". Leave the "Save session fo future logins" selected if you want to reopen the last applications used in your next session. 
2. Via **"My Interactive sessions"** in OpenOndemand. Go to "My interactive Sessions" in the main tab of OpenOndemand and just click on the red delete button that monitors your live session. 
3. Via the **Jobs manager tool** in OpenOndemand. Go to Jobs on the main window and click on "Active Jobs". There you will see all the job you are currently running. Identify the job that runs the VIBE desktop either by the name <vibe-desktop-dev> or by the job ID. To stop your job click on the red trash can button located at the right end of the entry under the "Actions" column.

!!! Warning
    Note that by simply closing the browser window where you have your VIBE instance running will not stop your current session and may incur in unexpected or unintentional billing cost. Make sure you terminate your session using the instructions.
!!! Note
    Your session is persistent after closed, that is, all data that you save on your environment such as files, models, images, etc will be preserved for the next session.


## Full video
The full video tutorial can be visualized here:

<video controls loop muted autoplay>
 <source src="../assets/videos/VIBE_quick_start_user_form_2x.mp4" type="video/mp4">
</video>