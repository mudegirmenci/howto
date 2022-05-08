# VIM Tab

Birkaç dosyayı ayrı tablar halinde açmak için

`vim -p file1 file2`

şeklinde kullanabiliriz.

tablar arasında gezmek için

`gt veya gT`

yazmanız yeterli.

yeni bir sekme eklemek için

`:tabenew`

komutunu kullan. 

yeni bir sekmede dosya açmak için

`:tabe dosyaismi`

sekmeleri kapatmak için:

```
:-tabclose      " close the previous tab page
:+tabclose      " close the next tab page

```

sekmelerde dolaşmak

```
:-tabnext   " go to the previous tab page
:+tabnext   " go to the next tab page
:+2tabnext  " go to the two next tab page
:1tabnext   " go to the first tab page
:$tabnext   " go to the last tab page

```

sekmeleri taşımak

```

:-tabmove    geri  
:+tabmove    ileri
