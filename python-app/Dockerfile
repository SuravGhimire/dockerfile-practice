FROM python:3.15-slim

WORKDIR /app

# Install dependencies first to leverage Docker's build cache
COPY requirements.txt .


#Add --no-cache-dir to pip. Running pip install --no-cache-dir -r requirements.txt prevents pip from saving downloaded wheel files inside the image layers
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

EXPOSE 5000

ENTRYPOINT ["python", "app.py"]

