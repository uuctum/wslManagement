# Install podman to wsl2

    sudo apt install podman


# Stop all the containers

    docker stop $(docker ps -a -q)

# Remove all the containers

    docker rm $(docker ps -a -q)

# Remove specific unused items

    docker container prune
    docker image prune
    docker volume prune
    docker network prune

# Remove all unused items

    docker system prune

