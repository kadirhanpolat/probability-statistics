# CLAUDE.md — Olasılık Teorisi ve Matematiksel İstatistik Projesi

## Proje Amacı

Matematik bölümü öğrencilerine yönelik, iki bölümlü (Part I: Olasılık Teorisi, Part II: Matematiksel İstatistik) kapsamlı bir Türkçe ders kitabı oluşturmak.

## Dizin Yapısı

```
probability-statistics/
├── CLAUDE.md              ← bu dosya
├── README.md              ← proje özeti (kullanıcı için)
├── kaynaklar/             ← referans PDF'ler
│   └── Olasilik ve Istatistik - Fikri Akdeniz - Edisyon 18 - 2013.pdf
├── tasarim_belgeleri/     ← kitap tasarım kararları (TAMAMLANDI v1.0)
│   ├── 00_PROJE_OZETI.md              — proje felsefesi ve kapsamı
│   ├── 01_ICINDEKILER_TASLAK.md       — 18 bölümlük içindekiler + kaynak haritası
│   ├── 02_KAYNAK_ANALIZI.md           — ~20 referans kitap; tam içindekiler
│   ├── 03_PEDAGOJIK_YAKLASIM.md       — bölüm yapısı, ispat felsefesi, problem seviyeleri
│   ├── 04_TERMINOLOJI_SOZLUGU.md      — Türkçe-İngilizce terim sözlüğü
│   └── 05_BOLUM_YAZIM_SABLONU.md      — bölüm yapısı ve tipografi şablonu
├── bolumler/              ← (oluşturulacak) asıl LaTeX içerik
│   ├── part1_olasilik/
│   └── part2_istatistik/
└── ekler/                 ← (oluşturulacak) tablolar, ekler
```

## Temel Tasarım Kararları

1. **Hedef kitle:** Matematik bölümü 3-4. yıl öğrencileri; gerçel analiz ve lineer cebir biliyorlar.
2. **İki Part:** Part I tamamen olasılık, Part II tamamen istatistik.
3. **Ölçüm teorisi:** Bölüm 1'de tanıtılır; kitap boyunca gerektiğinde kullanılır ama ön koşul değildir.
4. **Her teorem ispatlanır.** "İspatsız verilir" yok.
5. **Dil:** Türkçe; her terimin ilk geçişinde İngilizce karşılığı parantez içinde.
6. **Problem seviyeleri:** A (temel), B (orta), C (ileri/araştırma).

## Tasarım Belgelerine Bakış

- `00_PROJE_OZETI.md` — Projenin neden var olduğu, felsefesi, kapsamı, kapsam dışı
- `01_ICINDEKILER_TASLAK.md` — 18 bölümlük detaylı içindekiler + bölüm-kaynak haritası (v0.3)
- `02_KAYNAK_ANALIZI.md` — ~20 referans kitabın tam içindekiler ve karşılaştırma tablosu (v1.0)
- `03_PEDAGOJIK_YAKLASIM.md` — Bölüm mimarisi, ispat felsefesi, ders programı seçenekleri
- `04_TERMINOLOJI_SOZLUGU.md` — Türkçe-İngilizce terim sözlüğü; tartışmalı çeviriler; notasyon
- `05_BOLUM_YAZIM_SABLONU.md` — Tanım/Teorem/İspat kutu şablonları; LaTeX ortamları; dil kuralları

## Terminoloji Kuralları

- Rasgele değişken (random variable) — "rassal" değil
- Beklenti (expected value) — "beklenen değer" değil
- Olabilirlik fonksiyonu (likelihood function)
- Yeterli istatistik (sufficient statistic)
- Neredeyse kesin (almost surely, a.s. → n.k.)
- Tam terminoloji listesi: `04_TERMINOLOJI_SOZLUGU.md`

## PDF Okuma Notu

Akdeniz kitabı PyMuPDF ile okunabilir:
```python
import fitz
doc = fitz.open("kaynaklar/Olasilik ve Istatistik - Fikri Akdeniz - Edisyon 18 - 2013.pdf")
page = doc[sayfa_no]  # 0-indexed
text = page.get_text()
```
Toplam sayfa: 617. Kaynakça: sayfa 614-615 (0-indexed: 613-614).

## Araştırma Kaynakları

Referans kitaplar için web araştırması yapıldı. Detaylar `02_KAYNAK_ANALIZI.md`'de.

## Mevcut Durum (2026-05-29)

Tasarım belgeleri v1.0 olarak tamamlandı:
- 3 araştırma ajanı çalıştırıldı; klasik + modern olasılık ve istatistik kitapları araştırıldı
- Tam içindekiler ve kaynak analizi entegre edildi
- Terminoloji sözlüğü ve bölüm yazım şablonu hazırlandı

## Sonraki Adımlar

1. Pilot bölüm taslağı: Bölüm 2 (Olasılık Uzayları) — LaTeX ile yazılmaya başlanabilir
2. LaTeX şablonu oluşturulacak (`bolumler/` klasörü)
3. İçindekiler taslağını güncelleyip kesinleştirme (özellikle Bölüm 3 Klasik İstatistik kısmı)
