# HyperFrameOE-Apache

This is a group of Apache Docker files with versions for HyperFrame Open Edition.

### Prerequisites

Docker 19.03.12 (This is a workspace's version, other versions might be compatiable with this.)

### Set up Info

1) OS : CentOS 7
2) Apache : Apache 2.4.X

### Directory layout                                                         

```bash                                                                     
${pwd}                                                                       
|- apache_2.4                                                  
|   |- Dockerfile_list               # Dockerfile list directory
|   |   |-<dockerfile_version> ...       # Dockerfile version
|   |   |   |- Dockerfile                
|   |- conf                          # conf directory  
|   |   |- httpd.conf                    # The main Configuration File 
|   |   |- httpd-ssl.conf                # Apache configuration file that provide the functionality of Secure (SSL/TLS) connections
|   |   |- httpd-vhost.conf              # Apache configuration file that manage Virtual hosts
|   |- license                       # license directory  
|   |   |- LICENSE                       # Apache License                                  
|   |- ssl                           # ssl directory  
|   |   |- server.crt                    # Self-signed sample Certificate
|   |   |- server.key                    # Private sample key for ssl certificate                         
|   |   |- ssl_passwd.sh                 # Shell script for setting password when using sample ssl key
|   |- CHANGES                                                               
|   |- [latest]Dockerfile                    
|   |- start.sh
|- README.md                                                                    
```                                                                         

### Installing:

#### 1. Download a Dockerfile you want.

#### 2. If you want to modify the configuration, change the file below the conf directory.

#### 3. Place 'Dockerfile', 'conf' directory, 'start.sh', 'license' directory, and 'ssl' directory in the same path.

#### 4. Build an Docker Image.

```bash
$ docker build -t <create image_name>:<image_version> .
```

#### 5. Generate a Container from Image.

```bash
$ docker run -p 8080:80 -p 443:443 <image_name>:<image_version>
```

### License

This project is licensed under the Apache-2.0

