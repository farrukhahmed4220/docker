#Copy the command to Build the image first

docker build -t util-node .


#COpy the command to run the container that are being used with bind mount and  make the package
docker run -it -v $(pwd) util-node init
docker run -it -v $(pwd) util-node install express --save

OR

#You can use docker-compose to bring up the utility container

docker-compose run npm-container init

docker-compose run npm-container install express --save 
