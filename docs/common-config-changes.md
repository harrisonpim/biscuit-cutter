# Common changes to the project configuration

## Passing AWS credentials to a container

Add a new entry to the `volumes` section of the relevant service in `docker-compose.yml`

```yml
- type: volume
  source: $HOME/.aws/credentials
  target: /home/app/.aws/credentials
  readonly: true
```

## Running on GPU

Modify the the core jupyter service to use the [cschranz/gpu-jupyter](https://github.com/iot-salzburg/gpu-jupyter/) image as a base instead.

Your dockerfile should look something like this

```dockerfile
FROM cschranz/gpu-jupyter

RUN pip install --upgrade pip pip-tools
COPY requirements.* .
RUN pip-compile requirements.* --output-file requirements.txt
RUN pip install -r requirements.txt

RUN rm -rf work requirements*
```

Note that this image is _very_ large (around 6GB, compared to the 800MB regular image) and will take some time to download and unpack. Keeping a cached version of this image somewhere easily accessible will save you time and money if you're planning to use this image on cloud GPUs.
