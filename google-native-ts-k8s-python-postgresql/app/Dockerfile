FROM python:3.12.0b1-slim
RUN mkdir /opt/project
WORKDIR /opt/project
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY ./app ./app/
COPY ./VERSION.txt .
ENV PYTHONPATH "${PYTHONPATH}:/opt/project"
CMD ["python", "app/main.py"]
