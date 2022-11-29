# Launch the Mongo DB container
docker run \
-p 27017:27017 \
-d \
-e MONGO_INITDB_ROOT_USERNAME=admin \
-e MONGO_INITDB_ROOT_PASSWORD=password \
--name mongodb \
--net mongo-network \
mongo

# Lauch MongoDB Express

docker run \
-p 8080:8081 \
-e ME_CONFIG_MONGODB_ADMINUSERNAME=admin  \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=password \
-e ME_CONFIG_MONGODB_SERVER=mongodb \
--name mongo-express \
--net mongo-network \
mongo-express

check the result http://localhost:8080


