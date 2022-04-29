# Xdcc Downloader Docker
This project aim to create a docker image containing all xdcc dependencies and funcionalities.  
The image expose port 8888 as web access port.  

![alt name](https://i.imgur.com/zjwTn7M.png "screnshot")

## Docker compose
Use the **docker-compose** file to build and run the container in once.
```
$ docker-compose up -d
```
OR
```
$ docker-compose up -d --build
```

It will map the **/download** folder to the **/downloads** container folder.  
So edit the XdccDownload Settings throw the interface to download the file in that folder.
