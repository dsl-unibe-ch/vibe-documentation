# Known Limitations

## `lmod` currently unavailable on VIBE

VIBE currently is unable to load modules via the `lmod`, the tool that UBELIX uses to manage and change your software environment, so called modules. Find more information about the tool on the UBELIX documentation section on [Software Environments](https://hpc-unibe-ch.github.io/software/Lmod_modules/#finding-modules)

If you need a specific software or environment from the UBELIX software stack that is not currently present in the VIBE desktop, please get in touch with us.

## Clipboard not functional in some browsers

We have experience issues using the clipboard to copy content from the host system to some browsers including **Firefox** and **Safari**. 

**We recommend to use the Chrome browser** for the best experience using the VIBE desktop.

## Windows applications aren't supported

Desktops run on Linux, so Windows installers (.exe files) and native Windows applications aren't supported at this time.

## Extending a session after it expires

You can't extend the reservation time of a session that's already running. To continue working, start a new session and pick up where you left off. A few minutes before your session expires, you'll get a warning reminding you to save your work. To avoid interruptions, book enough time when you reserve your session.

## Links don't open in the browser automatically

When you click a link, for example in a terminal window, it won't open in the browser automatically. To open it, right-click the link and select **Open Link**.

For example, to open a JupyterLab notebook:

1. Start JupyterLab from the terminal.
2. In the terminal output, find the link where the application is hosted.
3. Right-click the link and select **Open Link**.

Firefox opens and loads your JupyterLab notebook.