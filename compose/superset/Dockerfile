FROM apache/superset:9e5876dc1739dfca5c5ffd87719cb71bb2e20b91-dev

WORKDIR /app

COPY requirements/local.txt /requirements/local.txt

RUN pip install -r /requirements/local.txt

RUN superset fab create-admin --username admin --firstname Admin --lastname Admin --email admin@localhost --password admin && \
    superset db upgrade && \
    superset init
