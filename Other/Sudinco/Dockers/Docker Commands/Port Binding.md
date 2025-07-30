
`docker run -d -p 9000:80 image_name`
- `-d` for detach (so the terminal is free for other processes)
- `-p` to publish => this will expose he container to the *localhost* 
- `9000:80`
	- `9000` is used for the **host port** 
	- `80` is the **port on which the container is using to run the image**
		- Every application has their own Port inside a container 