
# Guia Edutec Repository - Open Source

## Database project

* [Technical Documentation](https://github.com/EL-BID/geos-database/blob/master/Documentaci%C3%B3n_T%C3%A9cnica_Guia_Edutec.pdf)

Access to other projects
* [Back-end](https://github.com/EL-BID/geos-backend)
* [Front-end](https://github.com/EL-BID/geos-frontend)


---
Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg

---
_The Guia Edutec was originally developed by CIEB. The process of opening the code has made possible by financial support of Fundación ProFuturo._


---

## Backup database commands

mongodump
No Auth : docker exec <mongodb container> sh -c 'mongodump --archive' > db.dump

Authenticated : docker exec <mongodb container> sh -c 'mongodump --authenticationDatabase admin -u <user> -p <password> --db <database> --archive' > db.dump

mongorestore
No Auth : docker exec -i <mongodb container> sh -c 'mongorestore --archive' < db.dump

Authenticated : docker exec -i <mongodb container> sh -c 'mongorestore --authenticationDatabase admin -u <user> -p <password> --db <database> --archive' < db.dump

