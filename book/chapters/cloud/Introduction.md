# Introduction


## Cloud

Cloud computing refers to a system of rather loosely connected nodes. There are many cloud providers, though three are on the top list: Amazon Web Services (AWS), Google Cloud Platform (GCP), Microsoft Azure Cloud (Azure). Each of these cloud providers offer a free Python Hub access.

Cloud centers are distributed around the world, to enable global fast access to computing resources. The centers are called `regions`.

Usually, storing data on Clouds is the most expensive of geoscience research. One would typically find the 1) data storage/archive, then 2) choose the cloud provider. For optimal I/O performance, it is recommended to choose the `region` where the data is stored for compute.

Watch a presentation from eScience Institute Cloud experts Naomi Altermann (UW) and Rob Fatland (UW) regarding cloud computing: 
[Presentation](https://docs.google.com/presentation/d/1E9_nGlHW8Rz2g4UrQMXyRVZ1UoxuSNejGmszf-OVDrI/edit?usp=drive_link) and their video tutorial:
<iframe width="560" height="315" src="https://www.youtube.com/embed/S6X10HZDyrA?si=xMuZC5-VqMJjU9Rz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


### Google Colab

If you have a google account, you can access to a free tier GCP instance that uses CPU, or GPU, or TPU (Tensor Processing Unit).

Here is an example of a Google Colab: 
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1gpRHGtu9s67xntmM0uUtCJSBcSlB9vo0#scrollTo=J7KihpWyh9ed)


### AWS

AWS is the Amazon services for cloud. It is the cloud leader. Chapter 7 details access and usage of these resources.

Their JupyterHub for machine learning is ran out of [Sagemaker Studio](https://aws.amazon.com/sagemaker/). The first 250 hours of use (within the first 2 months) are *free*.

Why use AWS in the geosciences? It stores already lots of [open access data](https://registry.opendata.aws/). AWS also gathers Sagemaker notebooks associated with these open data for machine-learning purpose. See the [notebook catalog](https://registry.opendata.aws/service/sagemaker-studio-lab/usage-examples/).

Cool [geoscience data sets](https://aws.amazon.com/marketplace/search/results?category=ffb6cf06-608c-4b14-a5a9-756f1ccd5725&FULFILLMENT_OPTION_TYPE=DATA_EXCHANGE&CONTRACT_TYPE=OPEN_DATA_LICENSES&DATA_AVAILABLE_THROUGH=S3_OBJECTS&PRICING_MODEL=FREE&filters=FULFILLMENT_OPTION_TYPE%2CCONTRACT_TYPE%2CDATA_AVAILABLE_THROUGH%2CPRICING_MODEL) stored on the S3 (storage service) of AwS are. [Radiant MLHub](https://mlhub.earth/datasets) stores data on S3.

Some specific data set that could be used in this book:

* **Seismic Data**
    - Southern California Seismic Network. [Here](https://aws.amazon.com/marketplace/pp/prodview-c4rk5lxymj43i?sr=0-99&ref_=beagle&applicationId=AWSMPContessa).
    - Northern California Earthquake Data Center [here](https://registry.opendata.aws/northern-california-earthquakes/)
    - Distributed Acoustic Sensing (DAS) PoroTomo experiment. [Here](https://aws.amazon.com/marketplace/pp/prodview-qd7w6cbnmssl2?sr=0-41&ref_=beagle&applicationId=AWSMPContessa).
    - OpenEEW: low cost seismometers distributed in populated areas. [Here](https://aws.amazon.com/marketplace/pp/prodview-ot34yes3afyhq?sr=0-1&ref_=beagle&applicationId=AWSMPContessa)


### Azure

Azure is the Microsoft cloud computer. Chapter 7 details access and usage of these resources.

The JupyterHub *free* access of Azure is called the [Planetary Computer](https://planetarycomputer.microsoft.com/).

Cool [data sets](https://planetarycomputer.microsoft.com/catalog) to access directly on Azure that focus on oceans, atmosphere, surface land, demographics. Example below:

- [Landsat](https://planetarycomputer.microsoft.com/dataset/group/landsat)