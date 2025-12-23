# VIBE system configuration form

## Overview

The VIBE configuration form defines the features of your VIBE desktop instance in terms of resources and time. Here you will find a explanation of each the fields you can adjust to your needs.

!!! note 
    Show a screenshot of the VIBE form .

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