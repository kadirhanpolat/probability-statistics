# CLAUDE.md — Olasılık Teorisi ve Matematiksel İstatistik Projesi

## Proje Amacı

Matematik bölümü 3-4. yıl öğrencilerine yönelik, Türkiye Yüzyılı Maarif Modeli'ne (TYMM) uygun, iki bölümlü kapsamlı Türkçe ders kitabı oluşturmak. Part I: Olasılık Teorisi, Part II: Matematiksel İstatistik.

---

## Dizin Yapısı

```
probability-statistics/
├── CLAUDE.md              ← bu dosya
├── kaynaklar/             ← 16 referans PDF (tümü mevcut)
├── tasarim_belgeleri/     ← kitap tasarım kararları (v1.0 TAMAMLANDI)
│   ├── 00_PROJE_OZETI.md
│   ├── 01_ICINDEKILER_TASLAK.md
│   ├── 02_KAYNAK_ANALIZI.md
│   ├── 03_PEDAGOJIK_YAKLASIM.md
│   ├── 04_TERMINOLOJI_SOZLUGU.md
│   ├── 05_BOLUM_YAZIM_SABLONU.md  ← maarif.sty ortamları + alıştırma yapısı
│   ├── 06_YAZIM_SIRASI.md         ← bağımsızdan bağımlıya 19 bölüm sırası
│   └── 07_MAARIF_MODELI_UYUMU.md  ← TYMM pedagoji gereksinimleri
├── ornek_stil/            ← referans LaTeX dosyaları
│   ├── maarif.sty             — pedagojik kutular (kaynak)
│   └── topoloji.sty           — matematik ortamları şablonu
└── bolumler/              ← asıl LaTeX içerik (YAZIM AŞAMASINDA)
    ├── maarif.sty             — ornek_stil/'dan kopya
    ├── olasilik.sty           ← TEK YENİ: teorem ortamları + 50+ makro
    ├── main-ogrenci.tex       ← öğrenci PDF (alcozum gizli)
    ├── main-egitmen.tex       ← eğitmen PDF (alcozum görünür)
    ├── part1_olasilik/
    │   └── bolum00_onbilgiler.tex  ← SIRADAKI: yazılacak
    ├── part2_istatistik/
    └── ekler/
```

---

## Temel Tasarım Kararları

1. **Hedef kitle:** Matematik bölümü 3-4. yıl; gerçel analiz + lineer cebir biliyorlar.
2. **İki Part:** Part I tamamen olasılık (Böl. 0-10), Part II tamamen istatistik (Böl. 11-18).
3. **Her teorem ispatlanır** — "ispatsız verilir" yok.
4. **Dil:** Türkçe; her terimin ilk geçişinde İngilizce karşılığı parantez içinde.
5. **TYMM uyumu:** Her bölümde kazanım listesi + köprü kurma + disiplinlerarası bağlantı kutusu.
6. **Üç çıktı, tek kaynak:** `main-ogrenci.tex` / `main-egitmen.tex` / arşiv.
7. **Bayesian sınırı:** Böl. 12.7'de yalnızca konjugat önsel + sonsal + credible interval; Bayes hipotez testi kapsam dışı.

---

## LaTeX Altyapısı

### İki stil dosyası

| Dosya | Görev |
|---|---|
| `bolumler/maarif.sty` | Pedagojik kutular: motivasyon, kesif, kritiksorgu, tanimgerekce, hataanalizi, karsiornek, ispatiskele, kendinleifade, mikroozet, ozyansima, kopru, ipucu, alistirma, alcozum |
| `bolumler/olasilik.sty` | Teorem ortamları (tanim, teorem, lemma, sonuc…) + olasılık/istatistik makroları |

### Çift sürüm sistemi

```latex
\usepackage{maarif}            % öğrenci: \alcozum gizli
\usepackage[cozumler]{maarif}  % eğitmen: \alcozum görünür
```

### Bölüm sonu alıştırma yapısı

```latex
\cozumlualistirmalar   % çözümlü alıştırmalar başlığı
\begin{alistirma}[Al.N.1]{A}{Başlık} ... \end{alistirma}
\alcozum{Tam çözüm — her iki sürümde görünür}

\alistirmalar          % çözümsüz alıştırmalar başlığı
\begin{alistirma}[Al.N.5]{C}{Başlık} ... \end{alistirma}
\alcozum{Tam çözüm — YALNIZCA eğitmen PDF'inde}
```

### Önemli `olasilik.sty` makroları

```latex
\Prob        % P(A)
\Beklenti    % E[X]
\Var, \Cov, \Cor
\sigalg      % F (σ-cebiri)
\Borel       % B (Borel)
\olas{P}     % (Ω, F, P)
\iid         % i.i.d. ok
\asto        % n.k. ok
\pto         % P ok
\dto         % d ok
\Normal, \Pois, \Binom, \Gama, \Beta, \Exp, \Uniform
\Likh, \logLikh, \Fisher  % L, ℓ, I(θ)
\tahmin{θ}, \MLE{θ}, \UMVUE{θ}
\gostf{A}    % 1_A gösterge fonksiyonu
```

---

## Bölüm Yazım Şablonu — Standart Akış

```
\begin{kazanimlar}          % TYMM: 5-7 ölçülebilir madde
\begin{motivasyon}          % + köprü kurma paragrafı (TYMM)
[Tarihsel Not — opsiyonel]
  §N.k. Alt bölüm
    \begin{kesif}           % tanımdan önce keşif
    \begin{tanimgerekce}    % neden bu tanım böyle?
    \begin{tanim}           % tanım
    \begin{kritiksorgu}     % koşul kalkarsa?
    \begin{teorem} + proof  % teorem + ispat
    \begin{ispatiskele}     % B-seviyesi için
    \begin{hataanalizi}     % sık hata
    \begin{karsiornek}      % karşı örnek
    disiplinlerarası bağlantı kutusu (TYMM)
    \begin{kendinleifade}
    \begin{mikroozet}
\begin{ozyansima}           % bölüm sonu
\begin{kopru}               % ileri okuma + sonraki bölüm
\cozumlualistirmalar + \alistirmalar
```

---

## Terminoloji (Özet)

| Türkçe | İngilizce | Not |
|---|---|---|
| Rasgele değişken | random variable | "rassal" değil |
| Beklenti | expected value | "beklenen değer" değil |
| Neredeyse kesin | almost surely | kısaltma: n.k. |
| Olabilirlik | likelihood | "olasılık" değil |
| Yeterli istatistik | sufficient statistic | |
| Tahmin edici | estimator | |

Tam liste: `04_TERMINOLOJI_SOZLUGU.md`

---

## Kaynak Kitaplar (`kaynaklar/` klasöründe mevcut)

Feller Vol.I & II, Kolmogorov, Gnedenko, Billingsley, Shiryaev 1 & 2,
Durrett, Williams, Klenke, Hogg-Craig, Casella-Berger,
Lehmann-Casella, Lehmann-Romano, Mood et al., Akdeniz.
Bölüm-kaynak eşlemesi: `02_KAYNAK_ANALIZI.md §8`

---

## Mevcut Durum (2026-05-30)

**Tamamlananlar:**
- Tasarım belgeleri v1.0 (7 belge)
- LaTeX altyapısı: `olasilik.sty`, `maarif.sty` (güncellenmiş), `main-ogrenci.tex`, `main-egitmen.tex`
- Yazım sırası kararlaştırıldı (19 bölüm, bağımsızdan bağımlıya)

**Siradaki adım:**
- `bolumler/part1_olasilik/bolum00_onbilgiler.tex` — **Bölüm 0'ı yaz**

---

## Bölüm Yazım Sırası (Özet)

1→ Böl.0, 2→ Böl.1, 3→ Böl.2, 4→ Böl.3, 5→ Böl.4,
6→ Böl.5, 7→ Böl.7, 8→ Böl.6, 9→ Böl.8, 10→ Böl.11,
11→ Böl.9*, 12→ Böl.12, 13→ Böl.10*, 14→ Böl.13,
15→ Böl.14, 16→ Böl.17*, 17→ Böl.18*, 18→ Böl.15, 19→ Böl.16

Detay: `tasarim_belgeleri/06_YAZIM_SIRASI.md`

---

## PDF Okuma Notu

```python
import fitz
doc = fitz.open("kaynaklar/Olasilik ve Istatistik - Fikri Akdeniz - Edisyon 18 - 2013.pdf")
page = doc[sayfa_no]  # 0-indexed; toplam 617 sayfa
text = page.get_text()
```
