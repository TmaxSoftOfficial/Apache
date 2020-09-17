# HyperFrameOE-Apache

This Apache docker file is for HyperFrame Open Edition.

### Prerequisites

Docker 19.03.12 (Workspace version, recommended)

### Requirements

1) OS : CentOS 7
2) Apache : Apache 2.4.X

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

#### 1. Download Dockerfile.

#### 2. To change the configuration, modify files under the conf directory.

#### 3. Place the Dockerfile and start.sh files and the conf, license, and ssl directories in the same path.

#### 4. Build a Docker Image.

```bash
$ docker build -t <create image_name>:<image_version> .
```

#### 5. Generate a Container from the Image.

```bash
$ docker run -p 8080:80 -p 443:443 <image_name>:<image_version>
```

### License

Projects are licensed under the Apache 2.0 license. See the [LICENSE](https://github.com/TmaxSoftOfficial/HyperFrameOE-Apache/blob/master/apache_2.4/license/license.dat) file.

### Version History

[HyperFrame OE, Apache 2.4.41](https://github.com/TmaxSoftOfficial/HyperFrameOE-Apache/blob/master/apache_2.4/Dockerfile "dockerfile link") (latest)

### HyperFrameOE Service Level
[HyperFrameOE Service Level](https://github.com/TmaxSoftOfficial/HyperFrameOE-About/blob/master/ServiceLevel.md)
