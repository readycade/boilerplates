## Common MySQL Commands

##### show all users
```mysql
SELECT user, host FROM mysql.user;
```

##### create user at localhost
```mysql
CREATE USER 'wordpress'@'localhost' IDENTIFIED BY 'yourpassword';
```

##### grant privledges
```mysql
GRANT ALL PRIVILEGES ON wordpress.* TO 'wordpress'@'localhost';
```

```mysql
FLUSH PRIVILEGES;
```

```mysql
SHOW GRANTS FOR 'wordpress'@'localhost';
```

```mysql
REVOKE ALL PRIVILEGES ON wordpress.* FROM 'wordpress'@'localhost';
```

```mysql
CREATE USER 'wordpress'@'localhost' IDENTIFIED BY 'youruserPASSWORD';
```
