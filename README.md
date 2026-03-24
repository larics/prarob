# prarob
Repozitorij za laboratorijske vježbe kolegija "Praktikum robotike". (https://www.fer.unizg.hr/predmet/prarob)

## Upute
Laboratorijske vježbe akademske godine 2025./2026. se provode unutar ROS2 Jazzy okruženja.

ROS2 Jazzy je namjenjen za Ubuntu 22.04 distribuciju, ako imate drugu distribuciju Ubuntua ili želite modularnu instalaciju iskoristite Docker.

U ovom repozitoriju se nalazi Dockerfile pomoću kojeg možete jednostavno instalirati ROS2 Jazzy Docker container.

Kako biste pokrenuli Docker container, preuzmite Dockerfile iz glavnog direktorija ovog repozitorija i pokrenite sljedeću naredbu:
```
docker build -t prarob -f prarob.Dockerfile  .
docker run -it \
    --privileged \
    --device=/dev/ttyUSB0:/dev/ttyUSB0 \
    --env="DISPLAY=$DISPLAY" \
    --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw"
    prarob
```


Detaljnije upute za docker dostupne su na: https://github.com/larics/docker_files/wiki.
