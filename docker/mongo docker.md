### Local bir uygulamanın docker container içindeki mongodb ile bağlantısı şu şekilde yapılır:

**Komut Açıklamaları:**
```
-p ile içeri ve dışarı port haberleşmeleri(port mapping)
--name etiketi mongo container'a vermek istediğimiz isim
-d detached yani background process olarak çalış

Bu komutu verdikten sonra, compass veya herhangi bir uygulamadan 
mongodb://localhost:27017 adresini kullanarak mongodb ye bağlanırız

docker run --name mongodb -d -p 27017:27017 mongo
```

### VERİLERİ KALICI YAPMA

```
docker run --name mongodb -d -v YOUR_LOCAL_DIR:/data/db mongo

docker run --name mongodb -d -p 27017:27017 -v /opt/data/db:/data/db mongo

container içerisindeki /data/db klasörüdeki verileri ..../opt/data/db ye kaydet.

```
[Yardımcı Kaynak](https://stackoverflow.com/questions/55099622/docker-volume-data-lost-when-container-is-removed-or-stoped-and-then-restarted)




