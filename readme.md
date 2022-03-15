# correr dockers y en continu
docker-compose up --build -d

# subir dockers a docker-hub
docker login
docker tag app_vuelos:v2 jasbel/app_vuelos:v2
docker tag microservice-passengers:v2 jasbel/microservice-passengers:v2
docker tag microservice-users:v2 jasbel/microservice-users:v2
docker tag microservice-flights:v2 jasbel/microservice-flights:v2

docker push jasbel/app_vuelos:v2
docker push jasbel/microservice-flights:v2
docker push jasbel/microservice-passengers:v2
docker push jasbel/microservice-users:v2


# docker-compose