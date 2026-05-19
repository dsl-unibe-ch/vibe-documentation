# Determine your resource needs

This guide should help you to determine the resources required for your usage. Requesting only the resources necessary comes with multiple advantages, mainly less usage costs and less waiting time before your desktop session is started.


The following is a comparison benchmark of resources used for applying deconvolution, a relatively intense computation task, that was performed on different computer configuration and datasets:

1. Testing different instances with same dataset:

|   Instance Size | data size (GB) |   GPU Type | Run time (s) |
| :-------------: | :-----------:  | :--------: | :----------: |
|      Medium     |   2.5          |   RTX 4090 | 172          |
|       Large     |   2.5          |   RTX 4090 | 169      |



2. Testing different data sizes with the maximum VIBE instance (60 cores, 360 GB RAM, 4x RTX4090):


|    data size   | 15GB  |  27GB   |    35GB  | 40GB   |  45GB  |
| :------------: | :----: | :----: | :------: | :----: | :----: |
| Run time (s)   | 398   |   811   |    964   | 1043  |  1155  | 


3. Testing different GPU performance on a Large VIBE instance with a 15GB dataset.


|     GPU Type   |  RTX 4090 | H100 | A100 |
| :------------: | :------: | :--: | :--: |
|  Run time (s)  | 387,07 | 634,78 | 843,16 | 


From these examples we can remark the following:

- [x] Larger session instance does not necessary help with computation performance for small datasets.
- [x] Computation time increases with larger dataset.
- [x] Different GPU types are optimized for different tasks and the fact that they have larger memory does not necessary translate in better performance for your image computation task.
    

!!! NOTE 
    The number presented here depend on a number of factors and this should only be used as a reference for your resources estimation. If you are unsure of how much resources do you think you will need, please feel free to get in touch with us for a customized guidance.

In addition, if you encounter problems with your application such as sudden crash or frozen while performing very demanding computation task, limited RAM resources may be one reason of this problem. Please have a look at the FAQ section to know more and troubleshoot this problem.