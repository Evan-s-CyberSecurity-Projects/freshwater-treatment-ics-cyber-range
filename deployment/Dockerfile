# Use a slim Python base image
FROM python:3.10-slim

# Set working directory inside container
WORKDIR /app

# Copy required files explicitly
COPY gns3-project-deploy.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY ???-build.py /app/
COPY requirements.txt /app/
COPY project-id /app/
COPY datastore /app/
# Explicitly rename deploy_gns3_course.py to deploy-gns3-course.py upon copying
COPY ???
COPY ???
COPY ???

COPY scada/freshwater_treatment /app/scada/freshwater_treatment
COPY scada/templates/diagrams /app/scada/templates/diagrams
# Optional: install system utilities
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        curl \
        iputils-ping \
        && rm -rf /var/lib/apt/lists/*

# Install Python dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Default command
CMD ["python3", "???"]
