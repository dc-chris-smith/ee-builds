# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.209.6/containers/codespaces-linux/.devcontainer/base.Dockerfile

FROM mcr.microsoft.com/vscode/devcontainers/universal:1-focal

# ** [Optional] Uncomment this section to install additional packages. **
USER root
#
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
#
# USER codespace
RUN echo $'# To opt out of the system crypto-policies configuration of krb5, remove the \n\
# symlink at /etc/krb5.conf.d/crypto-policies which will not be recreated. \n\
# includedir /etc/krb5.conf.d/ \n\
 \n\
[logging] \n\
    default = FILE:/var/log/krb5libs.log \n\
    kdc = FILE:/var/log/krb5kdc.log \n\
    admin_server = FILE:/var/log/kadmind.log \n\
 \n\
[libdefaults] \n\
    dns_lookup_realm = false \n\
    dns_lookup_kdc = true \n\
    ticket_lifetime = 24h \n\
    renew_lifetime = 7d \n\
    forwardable = true \n\
    rdns = false \n\
    pkinit_anchors = FILE:/etc/pki/tls/certs/ca-bundle.crt \n\
    spake_preauth_groups = edwards25519 \n\
    default_realm = DCG.DEKALB.LOC \n\
    default_ccache_name = KEYRING:persistent:%{uid} \n\
    default_tgs_enctypes = rc4-hmac des-cbc-crc des-cbc-md5 \n\
    default_tkt_enctypes rc4-hmac des-cbc-crc des-cbc-md5 \n\
    permitted_enctypes = rc4-hmac des-cbc-crc des-cbc-md5 \n\
    allow_weak_crypto = true \n\
 \n\
[realms] \n\
DCG.DEKALB.LOC = { \n\
    kdc = kerberos.DCG.DEKALB.LOC \n\
    admin_server = kerberos.DCG.DEKALB.LOC \n\
    default_domain = DCG.DEKALB.LOC \n\
} \n\
 \n\
[domain_realm] \n\
.dcg.dekalb.loc = DCG.DEKALB.LOC \n\
dcg.dekalb.loc = DCG.DEKALB.LOC \n\' > ~/krb5.conf