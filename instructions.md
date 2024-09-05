Download docker

download docker img like node form docker hub

in cmd type ``docker pull node``

vscode: install docker extention


in nodeapp create dockerfile write code



``docker build -t myapp . ``

then we can see on docker desktop node as well as myapp 

we should not install nodemodules 

even if they r present we can create ``.dockerignore`` and add nodemodules into it

port maps in desktoip same like 4000 maps 4000

but in cmd also we can do

docker images
``docker run --name myapp_c1 myapp``

we can c listening for requests on port 4k
but when we run loaclhost 4k we cant c anything

open new terminal, go to project dir
``docker ps``
``docker stop myappp_c1``

now go to prev termianl and we can c that /c is stopeed

``docker run --name myapp_c2 -p 4000:4000 -d myapp``

now open loaclhost 4k and its working

``docker stop myapp_c2``
``docker ps``
``docker ps -a``
``docker start myapp_c2``

if we change anything in code we need to build docker again for new img
``docker build -t myapp .``

before copy . . all layers can be pulled from scratch maske sure it has 4 layers

````
FROM node:17-alpine

WORKDIR /app

COPY package.json .

RUN npm install
````

``docker build -t myapp4 . ``

if u change again anything in app.js then create new img like

``docker build -t myapp5 . ``

to check if everything is fine now

``docker run --name myapp5_c -p 4000:4000 my app5``

now eevrything in browser localhost is working





