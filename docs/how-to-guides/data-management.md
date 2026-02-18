# Overview

This section provides an overview of how data is organized and managed within your VIBE session, as well as how to transfer data to and from your VIBE desktop.

---

# Data Organization

Because VIBE runs on the UBELIX cluster, it uses the same file system and storage structure as UBELIX. This means that your `$HOME` directory, along with all folders and data available in your UBELIX account, is automatically accessible within your VIBE desktop session.

This includes:

- [x] User `$HOME`
- [x] Workspace (Research Storage, in case you have)
- [x] Capacity Storage (in case you have)
- [x] Network Scratch
- [x] Local Scratch

Your existing storage quotas, snapshot policies, and backup services configured for your UBELIX account also apply to your VIBE session.

For detailed information about the different storage services provided by UBELIX, please refer to the official [documentation](https://hpc-unibe-ch.github.io/storage/).

!!! note
    We encourage researchers to use the **Research Storage Service** provided by the University. It offers centralized, cost-effective storage with daily backups, as well as seamless connectivity and data transfer between UBELIX and the VIBE environment.

If your project has specific storage requirements, or if you are unsure whether additional storage is needed, please [contact us](../contact.md) or request a [quote](https://intern.unibe.ch/dienstleistungen/informatik/dienstleistungen_der_informatikdienste/dienstleistungen___ressourcen/research_storage/index_ger.html) through the University IT Services website.

---

# Data Transfer

Data can be transferred to and from your VIBE environment in several ways. Below we describe the recommended options.

---

## 1. Via UBELIX OnDemand

You can use the UBELIX OnDemand web interface to upload and download files.

- Click on **"Files"** in the menu bar at the top left of the UBELIX OnDemand portal (see arrow in the image below).
- Your session’s `$HOME` directory will be displayed along with its contents.
- Use the **"Upload"** button to transfer files from your local computer to any directory within your VIBE session.
- Use the **"Download"** button to copy files from your VIBE session to your local computer.

![](../assets/images/transfer_data_via_ood.png)

---

## 2. Via Command Line (Advanced)

If you are comfortable working with the command line, you can transfer data using tools such as `scp` or `rsync`.

Please refer to the official UBELIX [documentation](https://hpc-unibe-ch.github.io/firststeps/movingdata/) for detailed instructions:


---

## 3. Connecting to a Cloud Service

If your data is stored in a cloud service (e.g., OneDrive, Google Drive, Dropbox), you can access it directly from VIBE using the web browser. Simply log in with your credentials as you would from any other system and upload or download files as needed.
