---
layout: post
title: ISDone.dll, unarc.dll hatası
description: ISDone.dll, unarc.dll hatası
author: Sami BABAT
category: Başıma Gelenler
tags: windows, delphi, RAD Studio
finished: false

---
### ISDone.dll, unarc.dll hatası

Selamlar, windows kullanıcısı değilim. Fakat RAD Studio XE* için yapılmış bir bir kütüphaneyi test etmek için windows kurup işlerimi halletmeye çalıştım. Kütüphaneyi kurarken ‘ISDone.dll’ başlıklı;

> An error occurred when unpacking!  
> Unarc.dll returned an error code: 1  
> error archive data corrupted (decompression fails)

şeklinde bir hata aldım.(Aşağıda resimde):

![](https://i.hizliresim.com/99nE8t.png)

Sorun, boyutu büyük [binary(.bin)](http://web.archive.org/web/20170126141931/http://www.file-extensions.org/bin-file-extension-binary-executable) dosyalarının olması imiş.

ISDone.dll ve Unarc.dll hatalarından bazıları aşağıdadır:

* ISDone.dll error
* An error occurred while unpacking: archive corrupted!
* Unarc.dll returned an error code: 7
* Unarc.dll returned an error code: 6
* Unarc.dll returned an error code: 12
* Unarc.dll returned an error code: 1
* ERROR: archive data corrupted (decompression fails)

**Hataların Açıklaması:**

* Code 1 : “INVALID_FUNCTION”, Geçersiz fonksiyon yada arşiv bozuk.
* Code2 : “FILE_NOT_FOUND”, “Dosya bulunamadı” yani unarc belirtilen dosyayı bulamıyor.
* Code 3: “PATH_NOT_FOUND” , Yol bulunamadı
* Code 5: “ACCESS_DENIED” , erişim engellendi.
* Code 6: “INVALID_HANDLE”, Geçersiz işlem.
* Code 7: “STORAGE_BLOCKS_WERE_DESTROYED” , depolama blokları zarar görmüş.
* Code 11: “BAD_FORMAT”, Kötü/Bozuk dosya biçimi
* Code 12: “INVALID_ACCESS”, Erişim yok.
* Code 14: “OUT_OF_MEMORY”, Yetersiz bellek(Ram kullanımı)

Bu nalet hata yüzüden 1 saatir yapmadığım şey kalmadı. Acayip sinir bozucu bir durum ve çözümü akıl almaz derece basit olmasıda ayrı bir sinir.

Sorunun sebebi dosyaların(.bin) **virus olma ihtimali** yüzünden windows tarafından engelleniyor olması. Sorunu çözmek içinde **Makinanızda kurulu olan antivirüs yazılımını veya kurulu değilsede ‘Windows Defender’ adlı aleti devre dışı bırakmak imiş.**

Böyle sorun başınıza gelirde google’a aratırsanız karşınıza böyle bir yazı çıksın diye blog’ta “Başıma Gelenler” kısmına ekledim. Bu sayede de ‘Başıma gelenler’ adlı bir kategori oluşturmuş oldum. Artık başıma gelenler hata ve başka şeyleri buraya yazmak farz olacak sanırım.