FROM lscr.io/linuxserver/code-server:latest

# Install markdown plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension DavidAnson.vscode-markdownlint

# Install terraform plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension hashicorp.terraform

# Install python plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-python.python
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-python.vscode-pylance
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension njpwerner.autodocstring

# Install jupyter plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-toolsai.jupyter
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-toolsai.jupyter-renderers
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-toolsai.vscode-jupyter-cell-tags
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-toolsai.vscode-jupyter-slideshow

# Install go plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension golang.go

# Install image preview
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension kisstkondoros.vscode-gutter-preview

# Install makefile plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-vscode.makefile-tools

# Install Dev container plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension ms-azuretools.vscode-docker

# Install Rapid api plugins
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension RapidAPI.vscode-rapidapi-client
RUN /app/code-server/bin/code-server --extensions-dir /config/extensions --install-extension rapidapi.vscode-services

# Install golang
RUN curl -L -sS 'https://go.dev/dl/go1.20.6.linux-amd64.tar.gz' --output /tmp/go.tar.gz && tar -C /usr/local -xzf /tmp/go.tar.gz && rm -f /tmp/go.tar.gz
RUN echo 'export PATH=$PATH:/usr/local/go/bin' >> /etc/profile
RUN /usr/local/go/bin/go install -v golang.org/x/tools/gopls@latest

# Install python
RUN DEBIAN_FRONTEND=noninteractive apt update && apt install -y python3 python3-pip
