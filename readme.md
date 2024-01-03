# first docker

npm init -y

in package.json:
"type": "module"

# docker Cheatsheet

```javascript

docker pull <imagename> //lädt das image vom docker hub

docker run <imagename> // erstellt aus einem image ein Container, wenn das Image Lokal nicht vorhanden ist versucht docker es aus dem Hub zu laden

docker image ls // listet die vorhanden Image dateien auf

docker container ls // listet alle laufenden Container auf

docker container ls -a // listet auch alle beendeten Container auf

docker start <containername | containerid> // startet den Container

```

# Create a Image

1.- Create a Dockerfile

```markdown
# we use the node image (with ubuntu:alpine) as basis image

FROM node:alpine

# create a folder for the project

RUN mkdir firstdocker

# go to the new folder

WORKDIR /firstdocker

# we copy all ours data in our image

COPY . .

# we create the necessary files

RUN npm i

# We give the PORT number

EXPOSE 9000

# We define the comands to start the container as Array

CMD ["node", "app.js"]
```

# BUILD IMAGE

docker build .

![buildimage](/img/buildImage.png)

docker image ls

![list](/img/listimg.png)

docker run --name firstdocker_01 -d -p 8080:9000 1599a7e57c93

(with the id run the image in backdround (-d) and give a new port for 9000-> here 8080)

![runid](/img/runid.png)

docker container ls

![runid](/img/clist.png)

check the container list & test the container

![runid](/img/contworks.png)
