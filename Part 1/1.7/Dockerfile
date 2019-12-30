FROM ubuntu

RUN apt-get update && apt-get install -y curl

COPY scriptfile .

CMD ["/bin/bash", "scriptfile"]