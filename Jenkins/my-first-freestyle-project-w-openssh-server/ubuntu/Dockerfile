FROM ubuntu:latest

RUN apt update && apt install  openssh-server sudo -y

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test 
# RUN echo "user_name:password" | chpasswd
RUN  echo 'test:test' | chpasswd

RUN ssh-keygen -A

RUN service ssh start

EXPOSE 2222

CMD ["/usr/sbin/sshd","-D"]