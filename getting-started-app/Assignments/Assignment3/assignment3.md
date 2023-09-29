# Assignment3

Create Docker Containers for Web App and DB

I have a web application with a persistence database

1. Start an ubuntu container that will create a file named /data.txt with a random number between 1 and 10000.
```docker run -d ubuntu bash -c "shuf -i 1-10000 -n 1 -o /data.txt && tail -f /dev/null"```

2. Validate that you can see the output by accessing the terminal in the container
```docker ps```
```docker exec 7c0f62ae9eae cat /data.txt```

3. Now, start another ubuntu container (the same image)
```docker run -it ubuntu ls /```
```docker rm -f 3c904c384dc5``` (remove first container)

4. Create a volume by using the docker volume create command.
 ```docker volume create todo-db```

5. Start the todo app container, but add the --mount option to specify a volume mount. Give the volume a name, and mount it to /etc/todos in the container, which captures all files created at the path.
```docker run -dp 127.0.0.1:3000:3000 --mount type=volume,src=todo-db,target=/etc/todos getting-started```
verify that data persists

6. Inspect the volume
```docker volume inspect todo-db```

