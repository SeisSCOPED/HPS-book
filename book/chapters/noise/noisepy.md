# NoisePy


We will test NoisePy, a python package for ambient noise seismology.
While the software is currently under active development, we will test its new functionality for-cross correlation on the AWS SCEDC data.


Follow the [instructions](../cloud/AWS_101.md) to launch a cloud instance and install Docker.

1. Pull the image. This will pull the Docker image named `seisscoped/noisepy` from the GitHub Container Registry.
    ```bash
   sudo docker pull ghcr.io/seisscoped/noisepy:centos7_jupyterlab
    ```

2. Run the docker image as container. This will launch a Jupyter Lab within the container. The command also forwards port 8888 from the container to port 8888 on the EC2 instance.
    ```bash
    sudo docker run -p 8888:8888 --rm -it ghcr.io/seisscoped/noisepy:centos7_jupyterlab
    ```

Then, follow the [instructions](../cloud/AWS_101.md) To open the Jupyter notebook/lab, them find the Public IP address.