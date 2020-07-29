# Apache
### MAINTAINER> MW1-4

### Set up Info
1) OS : CentOS 7
2) Apache : Apache 2.4.X


### \<Apache-version\>\_\<Change_Version\>.tar.gz layout
/conf : configuration folder  
/ssl : sample.key, sample.crt, ssl_passwd.sh  
/start.sh : apache start shell script  

### Create an Image:
#### 1. Build an Docker Image
```bash
$ docker build -t <name: ex)apache:v20.0> -f <Dockerfile: ex)Dockerfile_v20.3> .
```

### Generate a Container from Image (access url = (http) : localhost:8080 or (https) : localhost:443)
```bash
$ docker run -p 8080:80 -p 443:443 <Image name>
```
