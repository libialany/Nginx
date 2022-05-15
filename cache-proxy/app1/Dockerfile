FROM python:3.7-alpine
COPY ./requirements.txt /requirements.txt
WORKDIR /
RUN pip install -r requirements.txt
COPY . /
RUN addgroup -S groupcache && adduser -S usercache -G groupcache
USER usercache
ENTRYPOINT ["python3"]
CMD ["app.py"]
