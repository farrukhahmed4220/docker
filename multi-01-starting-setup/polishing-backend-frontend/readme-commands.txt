#For Creating MongoDB Container:

docker run --rm -d --network goal-net -v data:/data/db -e MONGO_INITDB_ROOT_USERNAME=farrukh -e MONGO_INITDB_ROOT_PASSWORD=adminfarrukh --name mongodb mongo


#For Creating Backend Container, Go inside backend folder and run these command,change the path for bind mount:
docker build -t goal-backend
docker run --rm -d -p 80:80 --network goal-net --name goal-backend -v /app/node_modules -v /home/adminuser/Desktop/docker-complete/multi-01-starting-setup/polishing-backend/backend:/app -v logs:/app/logs goal-polish-backend


#For Creating Frontend Container, go inside frontend folder and run these commands, change the path for bind mount:
docker build -t goal-polish-frontend
docker run --rm -d -it -p 3000:3000 -v /home/adminuser/Desktop/docker-complete/multi-01-starting-setup/polishing-backend-frontend/frontend/src:/app/src --network goal-net --name goal-frontend goal-polish-frontend


