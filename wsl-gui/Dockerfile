FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y
RUN apt-get update && \
    apt-get install -y git python3 python3-pip x11-apps

# グループとユーザーを作成（IDを指定）
RUN groupadd -g 1000 code-ip && \
    useradd -u 1000 -g code-ip -m code-ip

USER code-ip
WORKDIR /home/code-ip

RUN pip install open-interpreter==0.1.5
RUN pip install numpy matplotlib pandas

