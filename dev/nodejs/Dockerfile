FROM node
MAINTAINER Gilmar Souza "gilmarcs@gmail.com"

RUN apt-get update -y && \
  npm install -g \
  bower \
  browser-sync \
  express-generator
  grunt-cli \
  pm2

RUN chmod +x /usr/local/bin/eclipse && \
    mkdir -p /home/developer && \
    echo "developer:x:1000:1000:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
    echo "developer:x:1000:" >> /etc/group && \
    echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
    chmod 0440 /etc/sudoers.d/developer && \
    chown developer:developer -R /home/developer && \
    chown root:root /usr/bin/sudo && chmod 4755 /usr/bin/sudo

USER developer
ENV HOME /home/developer
WORKDIR /home/developer

EXPOSE 3000 3001
CMD [ "bash" ]