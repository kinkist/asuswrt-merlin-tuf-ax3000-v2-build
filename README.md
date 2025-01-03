# asuswrt-merlin-tuf-ax3000-v2-build

## build
```
mkdir build

chmod 777 build

cd build

docker pull gnuton/asuswrt-merlin-toolchains-docker:latest  

docker run -it --rm -v "$PWD:/build"  -u "docker:docker" \
       gnuton/asuswrt-merlin-toolchains-docker:latest /bin/bash

git clone https://github.com/gnuton/asuswrt-merlin.ng.git  

cd asuswrt-merlin.ng
###### change tag for you wanted to building version, (git checkout tags/3004.388.6_2-gnuton1)  

export MERLINUPDATE=n
export MODEL=tuf-ax3000_v2
export SDK=src-rt-5.04axhnd.675x
export UI=default
export SKIP_BUILD=false
export GIT_REPO=https://github.com/gnuton/asuswrt-merlin.ng.git

source /home/docker/envs/bcm-hnd-ax-4.19.sh


cd release/${SDK}
# make ${MODEL}
```


