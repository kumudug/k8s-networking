FROM node:14-alpine

WORKDIR /app

COPY package.json .

RUN npm install

COPY . .

# Set build time argument
ARG DEFAULT_PORT=8000

# Set environment variable which can then be used in server.js
# The default value 8000 can be overriden during image creation in command line
ENV PORT $DEFAULT_PORT 

ARG DEFAULT_TASKS_FOLDER='\tasks'

ENV TASKS_FOLDER $DEFAULT_TASKS_FOLDER

EXPOSE $PORT

CMD [ "node", "tasks-app.js" ]