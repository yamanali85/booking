# Arapça → Türkçe Simultane Çeviri

Arapça konuşmayı dinler, Türkçesini ekranda canlı altyazı gibi gösterir. Tek dosyadan oluşur: `index.html`.

## Çalıştırma

1. `index.html` dosyasını **Chrome** veya **Edge** ile açın. Mikrofon izni sorunsuz çıksın diye yerel sunucu da kullanabilirsiniz:
   ```
   cd simultane-ceviri && python3 -m http.server 8000
   ```
   Ardından http://localhost:8000 adresini açın.
2. **▶ Başlat**'a basın ve mikrofon izni verin (boşluk tuşu da başlatır/durdurur).
3. Konuşmacının lehçesini üstteki listeden seçin.

Konuşma sürerken gri yazıyla anlık çeviri görünür. Cümle bitince çeviri kesinleşir ve beyaza döner.

## Ayarlar

- **Çeviri motoru**
  - *Google Translate*: Anahtar gerekmez, en hızlısı budur.
  - *Claude*: Daha doğal bir Türkçe verir ve önceki cümleleri bağlam olarak kullanır. Anthropic API anahtarı gerekir. Anahtar sadece tarayıcınızda (localStorage) saklanır.
- Yazı boyutunu ayarlayabilir, Arapça metni gizleyebilir, anlık çeviriyi kapatabilirsiniz. **⛶** düğmesi tam ekran yapar (projeksiyon veya TV için).

## Bilgisayar sesini çevirmek (YouTube, TV, Zoom)

Tarayıcının konuşma tanıma özelliği sadece mikrofon girişini dinler. Bilgisayarda çalan sesi çevirmek için bir sanal ses kablosu kurun ve onu mikrofon olarak seçin:

- **Windows**: [VB-Audio Virtual Cable](https://vb-audio.com/Cable/). Çıkışı "CABLE Input" yapın. Chrome'da mikrofon olarak "CABLE Output"u seçin (adres çubuğundaki kilit simgesi → Site ayarları).
- **macOS**: [BlackHole](https://existential.audio/blackhole/). Sesi duymaya devam etmek için Audio MIDI Setup'ta "Multi-Output Device" oluşturun.

## Notlar

- Konuşma tanıma Chrome/Edge'in bulut servisini kullanır, bu yüzden internet bağlantısı gerekir.
- Firefox ve Safari Web Speech API'yi tam desteklemez.
