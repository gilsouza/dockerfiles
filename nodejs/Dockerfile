FROM node

RUN apt-get update && apt-get upgrade -y \
  && npm install -g forever \
  && npm install -g grunt-cli \
  && npm install -g bower \
  && npm install -g browser-sync \
  && npm install -g express-generator

EXPOSE 3000 3001
CMD [ "bash" ]
