# deepeval-tests - Python Testing
FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .

# Upgrade vulnerable packages to fixed versions
RUN pip install --no-cache-dir --upgrade pip wheel>=0.46.2 jaraco.context>=6.1.0

RUN pip install --no-cache-dir -r requirements.txt

# Copy test files
COPY . .

# Default command runs deepeval tests
CMD ["deepeval", "test", "run"]
