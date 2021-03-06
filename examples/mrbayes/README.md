# MrBayes Docker Image

Docker image for [MrBayes](http://mrbayes.sourceforge.net/) based on the [ubuntu:14.04](https://hub.docker.com/r/library/ubuntu/tags/14.04/) Docker image.

## Local Usage

Gaining shell access:

```sh
docker run --rm -ti grycap/mrbayes /bin/bash
```

A sample execution can be initiated with:

```sh
docker run --rm -ti grycap/mrbayes /tmp/mrbayes-sample-run.sh
```

## Usage in AWS Lambda via SCAR

You can run this image in AWS Lambda via [SCAR](https://github.com/grycap/scar) using the following procedure:

1. Create the Lambda function

 ```sh
 scar init -n lambda-mrbayes -i grycap/mrbayes
 ```

2. Execute the Lambda function passing an execution script

 ```sh
 scar run -s examples/mrbayes/mrbayes-sample-run.sh -n lambda-mrbayes
 ```

