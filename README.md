# Share a folder with sshfs and Docker

On server, where the folder is, run: 

	sudo docker run -e HOST=$(hostname) -p 1522:22 -v $(readlink -e .):/_ -ti sharefolder

 On client, use sshfs to mount the shared folder: 

	sshfs -p 1522 _@hostname:/_ mount/
