FROM lscr.io/linuxserver/webtop:debian-xfce

# Install required tools
RUN DEBIAN_FRONTEND=noninteractive apt update && apt install -y curl unzip vim

# Install terraform
RUN curl -L -sS https://releases.hashicorp.com/terraform/1.5.4/terraform_1.5.4_linux_amd64.zip \
    --output /tmp/terraform.zip && \
    unzip -x -d /usr/local/bin/ /tmp/terraform.zip && \
    rm -f /tmp/terraform.zip

# Install terragrunt
RUN curl -L -sS https://github.com/gruntwork-io/terragrunt/releases/download/v0.48.5/terragrunt_linux_amd64 \
    --output /usr/local/bin/terragrunt && \
    /bin/chmod +x /usr/local/bin/terragrunt

RUN curl -L -sS https://raw.githubusercontent.com/terraform-linters/tflint/master/install_linux.sh | bash
