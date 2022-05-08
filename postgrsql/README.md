

### POSTGRSQL & PGADMIN  Kullanım

```
docker run -p 5432:5432  --name postg -e POSTGRES_PASSWORD="admin"  -v /opt/postgr/data/:/var/lib/postgrsql/data -d postgres


docker run -p 5050:80 --link postg -e "PGADMIN_DEFAULT_EMAIL=admin@admin.com" -e "PGADMIN_DEFAULT_PASSWORD=admin"  -d dpage/pgadmin4
```

#### Pgadminden bağlantı için:
docker inspect <container id> | grep IPAddress
host:ip adress
maintanence databases:postgres
username:postgres

### ÇALIŞAN CONTAINER İÇİNE GİRMEK:

```
docker exec -it 2f psql -U postgres

-it: intereactive terminal
-2f: container id
psql -U postgres:container içindeki postgres veritabanına -U ile verilen Username ile bağlan
```

### TERMİNAL EKRANI KULLANMA:

```
dvd=# \list :Veritabanlarını listeler
postgres-# \connect dvd : dvd veritabanına bağlan(mysql use gibi)
dvd-# \dt  : tabloları listele
dvd-# \d actor :actor tablosunun içeriğini göster

NOT: Eğer komutlar sonuna ; koymazsak, veritabanından sonra - işareti komutun hala bitmediğini ve devamının beklendiğini söyler. = çıkarsa komut bitmiştir.

ÖRNEĞİN:

dvd=# SELECT *
dvd-# FROM actor
dvd-# WHERE first_name LIKE 'T%'
dvd-# ;
 actor_id | first_name | last_name |      last_update       
----------+------------+-----------+------------------------
       32 | Tim        | Hackman   | 2013-05-26 14:47:57.62
       38 | Tom        | Mckellen  | 2013-05-26 14:47:57.62
       42 | Tom        | Miranda   | 2013-05-26 14:47:57.62
      200 | Thora      | Temple    | 2013-05-26 14:47:57.62
(4 rows)

dvd=# 

```