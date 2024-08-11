FROM node:20-alpine 

WORKDIR /placement_tracker_server

COPY . .

# Add ARG instructions for each environment variable
ARG DB_HOST
ARG DB_USER
ARG DB_PASSWORD
ARG DB_NAME
ARG MAIL_USER
ARG MAIL_PASSWORD
ARG SECRET_KEY

# Set ENV variables using the ARG values
ENV DB_HOST=$DB_HOST
ENV DB_USER=$DB_USER
ENV DB_PASSWORD=$DB_PASSWORD
ENV DB_NAME=$DB_NAME
ENV MAIL_USER=$MAIL_USER
ENV MAIL_PASSWORD=$MAIL_PASSWORD
ENV SECRET_KEY=$SECRET_KEY

RUN \
    npm ci && \
    npm cache clean --force 

EXPOSE 5000/tcp

CMD npm start