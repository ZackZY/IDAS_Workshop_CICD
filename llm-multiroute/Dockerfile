# llm-multiroute - FastAPI Backend
FROM python:3.11-slim

WORKDIR /app

# Install dependencies
COPY requirements.txt .

# Upgrade vulnerable packages to fixed versions
RUN pip install --no-cache-dir --upgrade pip wheel>=0.46.2 jaraco.context>=6.1.0 starlette>=0.40.0

RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY . .

# Expose port
EXPOSE 8082

# Run the application
CMD ["uvicorn", "app.main:app", "--host", "0.0.0.0", "--port", "8082"]
