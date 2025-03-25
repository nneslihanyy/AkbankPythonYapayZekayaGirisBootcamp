# 🚇 Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

## 📝 Proje Açıklaması
Bu proje, karmaşık bir metro ağında iki istasyon arasındaki en hızlı ve en az aktarmalı rotaları bulan gelişmiş bir rota optimizasyon simülasyonudur. Yapay zeka ve graph algoritmaları kullanarak metro yolculuklarını optimize eder.

## 🛠 Kullanılan Teknolojiler ve Kütüphaneler

### Programlama Dili
- **Python 3.x**: Projenin temel geliştirme dili

### Standart Kütüphaneler
- **collections (deque)**: 
  - Etkin kuyruk veri yapısı yönetimi
  - BFS algoritmasında sıralı gezinme
  - Bellek açısından optimize edilmiş kuyruk işlemleri

- **heapq**:
  - Öncelik kuyruğu uygulamaları
  - A* algoritmasında en düşük maliyetli düğümlerin hızlı çıkarımı
  - Otomatik sıralama ve düzenleme

- **typing**:
  - Statik tip kontrolleri
  - Kod kalitesini artırma
  - Hata ayıklama süreçlerini kolaylaştırma

## 🧠 Algoritmaların Çalışma Mantığı

### 1. BFS (Breadth-First Search) Algoritması
#### Çalışma Prensibi
- Tüm olası rotaları eşit derinlikte keşfeder
- Genişlik öncelikli arama stratejisi
- Minimum aktarma sayısını hedefler

#### Özellikleri
- `collections.deque` ile bellek verimli kuyruk yönetimi
- Katmanlı gezinme stratejisi
- Hat değişimlerini minimize etme
- Tüm olası rotaları sistematik olarak keşfetme

### 2. A* Algoritması
#### Çalışma Prensibi
- En hızlı ve en optimize rotayı bulma
- Sezgisel maliyet hesaplaması
- Gerçek zamanlı rota optimizasyonu

#### Özellikleri
- `heapq` ile dinamik öncelik sıralaması
- Toplam seyahat süresini hesaplama
- Düğüm maliyetlerini anlık değerlendirme
- Heuristic fonksiyonlarla optimizasyon

## 🎯 Algoritma Seçim Nedenleri

### BFS Tercih Gerekçeleri
- Aktarma sayısını minimize etme
- Karmaşık olmayan rota bulma
- Tüm olası rotaları eşit şekilde keşfetme
- Hesaplama açısından verimli

### A* Tercih Gerekçeleri
- Dinamik ve gerçek zamanlı rota hesaplama
- Performans odaklı optimizasyon
- Sezgisel maliyet hesaplamaları
- Kompleks metro ağları için uygunluk

## 🧪 Örnek Kullanım ve Test Sonuçları

### Test Senaryoları
1. **AŞTİ → OSB Rotası**
   - En az aktarmalı rota: 4 aktarma
   - En hızlı rota: 25 dakika
   - Güzergah: AŞTİ → Kızılay → Ulus → Demetevler → OSB

2. **Batıkent → Keçiören Rotası**
   - En az aktarmalı rota: 3 aktarma
   - En hızlı rota: 21 dakika
   - Güzergah: Batıkent → Demetevler → Gar → Keçiören

3. **Keçiören → AŞTİ Rotası**
   - En az aktarmalı rota: 5 aktarma
   - En hızlı rota: 19 dakika
   - Güzergah: Keçiören → Gar → Sıhhiye → Kızılay → AŞTİ

## 🚀 Gelecek Geliştirme Fikirleri

### 1. Görselleştirme Geliştirmeleri
- İnteraktif metro ağı haritası
- Gerçek zamanlı rota animasyonları
- 3D metro ağı görselleştirmesi

### 2. Gelişmiş Özellikler
- Gerçek zamanlı trafik entegrasyonu
- İstasyon yoğunluk haritası
- Dinamik rota önerileri
- Erişilebilirlik bilgilendirmesi
- Maliyet hesaplama sistemi

### 3. Teknik Altyapı İyileştirmeleri
- Büyük ölçekli metro ağı desteği
- Çoklu hat yönetimi
- Makine öğrenmesi ile rota optimizasyonu
- Gerçek zamanlı veri güncelleme mekanizması

