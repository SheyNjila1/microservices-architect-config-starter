FROM node:14-alpine  
WORKDIR /app  
COPY package*.json ./  
RUN npm install  
COPY . .  
EXPOSE 8080 
CMD ["npm", "start"]  


# FROM node:8
# WORKDIR /app
# COPY . .
# RUN npm install
# EXPOSE 8080
# CMD ["npm","start"]
