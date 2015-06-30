FROM node

RUN apt-get update -y && apt-get upgrade -y \
#  && npm install -g forever \
  && npm install -g pm2 \ 
  && npm install -g grunt-cli \
  && npm install -g bower \
  && npm install -g browser-sync \
  && npm install -g express-generator

EXPOSE 3000 3001
CMD [ "bash" ]
