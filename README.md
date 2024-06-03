# asuswrt-merlin-tuf-ax3000-v2-build

## build
git clone https://github.com/gnuton/asuswrt-merlin.ng.git  
cd asuswrt-merlin.ng  
docker pull gnuton/asuswrt-merlin-toolchains-docker:latest  
docker run -it --rm -v "$PWD:/build"  -u "docker:docker" \
       gnuton/asuswrt-merlin-toolchains-docker:latest /bin/bash
source /home/docker/envs/bcm-hnd-ax-4.19.sh
cd release/src-rt-5.04axhnd.675x/
make "tuf-ax3000_v2"



