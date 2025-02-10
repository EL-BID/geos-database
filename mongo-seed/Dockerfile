FROM mongo:4.2.12

COPY database/guia_edutec /guia_edutec
CMD  mongorestore --host=mongo --db=guia_edutec -u admin -p abc123 /guia_edutec --gzip --drop --authenticationDatabase=admin