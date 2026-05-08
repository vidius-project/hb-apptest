# Hepsiburada Mobile Automation Case

Bu proje, Hepsiburada Android uygulaması için hazırlanmış uçtan uca (end-to-end) Maestro otomasyon test senaryosunu içermektedir.

## Kullanılan Teknolojiler

- Maestro
- Android Emulator

---

## Test Senaryosu

1. Hepsiburada uygulaması açılır
2. Ana sayfada listelenen ilk ürün detayına gidilir
3. Ürün detay sayfasında “Sepete ekle” butonuna tıklanır
4. Kullanıcı login olmadan ödeme akışına yönlendirilir
5. Sepet sayfasında:
   - Ürünün sepette yer aldığı
   - Fiyat bilgisinin görüntülendiği
   - Ödeme akışının erişilebilir olduğu
doğrulanır

---

## Otomasyon Yaklaşımı

- Dinamik ekran yapısı nedeniyle reusable selector kullanılmıştır
- `scrollUntilVisible` ile dinamik içerikler yönetilmiştir
- Stabil çalışması için generic doğrulamalar tercih edilmiştir
- Login ekranı için optional akış uygulanmıştır
- Mümkün olduğunca id/text selector kullanılmış, coordinate-based yaklaşım tercih edilmemiştir

---

## Test Çalıştırma

```bash
maestro test hbapp_test.yaml
