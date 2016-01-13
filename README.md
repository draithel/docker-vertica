# Docker Image for Vertica v7.2.1
This is a fork of a the great work done by [Sumit Chawla and those whom contributed to it via its parent forks](https://github.com/sumitchawla/docker-vertica). I have simply updated it to use Vertica v7.2.1.
The image is available in Docker registry at https://registry.hub.docker.com/u/colemantw/vertica/

Base OS is Ubuntu 14.04.

## Usage:
You can either pull the image from Docker Registry using following command:

```bash
docker pull colemantw/vertica
```

Or, build your own image using following command. Download the Vertica DEB package from https://my.vertica.com and put it in this folder as "vertica.deb".
Then run:
```bash
docker build -t colemantw/vertica .
```

### To run without a persistent datastore
```bash
docker run -p 5433:5433  colemantw/vertica
```

### To run with a persistent datastore
```bash
docker run -p 5433:5433 -d -v /path/to/vertica_data:/home/dbadmin/docker colemantw/vertica
```
### Connection Parameters
 Default DB Name - docker
 
 Default User - dbadmin
 
 Default Password (NO PASSWORD) - 
