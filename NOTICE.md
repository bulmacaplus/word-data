# Atıflar / Attribution

Bu depodaki türetilmiş tablolar aşağıdaki kaynaklardan üretildi.
The derived tables in this repository are produced from the sources below.

---

## 1. Sıklık verisi / Frequency data — CC BY-SA 4.0

**hermitdave/FrequencyWords**
Telif / Copyright (c) 2016 Hermit Dave
https://github.com/hermitdave/FrequencyWords
Kaynak veri / Source corpus: OpenSubtitles

Lisans / Licence: **Creative Commons Attribution-ShareAlike 4.0
International (CC BY-SA 4.0)**
https://creativecommons.org/licenses/by-sa/4.0/

Yukarı akış deposu lisansını şöyle beyan ediyor / The upstream repository
states its licence as:

> "MIT License for code.
>  CC-by-sa-4.0 for content."

Kullanılan dosyalar / Files used:

| Dosya / File | SHA-256 (LF) |
|---|---|
| `content/2018/tr/tr_50k.txt` | `480192844e7fdfe9591bbf0b9cfbb96ed5751cfbba7024fd45d8cb7508e07d5c` |
| `content/2018/en/en_50k.txt` | `5351ff405b1126ef555791dd4d9798a48e3e9a501a9fc481a9da957752cfb458` |

**DEĞİŞTİRİLDİ Mİ? EVET / MODIFIED? YES.** Listeler olduğu gibi
dağıtılmıyor: bağımsız bir sözlük kaynağıyla kesiştirildi, yalnız
kesişimde kalan maddeler alındı, ham sıklık sayıları atılıp yerine sıra
tutuldu. Ayrıntı `README.md`'de.

---

## 2. Türkçe sözlük / Turkish lexicon — Apache-2.0

**Zemberek-NLP**, `master-dictionary.dict`
Telif / Copyright Ahmet A. Akın
https://github.com/ahmetaa/zemberek-nlp

Lisans / Licence: **Apache License, Version 2.0**
https://www.apache.org/licenses/LICENSE-2.0

Apache-2.0 §4, türetilmiş işin dağıtımında telif, patent, ticari marka ve
atıf bildirimlerinin korunmasını istiyor; bu bildirim onu karşılıyor.
Lisansın tam metni uygulamanın "Lisanslar" ekranıyla da dağıtılıyor.

Apache-2.0 §4 requires retaining copyright, patent, trademark and
attribution notices in derivative works; this notice serves that purpose.
The full licence text also ships with the application's licence screen.

---

## 3. Portekizce sözlük / Portuguese lexicon — MPL-2.0 / LGPL-3.0

**pythonprobr/palavras** (`palavras.txt`)
https://github.com/pythonprobr/palavras

Asıl kaynak / Upstream source: LibreOffice **VERO** `pt_BR.dic`
(Verificador Ortográfico Livre 3.2)
Telif / Copyright (C) 2006–2013 Raimundo Santos Moura
<raimundo.smoura@gmail.com> ve Brezilya topluluğu / and the Brazilian
community

Lisans / Licence: **Mozilla Public License 2.0 VEYA/OR GNU Lesser General
Public License 3.0** (çift lisans / dual-licensed)
https://www.mozilla.org/MPL/2.0/
https://www.gnu.org/licenses/lgpl-3.0.html

Kaynağın kendi lisans metni şunu diyor / The source's own licence file
states:

> "This is a dictionary for spell correction and hyphenation for the
> Brazilian Portuguese language for hunspell. This is a free program and
> it can be redistributed and/or modified under the terms of the GNU
> Lesser General Public License (LGPL) version 3 and Mozilla Public
> License."

**DEĞİŞTİRİLDİ Mİ? EVET / MODIFIED? YES.** Sıklık listesiyle
kesiştirildi, özel adlar çıkarıldı, dil politikası uygulandı, sıra
eklendi.

---

## 4. İngilizce sözlük / English lexicon — kamu malı / public domain

**ENABLE** (`enable1.txt`) — Enhanced North American Benchmark Lexicon
Kamu malı / public domain.

Kamu malı olduğu için atıf yükümlülüğü **yok**; yine de yazılı, çünkü bir
varlığın nereden geldiği, yükümlülük **doğmadığını** göstermek
gerektiğinde de gerekiyor.

Being public domain, this source carries **no** attribution obligation. It
is recorded anyway: provenance matters just as much when it shows that no
obligation arises.

---

## Lisansların birlikte durması / Licence interaction

### Türkçe ve İngilizce tablolar

`tr_words.tsv` ve `en_words.tsv` **CC BY-SA 4.0** ile lisanslı, çünkü en
kısıtlayıcı kaynak şartı bu ve tablolar ondan türetilmiş uyarlamalar.
Apache-2.0 (Zemberek) ve kamu malı (ENABLE) kaynaklar buna izin veriyor;
ikisi de yeniden lisanslamayı engellemiyor, yalnız bildirimlerin
korunmasını istiyor — yukarıda korundular.

`tr_words.tsv` and `en_words.tsv` are licensed **CC BY-SA 4.0**, being
adaptations of the most restrictive source. The Apache-2.0 and
public-domain sources permit this.

### `pt_words.tsv` FARKLI: iki copyleft kaynak üst üste

Portekizce tablo **iki** copyleft kaynaktan türedi: sözlük
MPL-2.0/LGPL-3.0, sıklık CC BY-SA 4.0. Türkçe ve İngilizce'de sözlük
tarafı izin vericiydi, burada değil.

**Bu dosya için birleşik tek bir lisans iddia EDİLMİYOR.** Her katkı
kendi şartlarını taşıyor:

| Katkı | Kaynak | Lisans |
|---|---|---|
| Kelimelerin kendisi (geçerlilik) | palavras / VERO | MPL-2.0 / LGPL-3.0 |
| Sıra ve bant (sıklık) | FrequencyWords | CC BY-SA 4.0 |

Tek bir dosyanın aynı anda hem MPL hem CC BY-SA olduğunu söylemek
doğrulanabilir bir şey değil ve öyle bir iddiada bulunmuyoruz. İki
lisansın da istediği şey aynı yönde: **türetilmiş veri erişilebilir
olsun** — bu depo onu karşılıyor. İkisinin bir dosyada nasıl
birleştiği hukuk kontrolüne açık bir madde.

**We make no combined single-licence claim for this file.** Each
contribution carries its own terms, as tabled above. Both licences point
the same way — the derived data must remain available — and this
repository satisfies that. How the two compose in one file is an open
question left to legal review.

**Uygulamanın kendisi bu lisansların hiçbirine tabi değil** — CC BY-SA'nın
ShareAlike koşulu uyarlanan materyale ait, onu içeren daha büyük işe
değil. / **The application itself falls under none of these** — ShareAlike
binds the adapted material, not the larger work containing it.
