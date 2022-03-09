# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/codespaces-linux/.devcontainer/base.Dockerfile

#FROM mcr.microsoft.com/vscode/devcontainers/universal:1-focal
FROM registry.redhat.io/ubi8/ubi:latest

RUN yum install vim
RUN mv /usr/share/crypto-policies/DEFAULT/krb5.txt /usr/share/crtypo-policies/DEFAULT/krb5.orig
COPY krb5.txt /usr/share/crtypo-policies/DEFAULT/krb5.txt