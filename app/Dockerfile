FROM --platform=linux/amd64 python:3.10-slim

WORKDIR /app
RUN groupadd -r webservice && useradd --no-log-init -r -g webservice webservice
COPY . .
RUN chown -R webservice:webservice /app

RUN pip install --no-cache-dir -r requirements.txt

USER webservice:webservice

EXPOSE 8050

ENTRYPOINT ["python"]
CMD ["hello.py"]