FROM scratch
ADD ubuntu-7.10-root.tar.xz /
COPY sources.list /etc/apt/sources.list
RUN apt-get update && apt-get upgrade -y
CMD ["/bin/bash"]
