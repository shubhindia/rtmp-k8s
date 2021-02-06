FROM node:alpine

LABEL maintainer="shubhindia <shubhindia123@gmail.com>"
WORKDIR /usr/app
# Install netcat for port checking
RUN apk add --update netcat-openbsd
RUN apk add ffmpeg
# Install some dependencies
COPY ./package.json ./
RUN npm install
COPY ./ ./
EXPOSE 1935 8000
CMD ["npm", "start"]
