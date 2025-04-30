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

## 3. Script for database backup
```bash
CURRENT_DATE=$(date +"%Y-%m-%d-%H-%M-%S")
BAKCUP_LOCATION="/var/www/database/backup"
if [ ! -d "$BAKCUP_LOCATION" ]; then
    mkdir -p $BAKCUP_LOCATION
fi
rm -rf $BAKCUP_LOCATION/* && /usr/bin/mysqldump -uDATABASE_USER -pDATABASE_PASSWORD DATABASE_NAME > $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.sql
tar -czvf $BAKCUP_LOCATION/DATABASE_NAME_$CURRENT_DATE.tar.gz -C $BAKCUP_LOCATION .
```
