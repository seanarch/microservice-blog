FROM node:alpine 

# Add the following lines to workaround two potential issues running react in kubernetes cluster
ENV CI=true
ENV WDS_SOCKET_PORT=0

WORKDIR /app
COPY package.json ./ 
RUN npm install 
COPY ./ ./ 

CMD ["npm", "start"]