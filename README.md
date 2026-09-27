# Bulmaca+ — türetilmiş kelime verisi / derived word data

**TR** · Bu depo, [Bulmaca+](https://github.com/bulmacaplus) kelime
oyunlarının kullandığı **türetilmiş** kelime tablolarını taşıyor. Buradaki
veri, açık kaynaklardan üretildi ve o kaynakların şartları gereği
yayımlanıyor.

**EN** · This repository holds the **derived** word tables used by the
Bulmaca+ word games. The data is produced from open sources and is
published here as those sources require.

---

## Ne var burada / What's here

| Dosya / File | Dil / Language | Madde / Entries | Lisans / Licence |
|---|---|---|---|
| `tr_words.tsv` | Türkçe | 25.423 | CC BY-SA 4.0 |
| `en_words.tsv` | English | 32.059 | CC BY-SA 4.0 |
| `pt_words.tsv` | Português (BR) | 14.554 | CC BY-SA 4.0 **+ MPL-2.0 / LGPL-3.0** |

**TR** · Portekizce tablo iki copyleft kaynaktan türedi ve bu yüzden
**birleşik tek bir lisans iddia edilmiyor** — ayrıntı
[`NOTICE.md`](NOTICE.md).

**EN** · The Portuguese table derives from two copyleft sources, so no
combined single licence is claimed for it — see [`NOTICE.md`](NOTICE.md).

Sekmeyle ayrılmış, dört sütun. `#` ile başlayan satırlar açıklama.
Tab-separated, four columns. Lines starting with `#` are comments.

| Sütun / Column | Anlamı / Meaning |
|---|---|
| `word` | Kelime, oyunda göründüğü gibi / the word as shown in game |
| `rank` | Sıklık listesindeki sıra; boşsa listede yok / frequency rank, empty if absent |
| `band` | `very_common` · `common` · `medium` · `rare` |
| `target_allowed` | `1` hedef olabilir, `0` yalnız bonus / `1` may be a puzzle target, `0` bonus only |

### Sıra neden boş olabiliyor / Why rank can be empty

**TR** · Sıklık listesi 50.000 kelimeyle sınırlı. Listede olmayan bir
kelime **hedef** olamıyor ama **bonus** olarak kabul ediliyor: oyuncu
biliyorsa ödülünü alıyor. Türkçede maddelerin 6.334'ü sıra taşıyor,
gerisi yalnız bonus.

**EN** · The frequency list is capped at 50,000 words. A word that is
absent cannot be a puzzle **target** but is still accepted as a **bonus**
word. In Turkish 6,334 entries carry a rank; the rest are bonus-only.

---

## Bu veri nasıl üretildi / How this was derived

**TR** · İki bağımsız kaynak kesiştirildi:

1. **Geçerli kelime mi?** — yetkili bir sözlük kaynağı.
2. **Gerçekten kullanılıyor mu?** — bir sıklık listesi.

Bir kelimenin havuza girmesi için **ikisini birden** geçmesi gerekiyor.
Sebebi şu: sözlük arkaik ve teknik maddeler taşıyor, sıklık listesi ise
ham altyazı jetonları (özel adlar, yabancı kelimeler, yazım hataları)
içeriyor. Kesişim ikisinin de kusurunu süzüyor.

Ham sıklık **sayıları** atıldı; yerine **sıra** tutuldu. Ham sayılar
derlem büyüklüğüne bağlı ve derlemler arası karşılaştırılamaz.

**EN** · Two independent sources were intersected: an authoritative
lexicon (*is this a valid word?*) and a frequency list (*is it actually
used?*). A word must pass **both**. Raw frequency counts were discarded in
favour of ranks, because raw counts depend on corpus size and are not
comparable across corpora.

Bu bir **uyarlamadır** (adaptation), kaynakların kopyası değil.

---

## Lisans / License

**TR** · Bu depodaki veri **CC BY-SA 4.0** ile lisanslıdır, çünkü sıklık
kaynağı o lisansta ve bu tablolar ondan türetilmiş uyarlamalar.

**EN** · The data in this repository is licensed under **CC BY-SA 4.0**,
because the frequency source carries that licence and these tables are
adaptations of it.

> Creative Commons Attribution-ShareAlike 4.0 International
> https://creativecommons.org/licenses/by-sa/4.0/

Kaynakların tek tek atıfları: [`NOTICE.md`](NOTICE.md).
Per-source attribution: [`NOTICE.md`](NOTICE.md).

**Uygulamanın kendisi bu lisansa tabi değil.** CC BY-SA'nın koşulu
uyarlanan materyale ait; Bulmaca+ uygulaması, bulmacaları, görselleri ve
seviye tasarımı ayrı ve kapalıdır.

**The application itself is not under this licence.** ShareAlike binds the
adapted material; the Bulmaca+ app, its puzzles, artwork and level design
are separate and proprietary.

---

## Neden yayımlıyoruz / Why we publish this

**TR** · Çünkü mecburuz ve bunu bilerek kabul ettik. Kullandığımız sıklık
ve sözlük kaynaklarının çoğu copyleft: CC BY-SA, GPL, LGPL, MPL. Hepsi
türetilmiş **listenin** aynı şartlarla erişilebilir olmasını istiyor —
ama hiçbiri uygulamanın açılmasını istemiyor.

Bir süre bu kaynakları "share-alike olduğu için kullanılamaz" diye
elemeye çalıştık. Yanlış kararmış: o şekilde hedeflediğimiz yedi dilin
beşinde kullanılabilir hiçbir kaynak kalmıyordu. Bedeli listenin kendisi
ve o bedel makul — liste ürünün değeri değil.

**EN** · Because we must, and we accepted that deliberately. Most usable
frequency and lexicon sources are copyleft (CC BY-SA, GPL, LGPL, MPL).
They require the derived **list** to stay available under the same terms;
none of them require the application to be opened. Treating share-alike as
disqualifying left five of our seven target languages with no usable
source at all.

---

## Bu dosyalar elle düzenlenmez / Do not edit by hand

**TR** · `tools/legal/export_public_word_data.dart` üretiyor, kaynağı
uygulamanın **paketlenen** sözlükleri. Bir kapı ikisinin aynı olduğunu
ölçüyor (`test/legal/published_word_data_test.dart`): yayımlanan kopya
paketlenenden ayrılırsa derleme düşüyor. Elle yapılan düzeltme ilk
üretimde kaybolur.

**EN** · Generated by `tools/legal/export_public_word_data.dart` from the
app's **bundled** dictionaries. A gate asserts the published copy matches
what ships; hand edits are lost on the next export.
