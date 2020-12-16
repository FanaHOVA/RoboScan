# RoboScan
This is the source code for a Lego+Raspberry Pi-powered analog film roll scanner. Watch it in action:
[![RoboScan](https://img.youtube.com/vi/yRDomN48SOs/0.jpg)](https://www.youtube.com/watch?v=yRDomN48SOs)

## Installation
First build the Angular frontend:
```bash
cd scanner-frontend
npm install
ng build --prod
cd ..
```

Then deploy the docker-compose:
```bash
cd docker
# Adjsut the hostname to your Raspberry Pi
export DOCKER_HOST=tcp://piscanner:2376 DOCKER_TLS_VERIFY=
docker-compose up -d --build
cd ..
```

## Starting it
The camera must be connected to the Raspberry Pi via USB. It must be compatible with [libgphoto2](www.gphoto.org/proj/libgphoto2/support.php).
