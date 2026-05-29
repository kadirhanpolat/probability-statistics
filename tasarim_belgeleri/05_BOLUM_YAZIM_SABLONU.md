# Bölüm Yazım Şablonu — Olasılık Teorisi ve Matematiksel İstatistik

> Bu belge, kitabın her bölümü için uyulacak yapıyı, tipografi kurallarını ve içerik kalıplarını tanımlar.

---

## 1. Bölüm Kapağı

```
═══════════════════════════════════════════════════════
BÖLÜM [N]

[BÖLÜM BAŞLIĞI]

"[Seçilmiş alıntı — matematikçi ya da düşünür]"
                                        — Ad Soyad (yıl)

Ön Koşullar: Bölüm X, Bölüm Y
Tahmini Okuma Süresi: ~ [n] saat
═══════════════════════════════════════════════════════
```

---

## 2. Motivasyon (1-3 Sayfa)

**Amaç:** Öğrencinin "neden bu bölümü öğreniyorum?" sorusunu yanıtlamak.

**Yapı:**
1. Somut bir problem ya da paradoks (matematiksel ya da gerçek hayattan)
2. "Bu bölümde şunları öğreneceğiz..." (madde listesi — 5-7 madde)
3. Bu bölümün kitabın genel yapısındaki yeri (1 cümle)

**Örnek kalıp:**
> Bir saati boyunca gelecek olan yolcu sayısını tahmin etmek istiyorsunuz...  
> Bu bölümde şunları öğreneceğiz:  
> — Rasgele bir değişkenin beklentisinin Lebesgue integrali olarak nasıl tanımlandığını  
> — Beklentinin önemli özellikleri ve eşitsizlikleri  
> — ...

---

## 3. Tarihsel Not (Opsiyonel, 0.5-1 Sayfa)

```
┌──────────────────────────────────────────────────────┐
│ TARİHSEL NOT                                         │
│                                                      │
│ [Konu ile ilgili tarihi arka plan; konuyu geliştiren │
│ matematikçiler; tarihsel motivasyon]                 │
│                                                      │
│ Kaynaklar: [...]                                     │
└──────────────────────────────────────────────────────┘
```

---

## 4. Ana İçerik Yapısı

### 4.1. Tanım Kutusu

```
╔══════════════════════════════════════════════════════╗
║ TANIM N.k — [Tanım Adı]                              ║
║                                                      ║
║ [Matematiksel tanım]                                 ║
║                                                      ║
║ [Eğer varsa: "Buna ... da denir."]                   ║
╚══════════════════════════════════════════════════════╝
```

**Kurallar:**
- Her tanımın bir numarası var: N bölüm numarası, k sıra numarası
- Tanım yalnızca matematiksel içerik; motivasyon önceden verilmiş olmalı
- İngilizce terim parantez içinde, tanımın ilk satırında

### 4.2. Teorem Kutusu

```
╔══════════════════════════════════════════════════════╗
║ TEOREM N.k — [Teorem Adı]                            ║
║                                                      ║
║ [Hipotezler (Varsayımlar)]                           ║
║                                                      ║
║ [Sonuç / İddia]                                      ║
╚══════════════════════════════════════════════════════╝
```

**Kurallar:**
- Her teoremin hemen ardından ispat gelir
- İspat "İspat." başlığı ile açılır, "□" ile kapanır
- İspat birden fazla adım içeriyorsa numaralandırılır: **Adım 1, Adım 2, ...**

### 4.3. İspat Yapısı

```
İspat.
[Fikir: Bu teoremin neden doğru olduğuna dair sezgisel açıklama — 1-2 cümle]

[Tam ispat:]
  Adım 1. ...
  Adım 2. ...
  ...
□
```

**Kurallar:**
- "Fikir:" kısmı zorunludur; matematiği "kara büyü" gibi göstermez
- Her adım kendi paragrafında
- Uzun ispatlar lemmalar ile bölünür

### 4.4. Lemma

```
LEMMA N.k — [Lemma Adı]
[İçerik]
İspat. [...] □
```

Lemma, teoremin ispatında kullanılan ara sonuçtur.

### 4.5. Sonuç (Corollary)

```
SONUÇ N.k — [Sonuç Adı]
[Teoremin özel bir durumu ya da doğrudan çıkarımı]
İspat. Teorem N.j'den doğrudan elde edilir. □
```

### 4.6. Önerme (Proposition)

Teorem kadar önemli olmayan ama ispatlanması gereken sonuçlar için:

```
ÖNERME N.k
[İçerik]
İspat. [...] □
```

### 4.7. Uyarı Kutusu

```
┌──────────────────────────────────────────────────────┐
│ ⚠ UYARI                                              │
│                                                      │
│ [Sık yapılan hata, dikkat edilmesi gereken incelik,  │
│ ya da karşı-örnek]                                   │
└──────────────────────────────────────────────────────┘
```

### 4.8. Not Kutusu

```
┌──────────────────────────────────────────────────────┐
│ NOT                                                  │
│                                                      │
│ [Ek bilgi, bağlantı, yorum]                          │
└──────────────────────────────────────────────────────┘
```

### 4.9. Geometrik / Sezgisel Yorum Kutusu

```
┌──────────────────────────────────────────────────────┐
│ SEZGİSEL YORUM                                       │
│                                                      │
│ [Bu sonucun geometrik, grafik ya da fiziksel          │
│ yorumu]                                              │
└──────────────────────────────────────────────────────┘
```

---

## 5. Çözümlü Örnekler (Her Bölümde En Az 8 Örnek)

### Örnek Başlığı

```
Örnek N.k.
[Problem ifadesi]

Çözüm.
[Adım adım çözüm]

[Yorum (gerekliyse): Bu sonuç ... anlamına gelir.]
```

**Seviye dağılımı:**
- Örneklerin ~40%'ı A seviyesi (doğrudan tanım uygulaması)
- ~40%'ı B seviyesi (birden fazla kavramı birleştiren)
- ~20%'si C seviyesi (ispat veya ileri analiz gerektiren)

---

## 6. Bölüm Sonu Özeti (0.5 Sayfa)

```
─────────────────────────────────────────────────────
BÖLÜM ÖZETİ

Bu bölümde öğrendiklerimiz:
• [Kavram 1]: ...
• [Kavram 2]: ...
• [Önemli teorem]: ...
• [Önemli bağlantı]: ...

Notasyon özeti:
  [simge] — [açıklama]
  ...
─────────────────────────────────────────────────────
```

---

## 7. Problemler

### Yapı

```
PROBLEMLER

— A Seviyesi (Temel) ————————————————————————

A.1. [Problem ifadesi]
A.2. [Problem ifadesi]
...

— B Seviyesi (Orta) —————————————————————————

B.1. [Problem ifadesi]
B.2. [Problem ifadesi]
...

— C Seviyesi (İleri / Araştırma) ————————————

C.1. [İspat gerektiren problem]
C.2. [Araştırma sorusu veya açık problem]
...
```

### Problem Yazım Kuralları

- Her A ve B seviyesi problemi bir yanıt veya kısa çözüm içerir (kitap sonunda)
- C seviyesi problemleri yalnızca ipucu içerir (tam çözüm değil)
- Bazı problemler "Bu sonucu kendi başınıza kanıtlayın" niteliğinde teorem ispat problemleri olabilir
- Bazı problemler önceki bölüm kavramlarını bu bölümdekilerle birleştirir

### Minimum Problem Sayısı

| Bölüm türü | A Seviyesi | B Seviyesi | C Seviyesi | Toplam |
|---|---|---|---|---|
| Teori ağırlıklı (Böl. 1-9) | 8 | 8 | 4 | 20 |
| İstatistik ağırlıklı (Böl. 11-16) | 10 | 10 | 5 | 25 |

---

## 8. Bölüm Başı Ön Koşul Tablosu

Her bölümün başında:

```
┌──────────────────────────────────────────────────────┐
│ BU BÖLÜMÜ OKUMADAN ÖNCE                              │
│                                                      │
│ Bilinmesi gerekenler:                                │
│  □ Gerçel analiz: limit, süreklilik, Riemann integ.  │
│  □ Bölüm 1: σ-cebiri, Lebesgue integrali            │
│  □ Bölüm 2: Olasılık uzayı, bağımsızlık             │
│                                                      │
│ Bu bölümün kullanıldığı sonraki bölümler:            │
│  → Bölüm 4 (beklenti için)                          │
│  → Bölüm 11 (örneklem dağılımları için)             │
└──────────────────────────────────────────────────────┘
```

---

## 9. İçerik Sırası — Standart Akış

```
[Bölüm Kapağı]
[Motivasyon]
[Tarihsel Not — isteğe bağlı]
  §N.1. [Alt bölüm başlığı]
    [Tanımlar]
    [Teoremler + İspatlar]
    [Örnekler A/B/C]
    [Uyarı/Not kutuları]
  §N.2. [...]
  ...
[Bölüm Özeti]
[Problemler: A / B / C]
[Kaynaklar ve İleri Okuma]
```

---

## 10. Tipografi Notları (LaTeX için)

```latex
% Tanım
\begin{definition}[Tanım Adı]
  ...
\end{definition}

% Teorem
\begin{theorem}[Teorem Adı]
  ...
\end{theorem}
\begin{proof}
  \textbf{Fikir:} ...
  
  \textbf{Adım 1.} ...
\end{proof}

% Uyarı kutusu
\begin{warning}
  ...
\end{warning}

% Sezgisel yorum
\begin{intuition}
  ...
\end{intuition}

% Örnek
\begin{example}
  ...
  \begin{solution}
    ...
  \end{solution}
\end{example}
```

Tüm bu ortamlar kitabın LaTeX şablonunda tanımlanacak.

---

## 11. Dil ve Üslup Kuralları

1. **Cümle uzunluğu:** Teoremler ve tanımlar için kısa, kesin cümleler. Açıklamalar için biraz daha uzun ama aşırıya kaçmadan.

2. **Aktif ifadeler:** "Kanıtlıyoruz" değil "kanıtlayacağız"; "gösterilir" değil "göstereceğiz" — okuyucuyu dahil eden üslup.

3. **"Açıktır ki" ve "kolayca görülür" ifadelerinden kaçın:** Her adım açıklanır.

4. **Soru cümleleri:** İspatın ara noktalarında "Peki neden...?" şeklinde sorular sorun — öğrenci gibi düşünün.

5. **İlk geçiş kuralı:** Her teknik terimin Türkçe adı ilk kullanımda İngilizce karşılığıyla birlikte verilir: *yeterli istatistik (sufficient statistic)*.

6. **Dipnot politikası:** Kısa açıklamalar ve terminoloji notları için dipnot. Tarihsel notlar ve genişlemeler için kutu veya bölüm sonu notu.
