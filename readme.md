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
