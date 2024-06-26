# Introduction

Ambient noise seismology is a fundamental subdiscipline of seismology that extract information about the Earth structure from diffuse waves.

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vSO6ACNFGwGJK-Q6kLKuyWBBA7XpGVdFuVvPUYQ8YcacqkrtcuqizypbsuB6y4q6APmFllmt8aUGnXe/embed?start=true&loop=false&delayms=3000" frameborder="0" width="800" height="474" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

We will test NoisePy, a python package for ambient noise seismology.
While the software is currently under active development, we will test its new functionality for-cross correlation on the AWS SCEDC data.

Follow the [instructions](../cloud/AWS_101.md) to launch a cloud instance and install Docker.

1. Pull the image. This will pull the Docker image named `seisscoped/noisepy` from the GitHub Container Registry.
    ```bash
   sudo docker pull ghcr.io/seisscoped/noisepy:centos7_jupyterlab
    ```

2. Run the docker image as container. This will launch a Jupyter Lab within the container. The command also forwards port 8888 from the container to port 80 on the EC2 instance (default port of the http service).
    ```bash
    sudo docker run -p 80:8888 --rm -it ghcr.io/seisscoped/noisepy:centos7_jupyterlab\
        nohup jupyter lab --no-browser --ip=0.0.0.0 --allow-root  --IdentityProvider.token=scoped &
    ```

Then, follow the [instructions](../cloud/AWS_101.md) to find the Public IP address and open the Jupyter notebook/lab with token `scoped`.


