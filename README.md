# dev-tools

Set of dockerfiles to create different portable development environment to access via docker.

It requires docker and docker-compose.

## vscode

Visual Studio Code + plugins.

It's mostly based in [https://hub.docker.com/r/linuxserver/code-server](https://hub.docker.com/r/linuxserver/code-server) from [linuxserver.io](https://www.linuxserver.io/).

Once started it can be accessed using a browser: [http://localhost:9000](http://localhost:9000)

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

## terraform

Visual Studio Code + plugins + terraform + terragrunt + tflint

Once started it can be accessed using a browser: [http://localhost:9001](http://localhost:9001)

Set proper variables in docker-compose.yaml. Dockerfile includes vscode plugins for Markdown and terraform.

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

### vscode issues

- disable welcome page.
- set configuration parametters from console.
- set dark mode.

### terraform issues

- add *vscode* as part of the UI
