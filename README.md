# docker-workshop
Simple static app and Dockerfile for use in Docker Workshop.  Example taken from Docker Beginner Lab (https://docs.docker.com/samples/)

## Commands you'll need
Create the image:
`docker build . -t workshop-image`
What it means: Create an image called `workshop-image` using the current directory as the context with the file called `Dockerfile` as the Dockerfile (default).

Run the image as a container:
`docker run --rm -p 8080:80 workshop-image`
What it means: run the `workshop-image` docker image and forward port 8080 of the host to 80 on the container.  This lets us browse the content being served.

If the Dockerfile is valid you should now be able to browse localhost:8080 in your browser to see the website being served

## Background information
This is an example of a static website described in HTML.  The website is intended to be served with NGINX 1.17.4 mainline.
This container allows us to run the website without installing or configuring NGINX on our Docker host
