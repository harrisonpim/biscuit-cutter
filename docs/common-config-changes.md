# Common changes to the project configuration

## Passing AWS credentials to a container

Add a new entry to the `volumes` section of the relevant service in `docker-compose.yml`

```yaml
- type: volume
  source: $HOME/.aws/credentials
  target: /home/app/.aws/credentials
  readonly: true
```
