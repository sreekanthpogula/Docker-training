# Assignment4

Create a Custom Network and Add Containers

To create a custom bridge network and add containers to it:

1. Create a custom bridge network

```docker network create my-network```

2. Run
Start containers and attach them to the custom network:

```docker run -d --name goofy_wright --network my-network getting-started```
```docker run -d --name kind_morse --network my-network ubuntu```

Now, goofy_wright and kind_morse can communicate with each other using their container names as hostnames.
