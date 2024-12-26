# FAPP / FreeBSD, Apache, PostgreSQL and PHP(PHPPgAdmin)
## Now apply template to container
```sh
bastille create fapp 14.1-RELEASE YourIP-Bastille
bastille bootstrap https://github.com/bastille-templates/fapp
bastille template fapp bastille-templates/fapp
```

## License
This project is licensed under the BSD-3-Clause license.

Change Password
```sh
# Password User System Account Management
root@www:~ # passwd postgres
Changing local password for postgres
New Password: psql
Retype New Password: psql
root@www:~ # su - postgres

# Change Password User postgres;
postgres@www:~ $ psql -c "ALTER USER postgres WITH PASSWORD 'yourpasswd'"

# Managemen User;
postgres@www:~ $ createuser admin -P
postgres@www:~ $ dropuser admin

# Managemen Database;
postgres@www:~ $ createdb testdb -O admin
postgres@www:~ $ dropdb testdb

# show users and databases
postgres@www:~ $ psql -c "select usename from pg_user;"
postgres@www:~ $ psql -l

# connect to testdb
postgres@www:~ $ psql testdb
```