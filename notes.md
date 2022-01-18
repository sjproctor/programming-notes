# Random Notes

- Submodule issues in git: `git rm --cashed <directory-name>`
- Move all the content of a directory up one level: `mv filename/* .` (Be in the outer directory then run the command with the file name of the nested directory)
- GraphQL - an alternative to a REST API
- Emojis take up the space of two characters

### Printing Git Tree
```bash
logr = “log --pretty=format:‘%h %s <= %an, %ar’ --graph”
lola = “log --graph --decorate --pretty=oneline --abbrev-commit --all”
```

### Terminal Shortcuts
- $ control + u - clear whole line of text in terminal
- $ control + a - move to the beginning of the line in terminal

### Postgres Smash
- $ brew update
- $ brew uninstall postgresql
- $ rm -rf /usr/local/var/postgres
- $ rm -rf .psql_history .psqlrc .psql.local .pgpass .psqlrc.local
- $ brew list
- Make sure postgresql is not in that list, if it is, repeat the above commands
- $ brew install postgres
- $ brew services start postgresql
