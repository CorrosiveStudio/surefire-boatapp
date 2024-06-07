FROM node:22-bullseye

WORKDIR /src

# Copy package.json and yarn.lock files
COPY package.json yarn.lock ./

# Install dependencies
RUN yarn install --production=false

# Expose the port your app runs on
EXPOSE 8100

# Set environment variable for Nuxt port
ENV NUXT_PORT 8100

# Copy the rest of your application's code
COPY . /src/

# You might not need to adjust the PATH if using global yarn installs
ENV PATH /src/node_modules/.bin:$PATH

# Set the Docker entrypoint and default command
ENTRYPOINT ["/src/docker-entrypoint.sh"]
CMD ["yarn", "dev", "--host", "0.0.0.0"]
