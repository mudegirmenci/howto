
### Mysql & phpmyadmin birlikte kullanımı

#### 1-**mysql-server** çalıştıralım:

`docker run --name mysql-server -p 3306:3306 -e MYSQL_ROOT_PASSWORD=test123 -d mysql`

**Komut açıklamaları:**

```

--name: çalışan containerımıza isim veriyoruz.

-p 3306:3306 : 
mysql-server dışarıda 3306 ve içeride 3306 portundan çalışacak.

-e MYSQL_ROOT_PASSWORD=test123: 
mysql bağlantı şifresi test123 olacak.

-d mysql:
mysql docker image bir deamon olarak çalışacak.

```

#### 2-**phpmyadmin** çalıştıralım:

`docker run --name pmyadmin -p 8000:80 --link mysql-server:db -d phpmyadmin`

**Komut açıklamaları:**

```
 --link mysql-server:db ->mysql-server isimli container ile aynı ağda çalış. Bu şekilde mysql ile phpmyadmin 
 haberleşebiliyorlar.
```

tarayıcımızdan `localhost:800` yazarak **phpmyadmin** arayüzüne ulaşabiliriz.
