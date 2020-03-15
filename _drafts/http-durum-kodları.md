---
layout: post
title: HTTP Durum Kodları
description: HTTP Durum Kodları
author: Sami BABAT
category: Tech
tags: http
finished: false

---
HTTP için durum kodları aşağıdaki gibidir :

# **1xx : Bilgi Amaçlı**

* **100 Continue** : İstek başarılı alındığı ve devam edilebileceği belirtilir
* **101 Switching Protocols** : Sunucu, istemciden aldığı protokol değiştirme isteğine uyacağını belirtmektedir

***

# **2xx : Başarılı**

* **200 OK** : İstek başarılı alınmış ve cevap başarılı verilmiştir
* **201 Created** : İstek başarılı olmuş ve sunucuda yeni bir kaynak yaratılmıştır
* **202 Accepted** : Sunucu isteği kabul etti ancak henüz işlemedi
* **203 Non-Authoritative Information** : Sunucu isteği başarılı işledi, ancak başka kaynakta olabilecek bilgi döndürmektedir
* **204 No Content** : İstek başarılı alınmış ancak geri içerik döndürülmemektedir
* **205 Reset Content** : İstek başarılı alınmış ancak geri içerik döndürülmemektedir. Ancak içerik temizlenecektir (örneğin bir web formunda doldurulan bilgiler)
* **206 Partial Content** : GET için kısmi içerik (içeriğin bir belirli bir parçası) başarılıyla döndürülmüştür

***

# **3xx : Yönlendirme**

* **300 Multiple Choices** : Sunucuda isteğe göre birden fazla seçenek olduğunu bildirir. Sunucu seçeneği kendisi seçebilir veya seçenek listesini görüntüleyebilir
* **301 Moved Permanently** : Bir kaynağın (veya sayfanın) kalıcı olarak başka bir yere taşındığını bildirir ve o yere yönlendirme sağlar
* **302 Found (HTTP 1.0) – Moved Temporarily (HTTP 1.1)** : Bir kaynağın (veya sayfanın) kalıcı değil geçici olarak başka bir kaynağa yönlendirir. Kaynağın ana adresi değişmemiştir
* **303 See Other** : Farklı bir kayanağa GET yapılması gerektiğini belirtir
* **304 Not Modified** : İstenilen kaynakta daha önce yapılan istekten beri herhangi bir değişikliğin olmadı belirtilir ve içerik gönderilmez
* **305 Use Proxy** : Sunucu tarafından döndürülen proxy’in kullanılması gerektiği belirtilir
* **306 Switch Proxy** : Bu durum kodu artık kullanılmıyor
* **307 Temporary Redirect** : Bir kaynağın (veya sayfanın) kalıcı değil geçici olarak başka bir kaynağa yönlendirir.

***

# **4xx: Client Hatası**

* **400 Bad Request** : İstek hatalı (isteğin yapısı hatalı) olduğu belirtilir
* **401 Unauthorized** : İstek için kimlik doğrulaması gerekiyor
* **402 Payment Required** : Ödeme gerekiyor. (gelecekte kullanılması için ayrılmıştır)
* **403 Forbidden** : Kaynağın yasaklandığını belirtir
* **404 Not Found** : İstek yapılan kaynağın (veya sayfanın) bulunamadığını belirtir
* **405 Method Not Allowed** : Sunucu , HTTP Method’u kabul etmiyor
* **406 Not Acceptable** : İstemcinin Accept header’ında verilen özellik karşılanamıyor
* **407 Proxy Authentication Required** : Proxy üzerinden yetkilendirme gerekir
* **408 Request Timeout** : İstek zaman aşımına uğradı (belirli bir sürede istek tamamlanamadı)
* **409 Conflict** : İstek içinde çelişki var
* **410 Gone** : Kaynak artık yok
* **411 Length Required** : İstekte “Content-Length” (içeriğin boyutu) belirtilmemiş
* **412 Precondition Failed** : Sunucu istekte belirtilen bazı önkoşulları karşılamıyor
* **413 Request Entity Too Large** : İsteğin boyutu çok büyük olduğu için işlenemedi
* **414 Request-URI Too Long** : URI (URL) fazla büyük
* **415 Unsupported Media Type** : İstenilen kaynak istenilen medya tipinin desteklemeiyor
* **416 Requested Range Not Satisfiable** : İstek yapılan parça (bir dosyanın bir parçası vb..) sunucu tarafından verilebiliyor veya uygun değil
* **417 Expectation Failed** : Sunucu “Expect” ile istenileni desteklemiyor veya yerine getiremiyor

***

# **5xx: Sunucu Hatası**

* **500 Internal Server Error** : Sunucuda bir hata oluştu ve istek karşılanamadı
* **501 Not Implemented** : Sunucu istenilen isteği yerine getirecek şekilde yapılandırılmamıştır
* **502 Bad Gateway** : Gateway veya Proxy sunucusu, kaynağın bulunduğu sunucudan (upstream sunucusu) cevap alamıyor
* **503 Service Unavailable** : Sunucu şu anda hizmet vermiyor (kapalı veya erişilemiyor)
* **504 Gateway Timeout** : Gateway veya Proxy sunucusu, kaynağın bulunduğu sunucudan (upstream sunucusu) belirli bir zaman içinde cevap alamadı
* **505 HTTP Version Not Supported** : HTTP Protokol versiyonu desteklenmiyor