FROM scratch
ADD ubuntu-6.06-root.tar.gz /
COPY sources.list /etc/apt/sources.list
RUN apt-get update && apt-get upgrade -y
CMD ["/bin/bash"]
