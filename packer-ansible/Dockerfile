ARG PACKER_VERSION

FROM hashicorp/packer:${PACKER_VERSION}
LABEL maintainer="Mihir Mone <monemihir@hotmail.com>"

RUN alpine -v && \
  apk --no-cache add ansible py-pip py-boto && \
  pip install pywinrm && \
  apk --no-cache add docker openrc && \
  rc-update add docker boot

RUN ansible --version
COPY ansible.cfg /etc/ansible

# Packer needs this set:
# https://github.com/mitchellh/packer/blob/49067e732a66c9f7a87843a2c91100de112b21cc/provisioner/ansible/provisioner.go#L127
ENV USER root
