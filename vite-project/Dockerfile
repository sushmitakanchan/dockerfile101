# use an official image of Node.js runtime
FROM node:20-alpine

# set the working directory inside the container
WORKDIR /app

COPY package*.json ./
# copying all the package and package-lock json into the current dir

# Difference between run and CMD command
#run executes at build time
#CMD executes at container run time

# install dependancies
RUN npm install

COPY . .
# first dot is current folder and second WORKDIR

EXPOSE 5173

CMD [ "npm" , "run", "dev" ]

# docker build -t <img_name> - creating an image
# docker run -p 5173:5173 <img_name>- running an image// port mapping: hostmachine:containermachine
# if there is any changes need to create img again