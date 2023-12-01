# Project-4

# Part 1
- Website added to /website  
  - Bonzai website (for you entertainment)

## Installing Docker

- ```curl -fsSL https://get.docker.com -o get-docker.sh```  
- ```sudo sh get-docker.sh```

[Image]

## Create a container image that will run a webserver and contains your website   
  
### Official Nginx image
```FROM nginx:latest```

### Copy website files into the default Nginx html directory (in this case copy entire website folder)
```COPY website/ /usr/share/nginx/html/```

### Expose port 80 for web traffic
```EXPOSE 80```

### Command to start Nginx when the container launches
```CMD ["nginx", "-g", "daemon off;"]```

## Build Docker image  
- ```docker build -t website .```  

[Image]
[Image]

## Run Container  
- ```sudo docker run -d -p 8080:80 --name website-container website```
  
### Now go to http://localhost:8080/ and boom:  

[Image]  
 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~  

  

