# Overview

The VIBE desktop is an interactive application running in your web browser. In simple terms, it works by connecting the VIBE desktop (or any other application) to the UBELIX HPC cluster via slurm scheduled jobs.

This guide you will walk you through the first steps for setting up your system configuration and launching the VIBE desktop.

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

## What do you need?

To use the VIBE desktop you are required to:

- **Be connected on the campus network**. You must be connected to the university network via EduRoam or use the forticlient VPN to connect remotely. Instructions on how to setup your VPN client can be found in the IT services on [Internet and Uninetwork documentation.](https://www.unibe.ch/universitaet/campus__und__infrastruktur/rund_um_computer/internetzugang/index_ger.html)
- **An active UBELIX account**. You need an UBELIX account to be able to access the VIBE desktop. Please follow the steps described in the UBELIX documentation on [How to Access UBELIX](ubelix-doc-access-ubelix).
- **A VIBE project Account**. To get full access to the computational resources offered by VIBE desktop you will need to have a VIBE project account. Get in touch with us or read more about our current [pricing model](). You could still access the VIBE desktop with a free account for limited access according to the [current UBELIX usage model](https://hpc-unibe-ch.github.io/costs/overview/).


## Defining your system configuration
- Visit the UBELIX OpenOndemand website: [https://ondemand.hpc.unibe.ch](https://ondemand.hpc.unibe.ch) and click on **"My interactive section"** on the navigation bar. You will see at the left side the interactive apps available for you such as VS Code server, Jupyter Notebook, etc and also the VIBE desktop. Select the VIBE desktop.
- You will see the form to define your system configuration. Here the sections explained:

    * **Time limit in hours**: define the time of your session.

    * ~~**Desktop Environment**~~: remove when solved issue [#16](https://github.com/dsl-unibe-ch/vibe-desktop-dev/issues/16) in vibe-desktop-dev.

    * **Account**: 
        - gratis: Use this option if you want to use VIBE desktop for testing only with limited resources for test only or beta testing.
        - paygo: You need to belong to a project to use this option. Read more on the [Pay-as-you-go (PAYG) Scheme](https://hpc-unibe-ch.github.io/costs/payg/) from UBELIX.
        - teaching: Use this option if you plan to use the VIBE desktop in a workshop or other teaching activities.

    * **Partition**: Currently you can run ondemand apps on GPU nodes only. The partition available are:
        - gpu
        - gpu-invest

        Additional information on the different partitions and their use are available in the [UBELIX documentation on Partition](https://hpc-unibe-ch.github.io/runjobs/partitions/#partitions)

    * **QoS**: the following QoS availables are:
        - job_cpu_premptable
        - job_debug
        - job_gpu_preemptable
        - job_gratis

        Additional information on the different QoS and their use are available in the [UBELIX documentation on QoS](https://hpc-unibe-ch.github.io/runjobs/partitions/#qos)

    * **GPU type**: the list of GPUs available in the VIBE.
        - RTX 3090
        - RTX 4090
        - A100
        - H100
        - H200
    * **Instance size**: This define the amount of resources in terms of CPU (number of cores) and RAM for your session. There exist three default configurations: 
        - Small: 4 cores, 8GB RAM
        - Medium: 32 cores, 32GB RAM
        - Large:16 cores, 64GB RAM
        - Custom

        However, you can also create an instance with custom configuration of hardware for your application. Read more on what type of configurations are allowed in the [UBELIX documentation on resources selection](https://hpc-unibe-ch.github.io/hardware/gpu/#cpu-memory).

    * **Number of Nodes**: In case you need more than one node for your computation.

    * **Email on start**: May your session be in the queue for a period of time and be notified when start. Introduce in this filed a valid email address and you will receive a notification when your session is being initialized.

## Launching the desktop

Once you have define the resources and time for your VIBE desktop, click on the button Launch. The desktop may take few minutes to launch depending on the current usage. Adjust the compression and image quality and click on the button "Launch VIBE desktop". A new window in your browser will be open displaying the VIBE desktop.

!!! note 
    Show the "launch the VIBE desktop" form.


## Interact with VIBE

VIBE behave as an usual desktop in a linux environment. You can browse files, open files and navigate the internet. However, the power of VIBE relies in its dedicated applications for Bioimage analysis already preinstalled and ready to use. In addition, VIBE has an integrated terminal emulator where more advanced users can script and run commands via the command line.

!!! note 
    show  screenshot showing the VIBE desktop menu, etc

VIBE, as a service attached to the UBELIX cluster, is connected directly to the Research storage. You can explore your research storage folder and open dataset from there.

Let's open an example image and visualize it in napari for instance.



## Closing your session

There exist few ways to close your VIBE session.
1. Via the **VIBE graphical user interface**. Go to the menu bar and click on Applications -> Log out. A new window will appears prompting you to leave log out. click "Log Out". Leave the "Save session fo future logins" if you want to reopen the last applications used in your next session. 
2. Via **"My Interactive sessions"** in OpenOndemand: Go to "My interactive Sessions" in the main tab of OpenOndemand and just click on the red delete button that monitors your live session. 
3. Via the **Jobs manager tool** in OpenOndemand: Go to Jobs on the main window and click on "Active Jobs". There you will see all the job you are currently running. Identify the job that runs the VIBE desktop either by the name <vibe-desktop-dev> or by the job ID. To stop your job click on the red trash can button located at the right end of the entry under the "Actions" column 


## Full video
The full video tutorial can be visualized here:

<video controls loop muted autoplay>
 <source src="../assets/videos/VIBE_quick_start_user_form_2x.mp4" type="video/mp4">
</video>