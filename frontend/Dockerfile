#Stage-1 Build
FROM node:22 AS builder 

#Creates a Work DIR named /app
WORKDIR /app

#Dependencies
COPY package*.json ./

#Install node modules
RUN npm install

# Copies are other files
COPY . .

#Creates dist/
RUN npm run build 

#Stage-2 Nignx for serving the staic files
FROM nginx:alpine

#copy custom nginx configuration proxies/api requests to backend)
COPY nginx/default.conf /etc/nginx/conf.d/default.conf

# Copy buit react application from builder stage
COPY --from=builder /app/dist /usr/share/nginx/html

#Nginx runs on port 80
EXPOSE 80
