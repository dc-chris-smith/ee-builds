# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/codespaces-linux/.devcontainer/base.Dockerfile

FROM mcr.microsoft.com/vscode/devcontainers/universal:1-focal

# ** [Optional] Uncomment this section to install additional packages. **
USER root
#
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
#
# USER codespace
COPY krb5.conf /etc/krb5.conf
RUN rm -f /etc/krb5.conf.d/crypto-policies