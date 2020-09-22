# HyperFrameOE-Apache

This Apache docker file is for HyperFrame Open Edition.

### Prerequisites

Docker 19.03.12 (Workspace version, recommended)

### Requirements

#### 1) OS : CentOS 7
#### 2) Apache : Apache 2.4.X

### Directory Structure                                                         

```bash                                                                     
${pwd}                                                                       
|- apache_2.4                                                  
|   |- Dockerfile_list               # Dockerfile list directory
|   |   |-<dockerfile_version> ...       # Dockerfile version
|   |   |   |- Dockerfile                
|   |- conf                          # Configuration directory  
|   |   |- httpd.conf                    # Main configuration file
|   |   |- httpd-ssl.conf                # Apache configuration file that provides the functionality of secure (SSL/TLS) connections
|   |   |- httpd-vhost.conf              # Apache configuration file that manages virtual hosts
|   |- license                       # license directory  
|   |   |- LICENSE                       # Apache license                                  
|   |- ssl                           # ssl directory  
|   |   |- server.crt                    # Self-signed sample certificate
|   |   |- server.key                    # Private sample key for SSL certificate
|   |   |- ssl_passwd.sh                 # Shell script for setting passwords for sample SSL keys
|   |- CHANGES                                                               
|   |- [latest]Dockerfile                    
|   |- start.sh
|- README.md                                                                    
```                                                                         

### Installing Steps:

### You can choose one of the following two installation methods.

### Installation Method 1 (using Dockerfile and binary after downloading them from GitHub)

#### 1. Access the following site: https://github.com/TmaxSoftOfficial/HyperFrameOE-Apache.

#### 2. Download the Dockerfile and binary.

#### 3. To change the configuration, modify files under the conf directory.

#### 4. Place the Dockerfile and start.sh files and the conf, license, and ssl directories in the same path.

#### 5. Build a Docker Image.
```bash
$ docker build -t <create image_name>:<image_version> .
```

#### 6. Generate a Container from the Image.
```bash
$ docker run -d -p 8080:80 -p 443:443 <image_name>:<image_version>
```


 

### Installation Method 2 (using Image of Docker Hub)

#### 1. Search for the Image.
- It can be searched from Docker Hub (https://hub.docker.com/repository/docker/tmaxsoftofficial/hyperframeoe-apache) or with the following docker search command.
```bash 
$ docker search hyperframeoe-apache
```

#### 2. Pull the Image.
```bash
$ docker pull tmaxsoftofficial/hyperframeoe-apache:latest
```

#### 3. Build a Docker Image.
```bash
$ docker build -t tmaxsoftofficial/hyperframeoe-apache:latest .
```

#### 4. Generate a Container from the Image.
```bash
$ docker run -d -p 8080:80 -p 443:443 tmaxsoftofficial/hyperframeoe-apache:latest
```


### License

Projects are licensed under the Apache 2.0 license. See the [LICENSE](https://github.com/TmaxSoftOfficial/HyperFrameOE-Apache/blob/master/apache_2.4/license/license.dat) file.

### Version History

[HyperFrame OE, Apache 2.4.41](https://github.com/TmaxSoftOfficial/HyperFrameOE-Apache/blob/master/apache_2.4/Dockerfile "dockerfile link") (latest)

### HyperFrameOE Service Level
[HyperFrameOE Service Level](https://github.com/TmaxSoftOfficial/HyperFrameOE-About/blob/master/ServiceLevel.md)
