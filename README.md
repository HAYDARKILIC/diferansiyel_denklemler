# Bilim İnsanları ve Mühendisler için Diferansiyel Denklemler

> **Adi ve Kısmi Diferansiyel Denklemler üzerine araştırma düzeyinde, 8 haftalık bir ustalık kursu — ilk ilkelerden modern makine öğrenmesi uygulamalarına.**
> Sembolik çözücü yok. Kara kutu kütüphane yok. Saf matematik, NumPy ve SciPy.

---

## Genel Bakış

Bu kurs, klasik teoriyi modern bilimsel hesaplama ve makine öğrenmesiyle birleştirerek diferansiyel denklemlerin eksiksiz bir anlayışını sıfırdan kurar. Her hafta; titiz türetmeler, elle yazılmış sayısal uygulamalar ve zengin görselleştirmelerle dolu, kendi içinde bütün bir Jupyter Notebook'tur.

Sonunda şunları türetmiş, uygulamış ve sınamış olacaksınız:

- Her büyük **ADD çözücüsü** (Euler, RK4, Adams-Bashforth, BDF, Radau) sıfırdan
- Özdeğer spektrumları ve faz portreleri yoluyla **kararlılık analizi**
- Atış yöntemleri ve sonlu farklarla **Sınır Değer Problemleri**
- Elle yazılmış DFT ve FFT çekirdekleriyle **Fourier Serileri ve Dönüşümleri**
- Fiziğin kanonik **KDD'leri**: ısı, dalga, Laplace ve Burgers denklemleri
- **Katı sistemler** ve sayısal patolojileri (katılık oranı, A-kararlılık)
- NumPy'da sıfırdan **Sinirsel ADD'ler** ve **Fizik-Bilgili Sinir Ağları (PINN)**

---

## Depo Yapısı

```
diferansiyel_denklemler/
│
├── hafta1/   01_birinci_mertebe_oddler.ipynb          # Ayrılabilir, doğrusal, Bernoulli, tam, homojen ADD'ler
├── hafta2/   02_ikinci_mertebe_ve_sistemler.ipynb     # Karakteristik denklemler, faz düzlemleri, sistemler
├── hafta3/   03_sayisal_yontemler.ipynb               # Euler, RK4, AB/AM çok adımlı, hata analizi
├── hafta4/   04_kati_sistemler_ve_sdp.ipynb           # Katılık, BDF/Radau, atış ve SF ile SDP
├── hafta5/   05_fourier_ve_laplace.ipynb              # Fourier serileri, sıfırdan DFT/FFT, Laplace dönüşümleri
├── hafta6/   06_kdd_isi_ve_dalga.ipynb                # Isı denklemi (FTCS/CN), dalga denklemi (sıçrama)
├── hafta7/   07_kdd_eliptik_ve_burgers.ipynb          # Laplace (SOR), Burgers (şok yakalama)
└── hafta8/   08_sinirsel_oddler_ve_pinnler.ipynb      # Neural ODE eşlenik yöntemi, sıfırdan KDD için PINN
```

---

## Haftalık Müfredat

| Hafta | Konu | Temel Uygulamalar |
|------|-------|---------------------|
| 1 | **Birinci Mertebeden ADD'ler** | İntegral çarpanı, tam ADD çözücüsü, Bernoulli dönüşümü, homojen denklemler, yön alanları |
| 2 | **İkinci Mertebeden ADD'ler ve Sistemler** | Karakteristik kökler, Wronskian, kuvvet serileri, parametrelerin değişimi, özdeğer faz portreleri |
| 3 | **ADD'ler için Sayısal Yöntemler** | Sıfırdan Euler/Orta nokta/RK4, yerel kesme hatası, küresel hata yakınsama grafikleri, Adams-Bashforth/Moulton |
| 4 | **Katı Sistemler ve SDP'ler** | Katılık oranı analizi, kapalı Euler, atış yöntemi, sonlu fark SDP'leri, Thomas algoritması |
| 5 | **Fourier ve Laplace Dönüşümleri** | Elle yazılmış DFT O(N²), Cooley-Tukey FFT O(N log N), Gibbs olayı, Bode grafikleri |
| 6 | **KDD'ler: Isı ve Dalga** | 1B ısı (FTCS, Crank-Nicolson), CFL koşulu, 1B dalga (sıçrama), d'Alembert çözümü |
| 7 | **Eliptik KDD'ler ve Burgers** | 2B Poisson, Jacobi/Gauss-Seidel/SOR, şok oluşumu, viskozlu/viskozitesiz Burgers |
| 8 | **Sinirsel ADD'ler ve PINN'ler** | Sıfırdan eşlenik duyarlılık, PyTorch Neural ODE, otomatik türevle PINN |

---

## Kurulum

```bash
pip install numpy scipy matplotlib jupyter
pip install torch    # yalnızca Hafta 8 için gerekli
```

Notebook'ları çalıştırmak için:

```bash
jupyter notebook
```

---

## Felsefe

Her yöntem **kodlanmadan önce türetilir**. Her sayısal uygulama, analitik bir çözüme veya bilinen bir referansa karşı **doğrulanır**. Amaç yalnızca diferansiyel denklemleri çözmek değil, çözücülerin *neden* çalıştığını — ve ne zaman başarısız olduğunu — anlamaktır.
