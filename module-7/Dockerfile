FROM node:13-alpine
ENV MONGO_DB_USERNAME=admin \
	MONGO_DB_PWD=password

RUN mkdir -p home/app %%run {os commands}%%

COPY ./developing-with-docker/app /home/app

# set default dir so that next commands executes in /home/app dir
WORKDIR /home/app

# will execute npm install in /home/app because of WORKDIR
RUN npm install

CMD ["node", "/home/app/server.js"]