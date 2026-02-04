# promptfoo-tests - Node.js Testing
FROM node:22-alpine

WORKDIR /app

# Copy package.json and test files
COPY package.json .
COPY *.yaml .

# Add overrides to fix vulnerable transitive dependencies and install locally
RUN npm pkg set overrides.glob=11.1.0 && \
    npm pkg set overrides.tar=7.5.7 && \
    npm pkg set dependencies.promptfoo=latest && \
    npm install

# Add node_modules/.bin to PATH for promptfoo
ENV PATH="/app/node_modules/.bin:$PATH"

# Expose port for promptfoo view command
EXPOSE 15500

# Default command runs all evaluations
CMD ["npm", "run", "eval"]
