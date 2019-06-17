---
layout: post
title: Pisi Linux Lazarus Kurulumu
description: "Pisi Linux Lazarus Kurulum"
author: Sami BABAT
category: linux
tags: linux, lazarus
finished: true
---


## Lazarus Nedir?

![panda]({{ site.url }}/assets/lazarus1.png)

Lazarus açık kaynak kodu ile dağıtılan Free Pascal ile geliştirilmiş görsel geliştirme arayüzüdür. Lazarus IDE (Integrated development environment : Tümleşik geliştirme arayüzü) ile bir çok ortam için yazılım geliştirilebilir.

## Farklı Sistemlerde Aynı Yazılım

Lazarus, programlama dili değil, Delphi programlama dilinin geliştirme ortamıdır. Derleyicisi ise FPC (Free Pascal Compiler). Görsel programlama konusunda en gelişmiş, geliştirme ortamlardan birisidir. Bunun sebebi ise Çapraz Platform. Cross-platform programming yada Multi Platform Programming ile Yazdığımız bir programı birden fazla işletim sistemin ve işlemci ile çalıştırmayı kastediyoruz. Yani yazdığınız bir uygulamayı Lazarus ayarlarından FPC sayesinde istediğiniz işletim sistemi ve işlemciye göre derleyebiliyorsunuz.

![panda]({{ site.url }}/assets/lazarus2.png)

## Lazarus'ta programlama

Lazarus, component(Bileşen) bakımında zengin ve çeşitli olması bunun yanı sıra kendi yazdığınız veya lazarus geliştiricileri tarafından yazılan eklentileri eklemek başka bir güzelliği. Diğer geliştirme ortamlara nazaran daha farklı bir görünüme sahip. Pencereler birbirinden ayrıdır(Component menüsü, Tools menüsü, mesaj bölümü).

![panda]({{ site.url }}/assets/lazarus3.png)
![panda]({{ site.url }}/assets/lazarus4.png)

## Pisi Linux'a Kurma

Lazarus, 1.8.4 en sürümü ile Pisi Linux deposunda. Kurulumu paket yöneticisinden veya konsoldan aşağıda ki komut ile kurabilirsiniz.


{% highlight python %}
sudo pisi em lazarus
{% endhighlight %}

