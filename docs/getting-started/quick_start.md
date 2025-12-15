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
- [ ] launching the desktop
- [ ] interacting with the VIBE desktop, check properties, menu, navigate the file system, look up at the research storage
- [ ] launching an application
- [ ] Opening an image
- [ ] Closing your session

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
    * **Instance size**: This define the amount of resources in terms of CPU (number of cores) and RAM for your session. There exist default configurations. However you can also create an instance with custom configuration if you need a different configuration of hardware for your application. Make sure you don not exceed the maximum hardware configuration define by UBElIX. Read more on what type of configurations are allowed in the [UBELIX documentation on resources selection](https://hpc-unibe-ch.github.io/hardware/gpu/#cpu-memory)
        - Small: 4 cores, 8GB RAM
        - Medium: 32 cores, 32GB RAM
        - Large:16 cores, 64GB RAM
        - Custom
    * **Number of Nodes**: In case you need more than one node for your computation.

    * **Email on start**: May your session be in the queue for a period of time and you would like to be notified when start. YOu amy introduce in this filed a valid email address to receive notification when your session has being launched.





## Full video
The full video tutorial can be visualized here:

<video controls loop muted autoplay>
 <source src="../assets/videos/VIBE_quick_start_user_form_2x.mp4" type="video/mp4">
</video>