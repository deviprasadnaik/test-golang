FROM google/cloud-sdk:alpine
RUN cd /tmp \
 && curl https://download.docker.com/linux/static/stable/x86_64/docker-17.09.0-ce.tgz -o docker.tgz \
 && tar xzvf docker.tgz \
 && mv docker/docker /usr/bin/docker \
 && chmod +x /usr/bin/docker

RUN cd /tmp \
 && curl https://releases.hashicorp.com/terraform/0.13.5/terraform_0.13.5_linux_amd64.zip -o terraform.zip \
 && unzip terraform.zip \
 && mv terraform /usr/bin/terraform \
 && chmod a+x /usr/bin/terraform

RUN apk update \
  && apk add jq

RUN gcloud components install kubectl
