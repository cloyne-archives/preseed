# preseed

beginnings of a minimal debian seed

## how to

download the latest debian netinst .iso

    wget http://cdimage.debian.org/debian-cd/7.1.0/amd64/iso-cd/debian-7.1.0-amd64-netinst.iso

copy the .iso to your lucky flash drive

    dd if=debian-7.1.0-amd64-netinst.iso of=/dev/sd#

host the preseed in this directory

    cd preseed/
    python -m SimpleHTTPServer

meanwhile, boot from the flash drive, then at the splash page type

    auto url=http://yourSimpleHTTPServer:8000/preseed.cfg

replacing yourSimpleHTTPServer with your hostname or IP address
