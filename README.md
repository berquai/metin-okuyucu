# Metin Okuyucu

Uzun akademik metinleri cümle cümle sesli okuyan, tarayıcıda çalışan bir okuma ve redaksiyon aracı. Tez yazımı sırasında metni kulakla gözden geçirmek için geliştirildi.

**Kullanmak için:** [berquai.github.io/metin-okuyucu](https://berquai.github.io/metin-okuyucu/)

Kurulum gerekmez. Sayfayı aç, metnini yapıştır ve **▶ Oku** düğmesine bas.

## Neler yapar?

- **Cümle cümle okuma:** Okunan cümle altı çizili, okunan kelime renkli olarak vurgulanır.
- **Türkçe akademik metne uygun cümle bölme:** "s. 45", "a.g.e.", "vd.", "Prof. Dr.", "M. Kemal", "I. Dünya Savaşı" gibi ifadelerde cümle yanlış yerden bölünmez.
- **Okunuş düzeltmeleri:** Roma rakamları sıra sayısı olarak okunur ("XX. yüzyıl" → yirminci yüzyıl). Kısaltmalar açılarak okunur ("bkz." → bakınız, "TBMM" → Te Be Me Me).
- **Düzenlenebilir kısaltma sözlüğü:** Kendi kısaltmalarını `kısaltma = okunuşu` biçiminde ekleyebilirsin.
- **İşaretleme:** Dinlerken sorunlu cümleleri işaretle, sonra hepsini liste olarak kopyala.
- **Uzun cümle uyarısı:** Belirlediğin kelime sayısını aşan cümleler işaretlenir (varsayılan: 40).
- **Ayarlanabilir okuma:** Hız, ses perdesi, cümle ve paragraf arası duraklama.
- **Kaldığın yeri hatırlar:** Metin, konum ve ayarlar tarayıcıda otomatik kaydedilir.
- **Mobil düzen:** Telefonda düğmeler ekranın altına iner. İstersen yalnızca simgeli düğmeler kullanılabilir.
- **Görünüm:** Beş hazır tema, özel renk, yazı tipi, boyut ve satır aralığı.

## Kısayollar

| Eylem | Masaüstü | Telefon |
|---|---|---|
| Bir cümleden okumaya başla | Çift tık | Çift dokunma |
| Oynat / duraklat | Boşluk | ▶ düğmesi |
| Önceki / sonraki cümle | ← / → | ◁ / ▷ düğmeleri |
| Cümleyi işaretle | M | ★ düğmesi |
| Cümleyi baştan oku | R | ↻ düğmesi |
| Durdur ve düzenlemeye dön | Esc | ■ düğmesi |

## En iyi ses için

Sayfayı **Microsoft Edge** ile aç. Edge, ücretsiz ve doğal Türkçe sesler sunar ("Microsoft Ahmet / Emel Online (Natural)"). Araç bu sesleri otomatik olarak öne alır.

Telefonda cihazın kendi Türkçe sesi kullanılır. iPhone'da Ayarlar > Erişilebilirlik > Seslendirilen İçerik > Sesler > Türkçe yolundan "Gelişmiş" bir ses indirmek kaliteyi belirgin şekilde artırır.

## Gizlilik

Yapıştırdığın metin hiçbir sunucuya gönderilmez. Seslendirme cihazının kendi ses motoruyla yapılır ve metin yalnızca senin tarayıcının yerel hafızasında saklanır.

Bu yüzden:
- Metin, cihazlar ve tarayıcılar arasında taşınmaz.
- Tarayıcı verilerini temizlersen kayıtlı metin de silinir. Asıl metnini her zaman başka bir yerde sakla.

İsteğe bağlı "Google (çevrimiçi)" sesi bu kuralın tek istisnasıdır: seçilirse metin Google sunucularına gider. Bu nedenle varsayılan olarak kapalıdır ve seçilmeden önce onay ister.

## Teknik notlar

- Tek bir HTML dosyasıdır. Dış kütüphane, sunucu veya derleme adımı gerektirmez.
- Tarayıcının Web Speech API'sini ve cümle bölme için `Intl.Segmenter`'ı kullanır.
- `index.html` dosyasını bilgisayarına indirip çevrimdışı da kullanabilirsin.

## Geliştirici

Berkay Çelik · berkcel@gmail.com

## Lisans

[MIT Lisansı](LICENSE). Aracı özgürce kullanabilir, değiştirebilir ve paylaşabilirsin; yeter ki telif ve lisans notunu koru.
