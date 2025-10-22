FROM ubuntu:22.04

RUN apt-get update

RUN apt-get install -y python3-dev python3-pip software-properties-common

RUN pip3 install --upgrade pip

ENV PATH="$PATH:~/.local/bin"

RUN pip3 install --user sciunit2 --break-system-packages

COPY files/utility/test_sciunit.sh /test_sciunit.sh
RUN chmod +x /test_sciunit.sh

CMD ["bash"]