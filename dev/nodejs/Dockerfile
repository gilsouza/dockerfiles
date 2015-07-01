FROM node
MAINTAINER Gilmar Souza "gilmarcs@gmail.com"

RUN apt-get update -y && apt-get install sudo -y -q --no-install-recommends && \
  npm install -g \
  bower \
  browser-sync \
  cordova \
  express-generator \
  grunt-cli \
  gulp \
  pm2 \
  yo \
  	generator-gulp-webapp \

  && apt-get clean && \
  	 rm -rf /var/lib/apt/lists/* && \
	 rm -rf /tmp/* \

  && mkdir -p /home/developer && \
     echo "developer:x:1000:1000:Developer,,,:/home/developer:/bin/bash" >> /etc/passwd && \
     echo "developer:x:1000:" >> /etc/group && \
     echo "developer ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/developer && \
     chmod 0440 /etc/sudoers.d/developer && \
     chown developer:developer -R /home/developer && \
     chown root:root /usr/bin/sudo && chmod 4755 /usr/bin/sudo

USER developer
ENV HOME /home/developer
WORKDIR /home/developer

EXPOSE 3000 3001 8080 80
CMD [ "bash" ]