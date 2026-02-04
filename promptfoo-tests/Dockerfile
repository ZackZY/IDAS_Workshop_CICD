# promptfoo-tests - Node.js Testing
FROM node:20-alpine

WORKDIR /app

# Copy package.json and test files
COPY package.json .
COPY *.yaml .

# Install promptfoo globally for faster execution
RUN npm install -g promptfoo@latest

# Expose port for promptfoo view command
EXPOSE 15500

# Default command runs all evaluations
CMD ["npm", "run", "eval"]
