**How to create an image and run it in the container** 
- I want to host static page in the Nginx server.
- Steps given below to create a docker image, run it in the docker container and access it from host.

# How to create a dockerfile?
  - Refer dockerfile in this directory

# How to create an image using dockerfile?
 - Go to directory where dockerfile resides
 - Run command: docker build -t bootstrap-static-page .

# How to do port mapping between host and container and run the container image
 - docker run -dp 3001:80 bootstrap-static-page

