# llm-frontend-python - Flask Frontend
FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .

# Upgrade vulnerable packages to fixed versions
RUN pip install --no-cache-dir --upgrade pip wheel>=0.46.2 jaraco.context>=6.1.0

RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Expose port
EXPOSE 5000

# Set environment variables
ENV FLASK_PORT=5000
ENV FLASK_DEBUG=false

# Run the application
CMD ["python", "app.py"]
