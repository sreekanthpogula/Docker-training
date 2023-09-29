Assignment4: Create a Custom Network and Add Containers

To create a custom bridge network and add containers to it:

# Create a custom bridge network:
docker network create my-network

# run
Start containers and attach them to the custom network:

docker run -d --name container1 --network my-network your-image1
docker run -d --name container2 --network my-network your-image2

Now, container1 and container2 can communicate with each other using their container names as hostnames