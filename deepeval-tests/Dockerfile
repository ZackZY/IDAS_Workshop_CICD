# deepeval-tests - Python Testing
FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy test files
COPY . .

# Default command runs deepeval tests
CMD ["deepeval", "test", "run"]
