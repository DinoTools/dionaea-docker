# What is dionaea?

dionaea is a low interaction honeypot.
The code from the [official dionaea repository](https://github.com/DinoTools/dionaea) is used to build the service during the image build process.

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

# User Feedback

## Issues

If you have any problems with or questions about this image, please create an [GitHub issue](https://github.com/DinoTools/dionaea-docker/issues).

## Contributing

You are invited to contribute new features, fixes or updates.
We recommend discussing your ideas through a [GitHub issue](https://github.com/DinoTools/dionaea-docker/issues), before you start.
