FROM node:20-alpine 

WORKDIR /placement_tracker_web

COPY . .

ARG BACKEND_URL

ENV NEXT_PUBLIC_URL=$BACKEND_URL

RUN npm ci

EXPOSE 3000

RUN npm run build

CMD ["npm","run","start"]

