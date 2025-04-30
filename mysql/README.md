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
