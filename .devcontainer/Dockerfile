# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/codespaces-linux/.devcontainer/base.Dockerfile

#FROM mcr.microsoft.com/vscode/devcontainers/universal:1-focal
FROM registry.redhat.io/ansible-automation-platform-21/ee-minimal-rhel8:latest

#ADD krb5.conf /etc/krb5.conf.d/dekalb-domain
USER root
RUN yum install vim
RUN echo $'[libdefaults]' > cat /usr/share/crypto-policies/DEFAULT/krb5.txt
RUN echo $'permitted_enctypes = rc4-hmac des-cbc-crc des-cbc-md5' >> cat /usr/share/crypto-policies/DEFAULT/krb5.txt
RUN echo $'allow_weak_crypto = true' >> cat /usr/share/crypto-policies/DEFAULT/krb5.txt