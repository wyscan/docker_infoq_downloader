# Docker Infoq Downloader

## Purpose
I love InfoQ presentations but I commute to work on a bus with relatively bad WiFi.  I'm lucky enough to have someone else do the heavy lifing of writing an InfoQ presentation downloader for me.  Unfortunately I don't like installing things on my host machine if I can help it (Docker is obviously an exception to this rule).

There are other Docker images that attempt to solve this exact problem in exactly the same way but sadly I couldn't get them to work.  I think it's an issue with the naming of their containers.  So instead I created this is project.  It creates a Docker container that encapsulates the Python script for an InfoQ presentation downloader.  The project for the downloader itself is not mine and can be found at https://github.com/mtayseer/infoq-downloader

## Usage
Assuming you have Docker installed on your machine you can simply point to my container on [Docker Hub](https://registry.hub.docker.com/u/wyscan/docker_infoq_downloader/), provide a location to store the download on your host machine (remember this directory must actually exist), and provide the URL of the presentation you'd like to download.  For example:

```
docker run -v ~/Downloads/infoq:/data wyscan/docker_infoq_downloader \
http://www.infoq.com/presentations/problems-distributed-systems 
```

Once the download completes you'll see a subdirectory within ~/Downloads/infoq containing the presentation.  You can now enjoy it offline in a web browser.  In my case that means copying it to my phone or tablet and then having a more productive bus ride.
