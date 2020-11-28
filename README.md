# pi-hole-docker-asustor
Setup for running pi-hole in docker on asustor NAS

## Usage
1. Install git and docker on NAS
2. Login to NAS using ssh.
3. clone this repo
```
> git@github.com:Alecktos/pi-hole-docker-asustor.git
```
4. Create [password.env](#passwordenv) file containing password
5. run [run.sh](#runsh) to start pi-hole
```
> sh run.sh
```
6. Check that pi-hole admin ui is running <http://yourAsustorIpAddress/admin/index.php>

## run.sh
1. Takes down current running container if any. 
2. Kills `myhttpd` using sudo. Process listens to port 80 and 443, used by pi-hole.
3. Create and start pi-hole container in background

## password.env
Create `password.env` file with login password `WEBPASSWORD=MySecretPassword`
