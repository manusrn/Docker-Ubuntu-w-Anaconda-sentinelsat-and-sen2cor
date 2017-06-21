# Docker-Ubuntu-w-Anaconda-sentinelsat-and-sen2cor
Docker unbuntu-based able to run sentinelsat and sen2cor

DOcker container based on ubuntu, added full Anaconda2 to run ESA Sen2cor processing

Added Anaconda2 from docker anaconda : https://github.com/ContinuumIO/docker-images/tree/master/anaconda

Added sentinelsat from https://github.com/ibamacsr/sentinelsat to download data from sentinel data hub

Added Sen2cor processing from lvhengani : https://github.com/lvhengani/sen2cor_docker

Added Apache2 and PHP7 from https://github.com/tagplus5/docker-php/tree/master/7-apache

#Build the Docker image:
-download repository
-go in the repo and launch docker

$docker build -t $IMAGE_NAME .

#using the docker container :

$docker run -p $port_on_host:$port_on container $IMAGE_NAME

ex : docker run -p 8888:80 docker-Ubuntu-w-Anaconda-sentinelsat-and-sen2cor

#To link  repository on the host to a repository inside the container :

Add to the previous line : -v /path_on_host:/path_in_container

ex :  docker run -p 8888:80 -v /c/Users/doc:/media/products  docker-Ubuntu-w-Anaconda-sentinelsat-and-sen2cor

If one of the repostories doesn't exist, it will be created. Otherwise, everything inside host repository will be accessible in container repository, and vice-versa.
