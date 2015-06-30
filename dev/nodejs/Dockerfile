FROM node

RUN apt-get update -y && \
  npm install -g \
  bower \
  browser-sync \
  express-generator
  grunt-cli \
  pm2 \

RUN mkdir /home/dev/

VOLUME ["/home/dev"] 

EXPOSE 3000 3001
CMD [ "bash" ]