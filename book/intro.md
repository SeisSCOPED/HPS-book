# Welcome to the HPS Jupyter Book!


![banner](img/banner_small.png)

📖 On this JupyterBook website, you will find resources for high-performance computing tailored to seismological research. In particular, we talk about two types of large-scale seismological research:
* Wavefield and earthquake simulations
* Big Data Mining

Both leverage two computing architectures: HPC and Cloud. This book provides training for best practices in computing and software environment.


## SSA Workshop 2024 Data Mining and Cloud 101 - information

This workshop will introduce participants to cloud computing, from concept and best practices to practice, for two main approaches of data mining in seismology: correlation seismology and machine learning. Participants will learn how to port their Python scripts from their laptops to the cloud, analyze their intermediate data products, and download the final data product. Participants will learn ambient noise seismology software noise and run it on cloud-hosted data sets of broadband seismometers and distributed acoustic sensing data. Participants will learn machine learning in seismology (earthquake catalog building and data discovery of various geohazards). The workshop curriculum is supported by the NSF project SCOPED.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRfbyhdW1xvgO0QTqQsaezZ4Xg0INNqOfjxWcCN4zeZDDlPqwnnXFv6je1b3ToELTDTk5VO13rsdXdC/embed?start=true&loop=false&delayms=3000" frameborder="0" width="800" height="474" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

:::{note}
URL to log-in to the AWS account for this workshop is https://806812320051.signin.aws.amazon.com/console.
Participants must use the username of the email address used for the workshop registration and the password sent via direct message on slack.
:::

### SCHEDULE

| Time | Topics | Instructors |  Link to notebook or slides |
| --- | --- | ---| --- |
| 9:00-9:30m |  Welcome  | Marine Denolle and Felix Waldhauser| |
| 10:00-11:15am | Cloud 101 | Yiyu Ni, Zoe Krauss, Marine Denolle | https://github.com/SeisSCOPED/seis_cloud, [book](./chapters/cloud/AWS_101.md)|
| 11:15-12:30 | Ambient Noise | Yiyu Ni, Kuan-Fu Feng, Marine Denolle | https://github.com/SeisSCOPED/noisepy, [book](./chapters/noise/noisepy.md)|
| 12:30 - 1:30pm| Lunch Break ||
| 1:30 - 2:30 pm | QuakeCatalog Building |  Kaiwen Wang | [ML Workflow - Lamont](./chapters/quake_catalog/MLworkflow_quakeflow.ipynb)|
| 2:30 - 3:30 pm | Event Discimination with ML | Akash Kharita | [ML-Detect](./chapters/quake_catalog/Automated_Surface_Event_Detection.ipynb)|
| 3:30 - 3:40 pm  | Coffee Break ||
| 3:40 - 5:00pm | Unsupervised Learning | Theresa Sawi |[SPECUFEX](./chapters/quake_catalog/specufex.ipynb)| 

