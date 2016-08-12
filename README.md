# What is dionaea?

dionaea is a low interaction honeypot.

# How to use this image.

### Create a `Dockerfile` in your project

```dockerfile
FROM dionae:0.5
COPY conf/your-service.conf /opt/dionaea/etc/dionaea/services/
COPY conf/your-ihandler.conf /opt/dionaea/etc/dionaea/ihandlers/
```

Then, run the commands to build and run the Docker image:

```console
docker build -t my-dionaea
docker run -it --rm my-dionaea
```

### Configuration

If you don't want to include a `Dockerfile` in your project, it is sufficient to do the following:

```console
$ docker run -it --rm -v "$PWD/etc":/opt/dionaea/etc/dionaea dionaea:0.5
```
