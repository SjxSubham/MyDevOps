#### Docker Tutorial just in 11 mnt

[Tutorial](https://youtu.be/DQdB7wFEygo?si=K-dk9NiCktU2rzcu)


- [X] Harkirat's reference site/documentation link - [Documentation](https://projects.100xdevs.com/tracks/docker-2/docker-2-1)



****
## Some Docker Commands

- TO run
` docker run <image_name> `

- To run on specific PORT 
` docker run -p 27018:27017 run mongo `  - lets u create a port mapping

- TO run container it in detached mode
` docker run -d <image_name> `

- To delete an image from images list ` docker rmi <image_name> ` or to Delte a image forcefully ` docker rmi <image_name> --force `

- To kill a running container 
` docker kill <container_id> `

- To show all image list ` docker images `

- To show all running container list currently 
` docker ps `

- To build a image 
` docker build -t <image_name> . `


#### Example
```Dockerfile
 # Suppose I'm trying to build a docker container

- FROM node:20      ----\
- WORKDIR /app            ----\
- COPY . .                      -----\
- RUN npm install                     ---> when u create ur image
- RUN npm run build             -----/
- RUN npx prisma generate ----/

- CMD ["node", "dist/index.js"] ---> When Starting the contaner

```

## Some more Commands
- How to execute a command inside a container
- Running an interactive shell , inside a container
` docker exec -it <container_name> /bin/bash `
    - check inside file structure
        ` root@a64458638b42:/app# ls `
    - to check CPU running usage
        ` root@a64458638b42:/app# top `
    - exit from interactive shell 
        ` root@a64458638b42:/app# exit `
- If u dont want to go inside interactive shell : ` docker exec <container_name> ls `



-- DATE - 14 june 2k25 -time stamp - 1:27:22 #harkirats docker tutorial


- Layers in Docker- step 15 - [Documentation](https://projects.100xdevs.com/tracks/docker-2/docker-2-15)

