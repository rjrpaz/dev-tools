# dev-tools

Set of dockerfiles to create different portable development environment to access via docker.

It requires docker and docker-compose.

## vscode

Visual Studio Code + plugins.

It's mostly based in [https://hub.docker.com/r/linuxserver/code-server](https://hub.docker.com/r/linuxserver/code-server) from [linuxserver.io](https://www.linuxserver.io/).

Once started it can be accessed using a browser: [http://localhost:8443](http://localhost:8443)

Set proper variables in docker-compose.yaml. Add any preferred vscode plugin in Dockerfile.

Build:

```bash
docker-compose build
```

Start:

```bash
docker-compose up -d
```

Stop:

```bash
docker-compose down
```

## TODO

- vscode: disable welcome page.

- vscode: set configuration parametters from console.

- vscode: set dark mode.
