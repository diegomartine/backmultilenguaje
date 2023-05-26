FROM node:12

ENV tmp_dir /tmp

RUN npm install -g json-server

RUN echo '{"articulos":[{"id":1,"ref":"PROD-001","nombre":"corsa", "descript": "carro corsa", "precio": 1500, "taxes": 0.19}], "pedidos":[{"id": 1, "products": [{"id": 1, "ref": "PROD-001", "nombre": "corsa", "cant": 1}], "precio": 1500, "total": 1785}]}' > /tmp/db.json

ENTRYPOINT ["json-server", "--port", "8080", "--host", "0.0.0.0"]

CMD ["/tmp/db.json"]

