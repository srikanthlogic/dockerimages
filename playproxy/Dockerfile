FROM beevelop/nodejs-python

WORKDIR /usr/src/app/google-play-api


RUN apt-get update -y && apt-get --assume-yes install npm git && \
    ln -s /usr/bin/nodejs /usr/bin/node && \
    cd /usr/src/app && \
    git clone https://github.com/srikanthlogic/google-play-api.git && \
    cd google-play-api && \
    npm install && \
    rm -rf /var/lib/apt/lists/* && \
    apt-get clean

COPY . .

EXPOSE 3000

CMD ["npm", "start"]
