# FAQ

Here you will find a list of the most frequently asked question and how to troubleshoot some issues.



## *Why my application crashes opening a large image or in the middle of an intense computation?*

RAM limitation may be a cause of your application crashing when working on large datasets. Consider increasing the size of your VIBE instance in terms or RAM. If you have specific requirements that surpass the current configuration, contact us to analyze and help you troubleshoot your resources needs.

## *I cannot work or interact on my session, is just lagging and too slow*

The user experience on the VIBE desktop depends among other factors on the stability of your network. Try to get a faster internet connection and reduce the image quality at launch time.

## *My session suddenly crash with message: "New connection has been rejected with reason: Authentication failed"*

Sometimes when the VIBE desktop site is refreshed or let idle for a few times it could suddenly crash. This is a known issue of the VNC server trying to stablish a connection and fail on authentication. Luckily this is not shutting down your session. To reestablish your session, simply return to the OpenOnDemand site on "My Interactive Sessions" and push the blue button on your session to reestablish your active session.

## *The layout and text of the VIBE desktop is too big and difficult to work with*

This may be caused by the current resolution settings of your screen of your host computer. Try to increase the resolution of your screen or if this is not possible, try to use the zoom out tool from your browser.

## *Is it possible to mount a smb share on my VIBE session?*

Unfortunately UBELIX policy restrict to mount external storage as this inherently leads to performance issues. Therefore currently data needs to be transferred in/out via either scp/rsync or through the OnDemand GUI. If users have access to research storage shares, they can also mount the share on their devices using smb and transfer data using smb to UBELIX.