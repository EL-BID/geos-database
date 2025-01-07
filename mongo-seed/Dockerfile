FROM mongo:4.2.12

COPY database/guia_edutec /guia_edutec_v2
CMD  mongorestore --host=mongo --db=guia_edutec_v2 -u admin -p abc123 /guia_edutec_v2 --gzip --drop --authenticationDatabase=admin