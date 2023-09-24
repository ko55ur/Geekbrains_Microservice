FROM python:3.9

COPY ./python/requirements.txt .

RUN pip install --user -r requirements.txt

WORKDIR /app

COPY ./python/app.py /app
RUN adduser --system --group worker
ENV PATH=/home/worker/.local:$PATH
CMD [ "python", "./app.py"]
EXPOSE 8080
