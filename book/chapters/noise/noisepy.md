# NoisePy


We will test NoisePy, a python package for ambient noise seismology.
While the software is currently under active development, we will test its new functionality for cross correlation on the AWS SCEDC data.


Follow the [instructions](../cloud/AWS_101.md) to open a cloud instance from docker. Make sure to choose an ``AMD`` platform.

Then in terminal, pull the noisepy docker image.

```bash
sudo docker pull ghcr.io/seisscoped/noisepy:centos7_jupyterlab
sudo docker run -p 8888:8888 --rm -it ghcr.io/seisscoped/noisepy:centos7_jupyterlab
```

To open the notebooks, them find the Public IP address.