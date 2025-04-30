# Mysql Commands Cheatsheet

## 🖥️ Basic Commands

### 📁 `mysql` - Dump and import database

## 1. Dump databate and salve to file.sql
```mysql
mysqldump
```
## Example:
```mysql
mysqldump -u root -p database_name > database_name.sql
```

## 2. Import databate from salved file.sql
```mysql
mysql
```
## Example:
```mysql
mysql -u root -p database_name < database_name.sql
```
---
## Script for database backup
```bash
CURRENT_DATE=$(date +"%Y-%m-%d-%H-%M-%S")
BAKCUP_LOCATION="/var/www/database/backup"
if [ ! -d "$BAKCUP_LOCATION" ]; then
    mkdir -p $BAKCUP_LOCATION
fi
rm -rf $BAKCUP_LOCATION/* && /usr/bin/mysqldump -uDATABASE_USER -pDATABASE_PASSWORD DATABASE_NAME > $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.sql
tar -czvf $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.tar.gz -C $BAKCUP_LOCATION .
```
## Explanation. Define the current date format:
```bash
CURRENT_DATE=$(date +"%Y-%m-%d-%H-%M-%S")
```
This command assigns the current date and time to the variable `CURRENT_DATE`.

The format `"%Y-%m-%d-%H-%M-%S"` means:

- `%Y` = Year (4 digits)
- `%m` = Month (2 digits)
- `%d` = Day of the month (2 digits)
- `%H` = Hour (24-hour format)
- `%M` = Minute
- `%S` = Second

The resulting value of `CURRENT_DATE` will look like `2025-04-30-14-22-55`.

## Explanation. Define backup location:
```bash
BAKCUP_LOCATION="/var/www/database/backup"
```
This defines the backup location where the database dumps will be stored, in this case, /var/www/database/backup.

## Explanation. Check if the backup directory exists:
```bash
if [ ! -d "$BAKCUP_LOCATION" ]; then
    mkdir -p $BAKCUP_LOCATION
fi
```
- This checks whether the directory $BAKCUP_LOCATION exists (-d checks if the directory exists).

- If it doesn't exist ([ ! -d "$BAKCUP_LOCATION" ]), it creates the directory using mkdir -p. The -p option ensures that parent directories are created if they don't exist.

## Explanation. Remove any existing backups in the backup directory:
```bash
rm -rf $BAKCUP_LOCATION/*
```
- This command removes (rm) all files and directories inside the $BAKCUP_LOCATION directory.

- The -rf flags:
    - -r = Recursive, meaning it will remove directories and their contents.
    - -f = Force, meaning it will delete without prompting for confirmation.

## Explanation. Create a database dump:
```bash
/usr/bin/mysqldump -uDATABASE_USER -pDATABASE_PASSWORD DATABASE_NAME > $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.sql
```

## Explanation. This creates a backup (dump) of the MySQL database `DATABASE_NAME` using `mysqldump`.

- `-uDATABASE_USER` specifies the username for the database.
- `-pDATABASE_PASSWORD` specifies the password for the database (note: there should be no space between `-p` and the password).
- `DATABASE_NAME` is the name of the database to back up.

- The output is redirected (`>`) to a file named `DATABASE_NAME_$CURRENT_DATE.sql` in the backup directory. This creates a `.sql` file with the backup of the database.

## Explanation. Compress the backup:
```bash
tar -czvf $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.tar.gz -C $BAKCUP_LOCATION .
```
This creates a compressed `.tar.gz` archive of the backup files.

- `tar`: Used to create archives.
- `-c`: Create a new archive.
- `-z`: Compress the archive using gzip.
- `-v`: Verbose, meaning it will list the files being added to the archive.
- `-f`: Specifies the filename of the archive.
- `$BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.tar.gz`: The name of the output archive.
- `-C $BAKCUP_LOCATION`: Change to the `$BAKCUP_LOCATION` directory before creating the archive.
- `.`: Adds all files in the current directory (i.e., the backup directory) to the archive.

### Summary:
This script performs the following:

1. Sets the current date and time.
2. Defines the backup directory.
3. Checks if the backup directory exists and creates it if it doesn't.
4. Removes any existing files in the backup directory.
5. Dumps the MySQL database to a `.sql` file.
6. Compresses the `.sql` file into a `.tar.gz` archive for storage.

This approach ensures that each backup is uniquely named based on the timestamp, and the backup directory is clean before each new backup is created.

