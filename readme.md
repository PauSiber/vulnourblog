## Vulnourblog KURULUM
****
  ** NOT : Öncelikle bilgisayarınızda Apache , MySQL , PHP ve phpMyAdmin'nin yüklü olması gerekmektedir. **

  ** NOT-2: Bu anlatımda Ubuntu işletim sistemi kullanılmıştır. Sizin kullandığınız işletim sistemi farklıysa veya local sunucunuz farklı bir yerde çalışıyorsa lütfen kurulum adımlarını ona göre uygulayınız. **

  İlk önce dosyalarımızı yerel sunucumuza çekelim. (git clone işleminde hata alırsanız başına sudo yazarak tekrar deneyiniz.)

      cd /var/www/html
      git clone https://github.com/PauSiber/vulnourblog.git

  Şimdi veritabanımızı phpMyAdmin üzerinden yükleyelim.


  Yukarıdaki menüden ** Import ** yazan kısma tıklıyoruz.

  ![](/uploads/import.png)

  Şimdi githubdan çektiğimiz dosyaların içinde bulunan ** vulnourblog.sql ** isimli dosyamızı import edelim.

  ** Choose File ** butonuna tıklayıp ** vulnourblog.sql ** dosyamızı seçiyoruz. Ardından ** Go ** butonuna basarak işlemimizi tamamlıyoruz.  

  ![](/uploads/import2.png)

  Sol taraftaki menüye bakarsanız ** cypwn_vulnourblog ** isimli veritabanımızın oluştuğunu görebilirsiniz.

  Şimdi son olarak veritabanı bağlantısını gerçekleştirelim.

    sudo nano /var/www/html/vulnourblog/include/settings.php

  ![](/uploads/connect.png)

  Bu kısımda ** $db_pass ** kısmına kendi phpMyAdmin parolanızı yazmanız gerekmektedir. ** $db_name ** kısmını ise ** cypwn_vulnourblog ** olarak değiştirelim.

  Tarayıcınızı açıp ** http://localhost/vulnourblog/ ** adresine gidip çözmeye başlayabilirsiniz.

  ![](/uploads/website.png)
