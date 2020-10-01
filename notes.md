# Random Notes

- Submodule issues in git: `rm --cashed <directory-name>`
- Move all the content of a directory up one level: `mv filename/* .` (Be in the outer directory then run the command with the file name of the nested directory)
- GraphQL - an alternative to a REST API


### Postgres Smash
- $ brew update
- $ brew uninstall postgresql
- $ rm -rf /usr/local/var/postgres
- $ rm -rf .psql_history .psqlrc .psql.local .pgpass .psqlrc.local
- $ brew list
- Make sure postgresql is not in that list, if it is, repeat the above commands
- $ brew install postgres
- $ brew services start postgresql
