# pi-hole-docker-asustor
Setup for running pi-hole in docker on asustor NAS

## Run
```
> sh run.sh
```

## run.sh
1. Takes down current running container if any. 
2. Kills `myhttpd` using sudo. Process listens to port 80 and 443, used by pi-hole.
3. Create and start pi-hole container in background
