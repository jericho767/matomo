# base image
FROM nikolaik/python-nodejs:python3.10-nodejs14-slim

# Set working directory
WORKDIR /var/www/matomo

ENV PATH /var/www/matomo/node_modules/.bin:$PATH

COPY . /var/www/matomo

EXPOSE 3000

RUN npm init --yes
RUN npm install -g react-scripts
RUN npm install --save

CMD ["npm", "--", "start"]
