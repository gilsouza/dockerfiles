# Run with display in fedora
# docker run -it --rm -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY

# Run with display in ubuntu
# docker run -ti --rm -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=$DISPLAY 


FROM ubuntu
MAINTAINER Gilmar Souza "gilmarcs@gmail.com"

RUN apt-get update -y && apt-get upgrade -y && \
	apt-get install --no-install-recommends -y -q unzip curl python build-essential git ca-certificates software-properties-common && \
	add-apt-repository ppa:webupd8team/java -y && \
    apt-get update && \
    echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | /usr/bin/debconf-set-selections && \
    apt-get install -y oracle-java8-installer libxext-dev libxrender-dev libxtst-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    rm -rf /tmp/* && \
    mkdir ~/dev/

#RUN apt-get update && apt-get install -y libgtk2.0-0 libcanberra-gtk-module

CMD [ "bash" ]