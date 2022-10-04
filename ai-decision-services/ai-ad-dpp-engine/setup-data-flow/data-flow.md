Lab 5: Configure OCI Data Flow service
===

Data Flow is OCI's cloud based serverless Spark service. This workshop will mainly rely on Data Flow to process data and conduct post processing steps. Users can choose the appropriate shape for the driver and executor nodes based on data size. Increasing the number of Executors will speed up the processing for large data sets. For small data sets such as the ones used in this workshop, most of the options can be left at their default values. The following options need to be updated:

![](./images/Set-DF1.png)
![](./images/Set-DF2.png)

*   For the **Language** section, choose **Python**.
*   Select df_driver.py from the driver bucket.
*   For **Arguments**, simply input `--response ${response} --phase ${phase}`, and enter **placeholder** as the default value. This will be overriden later
*   For **Archive URI**, enter the fully qualified path to archive.zip in Object Storage. The structure of path is `oci://<bucket-name>@<namespace>/<path-to-archive.zip>`. Same below.
*   At **Application log location**, enter the path to logs-bucket. This is very useful for debugging when the application run fails.