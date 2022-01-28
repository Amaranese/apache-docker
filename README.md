# Simple APACHE Server 
![Apache](https://www.prodefence.org/wp-content/uploads/2017/06/apache-web-server.png)

To build our image, give it a name with the `-t` flag in the below command 

## BUILD 

```
docker build -t wsimage:v1 .

```
- The tag v1 is now added
- Check image is up by running 

```
docker images
```

## RUN 

run in the background using the `-d` flag as shown below where `externalIP` is your free port


```
docker run -d --name wscontainer -v $(pwd)/src:/var/www/html/ -p externalIP:80 wsimage:v1
```

Example 

```
docker run -d --name wscontainer -v $(pwd)/src:/var/www/html/ -p 8880:80 wsimage:v1
```


## LOG INTO CONTAINER 

```
docker exec -it <container name> /bin/bash
```

