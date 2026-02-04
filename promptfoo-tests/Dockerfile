# promptfoo-tests - Node.js Testing
FROM node:20-alpine

WORKDIR /app

# Copy package.json and test files
COPY package.json .
COPY *.yaml .

# Install promptfoo globally with fixed vulnerable dependencies
RUN npm install -g cross-spawn@7.0.5 glob@10.5.0 tar@7.5.7 promptfoo@latest

# Expose port for promptfoo view command
EXPOSE 15500

# Default command runs all evaluations
CMD ["npm", "run", "eval"]
