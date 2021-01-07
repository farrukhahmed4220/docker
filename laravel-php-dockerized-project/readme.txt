# RUN this command
docker-compose up -d --build server

# Then run this command , after successfuly run below command visit, localhost:8000
docker-compose run --rm artisan migrate
