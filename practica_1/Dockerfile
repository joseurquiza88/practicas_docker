FROM python:3.13-slim

WORKDIR /app

COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt
# Quedate ejecutándote aunque no tengas una aplicación que arrancar.
CMD ["tail", "-f", "/dev/null"] 