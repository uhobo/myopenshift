FROM registry.access.redhat.com/ubi8/nodejs-16

WORKDIR /app

# Switch to non-root user for npm install if possible (depends on base image permissions)
USER 1001

# copy packge.json to the workdir
COPY package*.json ./


# install npm dependencies
RUN npm install

# Copy application file to the 
COPY Application/src .

# create local env varibel for the PORT
ENV PORT 8080

USER 1001

EXPOSE 8080
CMD [ "node", "app.js" ]