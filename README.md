Docker Infoq Downloader

Encapsulates the Python script for an InfoQ presentation downloader found at https://github.com/mtayseer/infoq-downloader

Assuming you have docker installed on your machine you can download an InfoQ presentation like so:

```
docker run -v ~/Downloads/infoq:/data wyscan/docker_infoq_downloader http://www.infoq.com/presentations/problems-distributed-systems 
```