# Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

Bu proje, bir metro ağında iki istasyon arasındaki en hızlı ve en az aktarmalı rotaları bulan bir simülasyon uygulamasıdır.

## Kullanılan Teknolojiler ve Kütüphaneler

- Python 3.x
- collections (deque): Kuyruk veri yapısı için
- heapq: Öncelik kuyruğu için
- typing: Tip kontrolleri için

## Algoritmaların Çalışma Mantığı

### BFS (Breadth-First Search) Algoritması
- En az aktarmalı rotayı bulmak için kullanılır
- Özellikler:
  - Kuyruk veri yapısı kullanır (collections.deque)
  - Ziyaret edilen istasyonları takip eder
  - Komşu istasyonları keşfeder
  - Hat değişimlerini belirginleştirir
  - En kısa rotayı bulur

### A* Algoritması
- En hızlı rotayı bulmak için kullanılır
- Özellikler:
  - Öncelik kuyruğu kullanır (heapq)
  - Ziyaret edilen istasyonları takip eder
  - Toplam süreyi hesaplar
  - Hat değişimlerini belirginleştirir
  - En hızlı rotayı bulur

## Neden Bu Algoritmaları Kullandık?

1. BFS Algoritması:
   - En az aktarmalı rotayı bulmak için ideal
   - Tüm olası rotaları eşit derinlikte keşfeder
   - Hat değişimlerini minimize eder

2. A* Algoritması:
   - En hızlı rotayı bulmak için en uygun
   - Öncelik kuyruğu sayesinde en kısa süreli rotayı bulur
   - Gerçek zamanlı süre hesaplaması yapar

## Örnek Kullanım ve Test Sonuçları

```
=== Test Senaryoları ===

1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (25 dakika): AŞTİ -> Kızılay -> Kızılay -> Ulus -> Demetevler -> OSB

2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören

3. Keçiören'den AŞTİ'ye:
En az aktarmalı rota: Keçiören -> Gar -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
En hızlı rota (19 dakika): Keçiören -> Gar -> Gar -> Sıhhiye -> Kızılay -> AŞTİ
```

## Projeyi Geliştirme Fikirleri

1. Görselleştirme:
   - Metro ağını görsel olarak gösterme
   - Rotaları harita üzerinde çizme
   - Animasyonlu rota gösterimi

2. Ek Özellikler:
   - Gerçek zamanlı trafik durumu
   - İstasyon yoğunluğu bilgisi
   - Alternatif rotalar
   - Fiyat hesaplama
   - Engelli erişimi bilgisi

3. Veri Yapısı İyileştirmeleri:
   - Daha büyük metro ağı desteği
   - Çoklu hat desteği
   - Dinamik rota güncelleme 