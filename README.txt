
Sistem Mimarisi
Client

Client aşağıdaki işlemleri gerçekleştirir:

Kullanıcıdan dosya boyutunu alır.
Rastgele veri oluşturur.
Veriyi SHA-256 ile özetler.
Veriyi 1024 byte'lık paketlere böler.
Paketleri UDP üzerinden gönderir.
ACK bekler.
Timeout oluşursa paketi yeniden gönderir.
İstatistikleri raporlar.

Server
Server aşağıdaki işlemleri gerçekleştirir:

UDP portunda dinleme yapar.
Gelen paketleri alır.
Paketleri sıra numarasına göre saklar.
ACK gönderir.
Tüm paketler alındığında verileri birleştirir.
SHA-256 hesaplar.
İstatistikleri raporlar.
Örnek Çıktı
Client
Paket 0 Gönderildi
ACK Alındı : 0
RTT = 2 ms

Paket 1 Gönderildi
ACK Alındı : 1
RTT = 1 ms

===== CLIENT RAPORU =====

Toplam Paket : 10
Başarılı Paket : 10
Başarısız Paket : 0
Timeout Sayısı : 0
Yeniden Gönderim : 0
Toplam Süre : 0.05 saniye
Server
Paket Alındı -> Seq=0 Boyut=1024
ACK Gönderildi -> 0

Paket Alındı -> Seq=1 Boyut=1024
ACK Gönderildi -> 1

===== SERVER RAPORU =====

Toplam Paket : 10
Başarılı Paket : 10
Başarısız Paket : 0