# FAPP / FreeBSD, Apache, PostgreSQL and PHP(PHPPgAdmin)
## Now apply template to container
```sh
bastille create fapp 14.1-RELEASE YourIP-Bastille
bastille bootstrap https://github.com/bastille-templates/fapp
bastille template fapp bastille-templates/fapp
```

## License
This project is licensed under the BSD-3-Clause license.