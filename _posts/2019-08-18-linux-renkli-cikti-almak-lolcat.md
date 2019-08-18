---
layout: post
title: lolcat ile Konsoldan renkli çıktı almak 
description: "Konsoldan renkli çıktı almak: lolcat"
author: Sami BABAT
category: linux
tags: linux, lolcat
finished: true
youtubeId: 2gZvBZsLqWA
---


## lolcat ile Konsoldan renkli çıktı almak 

Linux denilince akla gelen ilk şey, siyah bir ekran ve siyah ekranda hızlı hızlı geçişen yazılar. Romantik bir kavram kullandım gibi :) Çoğu kullanıcı estetikliği sever eğlenceli ve hoş bir uygulamamız var. bu uygulama, konsolda renkli çıktılar vermemizi sağlıyor.

{% include youtubePlayer.html id=page.youtubeId %}

# KURULUM

Tüm linux dağıtımları için kurulum göstereceğim için dağıtımlara özel paket yöneticileri ile kurulum yapmayacam. Ruby’in gem sistemini kullanarak kuralım. Tabi siz paket yöneticisinden kurmak isterseniz(Kullandığınız dağıtım deposunda varsa) lolcat diye aratmanız yeterli.

İNDİRME LİNKİ: <a href="https://github.com/rubygems/rubygems/archive/master.zip">https://github.com/rubygems/rubygems/archive/master.zip</a>

Eğer Git kurulu ise indirme linkini es geçip aşağıdan devam edin.

Git tamamsa konsolu açıp lolcatı kuralım.
{% highlight bash %}
git clone https://github.com/rubygems/rubygems.git
{% endhighlight %}
İndirdiğiniz dizin içine girin ve aşağıda ki komutu verin(Ruby kurulu olması gerekir/varsayılan olarak kurulu gelir.)
{% highlight bash %}
sudo ruby setup.rb
{% endhighlight %}
Kurulumu test etmek için:
{% highlight bash %}
gem -v
{% endhighlight %}
Gem paket yöneticisini kurduğumuza göre lolcat’a geçelim.
Kurulum için aşağıda ki komutu vererek kuralım

{% highlight bash %}
sudo gem install lolcat
{% endhighlight %}
# KULLANIM

lolcat tüm seçenekleri için lolcat -h komutunu verebilirsiniz.

Kullandığınız tüm komutları renkli çıktı olarak almak isterseniz:
{% highlight bash %}
<komut> | lolcat
{% endhighlight %}
cal | lolcat
yada text olarak
{% highlight bash %}
echo "Renkli yazı" | lolcat -a -d 500
{% endhighlight %}