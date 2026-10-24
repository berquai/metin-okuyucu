# Metin Okuyucu

Uzun akademik metinleri cümle cümle sesli okuyan, tarayıcıda çalışan bir okuma ve redaksiyon aracı. Tez yazımı sırasında metni kulakla gözden geçirmek için geliştirildi.

**Kullanmak için:** [berquai.github.io/metin-okuyucu](https://berquai.github.io/metin-okuyucu/)

Kurulum gerekmez. Sayfayı aç, metnini yapıştır ya da bir dosyayı sayfaya sürükleyip bırak, sonra **▶ Oku** düğmesine bas.

## Neler yapar?

- **Dosya açma ve sürükle-bırak:** PDF, Word (.docx), EPUB, ODT, RTF, TXT, Markdown, HTML ve altyazı (SRT/VTT) dosyalarını okur. Birden çok dosya bırakılırsa sırayla birleştirilir.
- **Cümle cümle okuma:** Okunan cümle altı çizili, okunan kelime renkli olarak vurgulanır.
- **Türkçe akademik metne uygun cümle bölme:** "s. 45", "a.g.e.", "vd.", "Prof. Dr.", "M. Kemal", "I. Dünya Savaşı" gibi ifadelerde cümle yanlış yerden bölünmez.
- **Okunuş düzeltmeleri:** Roma rakamları sıra sayısı olarak okunur ("XX. yüzyıl" → yirminci yüzyıl). Kısaltmalar açılarak okunur ("bkz." → bakınız, "TBMM" → Te Be Me Me).
- **Düzenlenebilir kısaltma sözlüğü:** Kendi kısaltmalarını `kısaltma = okunuşu` biçiminde ekleyebilirsin.
- **Doğal ve çok dilli sesler:** Edge'de Ahmet ve Emel'in yanında Brian, Andrew, Florian, Emma ve Ava gibi çok dilli sesler. Çok dilli sesler Türkçeyi de okur, metindeki İngilizce bölümleri doğru telaffuzla seslendirir.
- **İşaretleme:** Dinlerken sorunlu cümleleri işaretle, sonra hepsini liste olarak kopyala.
- **Uzun cümle uyarısı:** Belirlediğin kelime sayısını aşan cümleler işaretlenir (varsayılan: 40).
- **Geri alma:** Yeni metin yüklediğinde ya da metni temizlediğinde önceki metin tek tıkla geri gelir.
- **Görünüm:** 25 hazır tema (iki yüksek karşıtlık teması dahil) ve özel tema; bilgisayarda kurulu yazı tipleri ile internetten yüklenen okuma yazı tipleri; boyut, satır aralığı, harf ve kelime aralığı, kalınlık, satır genişliği ve hizalama.
- **Ekrana kendiliğinden sığar:** Arayüz pencere boyutuna göre ölçeklenir; küçük pencerede bile bütün düğmeler kaydırmadan görünür.
- **Kaldığın yeri hatırlar:** Metin, konum ve ayarlar tarayıcıda otomatik kaydedilir.
- **Yardım ve Hakkında pencereleri:** Bütün özelliklerin ve kısayolların açıklaması uygulamanın içinde (F1).

## Klavye kısayolları

Tek tuşlu kısayollar metin alanının dışındayken çalışır. Metin alanındayken `Esc` okuma görünümüne geçirir.

| Tuş | İşlev |
|---|---|
| `Boşluk` | Oku / duraklat / devam et |
| `A` | Tümünü en baştan oku |
| `←` / `→` | Önceki / sonraki cümle |
| `R` | Cümleyi baştan oku |
| `M` | Cümleyi işaretle |
| `C` | Okunan cümleyi kopyala |
| `V` | Panodaki metni yapıştır |
| `E` | Metni temizle (geri alınabilir) |
| `Ctrl+O` | Dosya aç |
| `Esc` | Okumayı durdur; okuma ve düzenleme görünümü arasında geç |
| `F1` | Yardım |
| Çift tık | O cümleden okumaya başla |

## En iyi ses için

Sayfayı **Microsoft Edge** ile aç. Edge ücretsiz ve doğal sinir ağı sesleri sunar. Araç bu sesleri şu sırayla öne alır: Ahmet, Emel, çok dilli sesler (Brian, Andrew, Florian, Emma, Ava…), diğer Türkçe sesler, diğer diller.

## Gizlilik

- **Metin:** Yalnızca tarayıcının yerel hafızasında saklanır. Hiçbir sunucuya kaydedilmez, cihazlar ve tarayıcılar arasında taşınmaz.
- **Dosyalar:** Açtığın dosyalar tamamen tarayıcının içinde, kendi bilgisayarında işlenir; hiçbir yere yüklenmez.
- **Seslendirme:** Ses listesinde her sesin yanında bir işaret vardır.
  - **☁ Bulut sesi** (Edge'in "Online (Natural)" sesleri, Chrome'un Google sesleri): Okunan cümleler, sesi üretmesi için tarayıcı üreticisinin sunucusuna gönderilir (Microsoft ya da Google).
  - **💻 Cihaz sesi:** Seslendirme bilgisayarında yapılır; metin cihazdan çıkmaz.
  
  Yayımlanmamış bir metni tamamen yerel dinlemek istersen 💻 işaretli bir ses seç.
- **Dış bağlantılar:** Sayfa yalnızca iki durumda internete bağlanır: ilk PDF açıldığında PDF okuyucusunu (Mozilla PDF.js, cdnjs.cloudflare.com) indirmek için ve "İnternetten" grubundan bir yazı tipi seçilirse Google Fonts'tan yazı tipini indirmek için. Bu isteklerle metin gönderilmez.

Tarayıcı verilerini temizlersen kayıtlı metin de silinir. Asıl metnini her zaman başka bir yerde sakla.

## Teknik notlar

- Tek bir HTML dosyasıdır. Sunucu ya da derleme adımı gerektirmez.
- Seslendirme için tarayıcının Web Speech API'sini, cümle bölme için `Intl.Segmenter`'ı kullanır.
- DOCX, ODT ve EPUB dosyaları tarayıcının yerleşik `DecompressionStream` özelliğiyle açılır; bunun için dış kütüphane gerekmez.
- PDF'ler Mozilla PDF.js ile okunur. Satır sonu tirelemeleri birleştirilir, üst simge dipnot numaraları ve tek başına duran sayfa numaraları atlanır, paragraflar ve sayfa geçişleri korunur. Taranmış (görüntü) PDF'lerde seçilebilir metin olmadığı için okunamaz.
- `index.html` dosyasını bilgisayarına indirip çevrimdışı da kullanabilirsin; PDF açmak ve internetten yazı tipi yüklemek için bağlantı gerekir.
- v3'teki ayarlar, kısaltma sözlüğü, işaretler ve kayıtlı metin v4'e otomatik taşınır.

## Geliştirici

Berkay Çelik · berkcel@gmail.com

## Lisans

[MIT Lisansı](LICENSE). Aracı özgürce kullanabilir, değiştirebilir ve paylaşabilirsin; yeter ki telif ve lisans notunu koru.

Üçüncü taraf bileşenler: [PDF.js](https://mozilla.github.io/pdf.js/) © Mozilla, Apache 2.0 Lisansı. İsteğe bağlı yazı tipleri Google Fonts üzerinden SIL Open Font License ile sunulur.
