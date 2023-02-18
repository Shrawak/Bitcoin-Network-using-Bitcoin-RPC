FROM ruimarinho/bitcoin-core:latest
RUN apt update -y
RUN apt install -y python3-pip
RUN pip3 install notebook
RUN mkdir /code
ADD "bitcoin-rpc.ipynb" /code/
WORKDIR /code
CMD ["jupyter","notebook", "--ip", "0.0.0.0","--no-browser","--allow-root"]