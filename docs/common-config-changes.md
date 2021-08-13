# Common changes to the project configuration

## Passing AWS credentials to the container

Add a new entry to the `volumes` section of `docker-compose.yml`

```yaml
- type: volume
  source: $HOME/.aws/credentials
  target: /home/app/.aws/credentials
  readonly: true
```

## Adding local database containers

