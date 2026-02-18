# Overview

The VIBE desktop is an interactive application that runs directly in your web browser using the OpenOnDemand interface, which connects you to the UBELIX HPC cluster via SLURM-scheduled jobs. In simple terms, VIBE allows you to access a high-performance computing environment for bio-image analysis and other tasks, without needing to install software locally.

This guide will walk you through the initial setup and usage of the VIBE desktop.

!!! warning
    The following description is based on the current version of the form. Please note that the content may change as the form evolves.

## What You Need

To use the VIBE desktop you will need:

* **Access to the campus network**: You need to be connected to the university network either through EduRoam or using the FortiClient VPN to connect remotely. Find instructions for setting up the VPN client in the IT Services [Internet and Network Access documentation](https://www.unibe.ch/universitaet/campus__und__infrastruktur/rund_um_computer/internetzugang/index_ger.html).

* **An active UBELIX account**: You must have an active UBELIX account to access the VIBE desktop. Follow the steps outlined in the UBELIX documentation on [how to access UBELIX](https://hpc-unibe-ch.github.io/firststeps/accessUBELIX/).

* **A VIBE project account**: To access the full computational resources of the VIBE desktop, you need a VIBE project account. [Get in touch](../contact.md) for additional details and costs of the service. You can still access VIBE with a free account, but your resources will be limited and subject to queue times if resources are not available.

## Defining Your System Configuration

1. **Access the UBELIX OpenOnDemand portal**: Go to [https://ondemand.hpc.unibe.ch](https://ondemand.hpc.unibe.ch). In the navigation bar, click on **"My Interactive Sessions"**. You will see a list of available interactive applications such as VS Code server, Jupyter Notebook, and, of course, VIBE Desktop. Select **VIBE Desktop** to proceed.

2. **VIBE system configuration form**: Once you select VIBE, you will be redirected to the system configuration form. This is where you will define the parameters for your session. For more details on the configuration options, see the [VIBE system configuration form documentation](../in-depth-explanations/vibe_configuration_form.md). Fill out the system configuration form:

    - **Time limit**: 3 hour
    - **Accounts**: gratis
    - **Partition**: gpu-invest
    - **QoS**: job_gpu_preemptable
    - **GPU type**: RTX 4090 
    - **Number of GPUs**: 1
    - **Instance size**: Large

![vibe\_configuration\_form](../assets/images/VIBE_submission_form_quick_start.png)

3. **Launch the desktop**: Once you've configured your session, click on the blue **"Launch"** button. It may take a few minutes for your session to start. Please be patient while the system prepares your environment.

## Interacting with the VIBE Desktop

The VIBE desktop operates like a typical Linux desktop, providing a familiar graphical user interface (GUI) for browsing files, launching applications, and even navigating the internet. However, its real power lies in the pre-installed bio-image analysis tools that are ready to use.

Additionally, VIBE includes an integrated terminal emulator, which allows more advanced users to run custom commands or scripts directly from the command line.

!!! note "Note for me"
    *Consider showing a screenshot of the VIBE desktop menu here, highlighting key areas such as the applications in the menu, file manager, etc.*

Since VIBE is connected directly to the UBELIX cluster, you have seamless access to research storage. You can easily browse your research files and open datasets directly within the desktop environment.

You can for instance, open a sample image from the research storage and visualize it using **Napari**, a popular tool for bio-image analysis.

!!! note "Note for me"
    *add screenshot of an open image using napari*

## Closing Your Session

There are several ways to close your VIBE session:

1. **Using the VIBE graphical user interface**:

   * In the menu bar, click on **Applications → Log Out**. A confirmation window will appear asking if you want to log out. Click **Log Out**. Leave the "Save session for future logins" option selected if you want to restore the same applications when you log in next time.

2. **Via the OpenOnDemand "My Interactive Sessions" panel**:

   * In OpenOnDemand, go to **"My Interactive Sessions"** and click the red **Delete** button next to your active session.

3. **Via the Jobs Manager tool in OpenOnDemand**:

   * In the OpenOnDemand dashboard, click on **Jobs** in the main window and then go to **Active Jobs**. Find the job running the VIBE desktop by its name `<vibe-desktop-dev>` or job ID. To terminate the session, click the red trash can icon under the "Actions" column.

!!! warning
    **Important**: Simply closing your browser window without properly terminating your session may result in unintended billing charges. Always follow the termination steps outlined above.

!!! note 
    **Persistent Session**: Your session is persistent after closing. This means any files, models, images, or other data saved during your session will be preserved for the next time you log in.

## Full Video Tutorial

For a detailed walkthrough of the VIBE desktop setup and usage, you can watch the full tutorial video here:

!!! note "Note for me"
    replace this outdated video so it matches the last changes in this form.
<video controls loop muted autoplay>
    <source src="../assets/videos/VIBE_quick_start_user_form_2x.mp4" type="video/mp4">
</video>