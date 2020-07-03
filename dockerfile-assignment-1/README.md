## Docker File

Create an image based on the docker file using a simple node application.

### Quick Start

\** The docker file "Dockerfile" contains all steps to create an image of this application.

1. Run `cd dockerfile-assignment-1` to go the directory.

2. Run `docker image build -t node6-app-img .` to build the image.

3. Run `docker container run --rm -p 80:3000 node6-app-img` to test the image. 
    
    ** Open your browser and navigate to `http://localhost`.

### Push This Image To Docker Hub

1. Run `docker login` to signin to [Ducker Hub](https://hub.docker.com/).

2. Run `docker image tag node6-app-img USERNAME/simple-node-app` to create a tag name for this image. ** Please change your username.

3. Run `docker image push USERNAME/simple-node-app` to push the image to Docker Hub.

### Test Your Image From Docker Hub

1. Run `docker image rm USERNAME/simple-node-app` to remove the image locally.

2. Run `docker container run --rm -p 80:3000 USERNAME/simple-node-app` to test it from Docker hub.
