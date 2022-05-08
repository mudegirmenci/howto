### Docker bazı komutlar:

`docker rm $(docker ps -aq)`:Açık bütün konteynırları sil:

`docker ps -a`:Çalışıp işi bitenleri listele:

`docker run -rm ubuntu`: konteynırı çalıştır işi bitince sil:

`docker run rmi ubuntu`: docker image sil

`docker inspect <container> `:container ile ilgili bilgiler verir.

`docker exec -it 2f psql -U postgres`:***2f*** id li **çalışan** konteynıra bağlan. `-U postgres`  postgres veritabanına postgres kullanıcı ile bağlan.
