# 🖼️ COM0418 - Image Processing Laboratuvar Çalışmaları

## 🎓 İstanbul Kültür Üniversitesi - Bilgisayar Mühendisliği Bölümü

Bu repository, **COM0418 - Image Processing** dersi kapsamında gerçekleştirilen laboratuvar çalışmalarını içermektedir.

---

## 📚 Laboratuvar İçerikleri

### 🔬 Lab 2 - NumPy Arrays, Image I/O & Bit-Plane Steganography
Bu laboratuvar, NumPy dizileri, MATLAB test görüntüleri, OpenCV I/O, veri tipleri, görüntü gösterimi ve bit-plane steganografi konularını kapsamaktadır.

- **📄 Dosyalar:**
  - `COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb` - Öğrenci notebook'u (**30 exercise + review cevapları + extra work**)
  - `COM0418_ImageProcessing_Week2_Lab_Instructor_Guided.pdf` - Instructor kılavuzu / PDF
  - `matlab_test_images/` - MATLAB örnek görüntülerinin yerel kopyaları
  - `week2_lab_output/` - Notebook çalıştırılınca üretilen çıktılar (PNG/JPEG)

- **📁 Test Görüntüleri (`matlab_test_images/`):**
  - `cameraman.tif` - Gri seviye görüntü (binary, data type, bit-plane, LSB steganografi)
  - `baby.jpg` - True-color görüntü (OpenCV ile okuma)
  - `sherlock.jpg` - True-color görüntü (Pillow ile karşılaştırma)
  - `trees.tif` - Indexed / palette renkli görüntü
  - `astronaut_rgb.png`, `camera_gray.png`, `camera_binary.png`, `gradient16.png`, `indexed_palette.gif` - Ek örnek görüntüler

#### ✅ Notebook İçeriği
| Bölüm | Konu | Exercise |
|---|---|---|
| 1 | NumPy arrays (list→array, create, indexing, view/copy) | 01–04 |
| 2 | Grayscale + ROI (`cameraman.tif`) | 05–07 |
| 3 | Binary threshold | 08 |
| 4 | True-color BGR vs RGB + Pillow | 09–12 |
| 5 | Indexed / palette (`trees.tif`) | 13–15 |
| 6 | Data types & arithmetic | 16–20 |
| 7 | Display & save | 21–23 |
| 8 | Bit planes | 24–25 |
| 9 | LSB steganography | 26–30 |
| 10 | Review answers + extra work | notebook sonu |

#### 📦 Bölüm 1 - NumPy Arrays for Image Processing
- Python list → NumPy array dönüşümü
- Array oluşturma (`arange`, `zeros`, `ones`, random)
- Shape, dtype, reshape
- Indexing ve slicing
- View vs copy ve ROI (Region of Interest) değiştirme

#### ⬛ Bölüm 2 - Grayscale Images
- `cameraman.tif` okuma (`cv2.IMREAD_GRAYSCALE`)
- Matplotlib ile gri seviye görüntü gösterme (`cmap='gray'`, `vmin`/`vmax`)
- NumPy slicing ile ROI seçimi

#### ⚪ Bölüm 3 - Binary Images
- Threshold ile binary görüntü üretme (`cv2.threshold`)
- 0/255 ve 0/1 temsilleri

#### 🎨 Bölüm 4 - True-Color Images (BGR vs RGB)
- OpenCV ile `baby.jpg` okuma (BGR)
- Matplotlib için kanal sırasını düzeltme (`cv2.cvtColor`)
- RGB kanallarını ayırma ve inceleme
- Pillow ile `sherlock.jpg` okuma (RGB)

#### 🗺️ Bölüm 5 - Indexed / Palette Images
- Pillow ile `trees.tif` palette inceleme
- Indexed görüntüyü RGB'ye çevirip gösterme
- OpenCV'nin indexed görüntüyü nasıl genişlettiğini karşılaştırma

#### 🔢 Bölüm 6 - Data Types & Arithmetic
- `uint8` ↔ float dönüşümleri
- Normalize edilmiş float → `uint8`
- 16-bit dönüşüm
- NumPy overflow vs OpenCV saturated arithmetic

#### 🖥️ Bölüm 7 - Display & Save
- Matplotlib ile notebook içi görüntüleme
- `cv2.imshow` ile GUI gösterimi
- OpenCV ile görüntü kaydetme (`week2_lab_output/`)

#### 🧩 Bölüm 8 - Bit Planes
- 8-bit gri görüntünün bit-plane'lerini çıkarma
- Seçili bit-plane'lerden görüntü yeniden oluşturma

#### 🕵️ Bölüm 9 - LSB Steganography
- LSB düzlemine mesaj gömme / çıkarma (`embed_lsb`, `extract_lsb`)
- Değişimi ölçme (MSE, PSNR) ve görselleştirme
- Stego görüntüyü PNG olarak kaydetme / yeniden yükleme

#### 📝 Bölüm 10 - Review & Extra Work
- 8 review sorusunun cevapları (notebook içinde markdown)
- Extra work kod hücreleri:
  - Farklı threshold değerleri
  - BGR vs RGB karşılaştırma
  - `trees.tif` index ROI + palette
  - Sadece bit 5–7 ile rekonstrüksiyon
  - Farklı mesaj uzunlukları vs değişen piksel sayısı
  - JPEG ile stego testi (LSB’nin bozulması)

- **🎯 Öğrenilen Konular:**
  - NumPy dizilerini oluşturma, indeksleme, dilimleme ve kopyalama
  - Görüntüyü NumPy array olarak yorumlama
  - Binary, grayscale, true-color/RGB ve indexed-color görüntü okuma
  - OpenCV (BGR) ile Matplotlib/Pillow (RGB) kanal sırası farkı
  - Görüntü veri tiplerini güvenli dönüştürme
  - Matplotlib ve OpenCV ile görüntü gösterme / kaydetme
  - 8-bit gri görüntünün bit-plane'lerini çıkarma
  - LSB (Least Significant Bit) ile basit steganografi demosu

> **Not:** Steganografi mesajın *varlığını* gizler; şifreleme değildir. Bu teknikleri yalnızca izin verilen veriler üzerinde kullanın.

---

### 🔬 Lab 3 - Point Processing, Histograms & Lookup Tables
Bu laboratuvar, noktasal işlemler (`y = f(x)`), aritmetik işlemler, histogram, contrast stretching, histogram equalization ve lookup table konularını kapsamaktadır.

- **📄 Dosyalar:**
  - `COM0418_ImageProcessing_Week3_Lab_Student.ipynb` - Öğrenci notebook'u (**13 exercise + review cevapları + 4 extra work**)
  - `tiles.png`, `pout.tif`, `tire.tif` - Notebook ile aynı klasördeki test görüntüleri

- **📁 Test Görüntüleri:**
  - `tiles.png` - Parlaklık, aritmetik, complement / solarization
  - `pout.tif` - Düşük kontrastlı görüntü (histogram, stretching, equalization, CLAHE)
  - `tire.tif` - Histogram ve LUT örnekleri; iki görüntü aritmetiği

#### ✅ Notebook İçeriği
| Bölüm | Konu | Exercise |
|---|---|---|
| 1 | Test görüntülerini okuma ve gösterme | 01 |
| 2 | Brightness (add / subtract) | 02 |
| 3 | NumPy overflow vs OpenCV saturation | 03 |
| 4 | Multiplication, division, affine (`convertScaleAbs`) | 04 |
| 5 | Complement ve partial complement | 05 |
| 6 | İki görüntü aritmetiği (add, subtract, blend) | 06 |
| 7 | Grayscale histogram (`calcHist`) | 07 |
| 8 | Contrast stretching (`normalize`) | 08 |
| 9 | Manuel contrast stretching formülü | 09 |
| 10 | Histogram equalization (`equalizeHist`) | 10 |
| 11 | Küçük matriste manuel equalization (CDF → LUT) | 11 |
| 12 | Lookup tables (`cv2.LUT`) | 12 |
| 13 | Stretching vs equalization karşılaştırması | 13 |
| 14 | Review answers + extra work | notebook sonu |

#### ✨ Bölüm özeti
- **Point processing:** Her çıktı pikseli yalnızca aynı konumdaki girdi pikselinden üretilir
- **Aritmetik:** `cv2.add` / `cv2.subtract` saturation; NumPy `uint8` overflow
- **Affine dönüşüm:** `y = αx + β` (`cv2.convertScaleAbs`)
- **Complement:** Tam ve kısmi invert (solarization benzeri etki)
- **Histogram:** Parlaklık ve kontrastın frekans dağılımı olarak yorumlanması
- **Contrast stretching:** Min–max aralığını 0…255’e doğrusal açma
- **Histogram equalization:** CDF tabanlı yeniden dağıtım
- **LUT:** Negatif, threshold, gamma dönüşümleri (`cv2.LUT`)

#### 📝 Bölüm 14 - Review & Extra Work
- 7 review sorusunun kısa cevapları (notebook içinde markdown)
- Extra work kod hücreleri:
  - `tire` ve `tiles` üzerinde histogram equalization
  - Gamma LUT’ları: 0.4, 0.8, 1.5, 2.0
  - Partial complement: `<80`, `<128`, `>180`
  - `equalizeHist` vs CLAHE (`cv2.createCLAHE`) karşılaştırması

- **🎯 Öğrenilen Konular:**
  - Noktasal işlemleri (`y = f(x)`) uygulama
  - OpenCV saturation ile NumPy overflow farkını açıklama
  - Parlaklık, ölçekleme, complement ve iki görüntü aritmetiği
  - Histogram okuma ve yorumlama
  - Contrast stretching ve histogram equalization farkı
  - CDF’den equalization LUT’u üretme
  - `cv2.LUT` ile hızlı point transform
  - CLAHE ile lokal kontrast iyileştirme

---

## 🚀 Nasıl Kullanılır

1. **📥 Repository'yi klonlayın:**
   ```bash
   git clone https://github.com/OnurAkyuz61/COM0418-ImageProcessing.git
   cd COM0418-ImageProcessing
   ```

2. **📂 İlgili laboratuvar klasörüne gidin:**
   ```bash
   cd "Lab 2"   # veya: cd "Lab 3"
   ```

3. **🐍 Ortamı hazırlayın (Anaconda önerilir):**
   ```bash
   conda activate imagepr_env
   jupyter lab
   ```

   Anaconda yoksa alternatif:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Windows: .venv\Scripts\activate
   pip install jupyterlab numpy matplotlib opencv-python pillow
   jupyter lab
   ```

4. **📓 Notebook'u açın:**
   - Lab 2: `COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb`
   - Lab 3: `COM0418_ImageProcessing_Week3_Lab_Student.ipynb`
   - Önce setup hücrelerini çalıştırın
   - Exercise hücrelerini sırayla **Shift+Enter** ile çalıştırın
   - En sonda **Review answers** ve **Extra work** hücrelerini çalıştırın

5. **🖼️ Test görüntüleri:**
   - **Lab 2:** Lab bilgisayarlarında öncelik MATLAB image data dizinidir; yoksa `matlab_test_images/` fallback kullanılır
   - **Lab 3:** `tiles.png`, `pout.tif`, `tire.tif` notebook ile aynı klasörde olmalıdır

6. **💾 Çıktılar:**
   - Lab 2 kaydedilen görüntüler `week2_lab_output/` altına yazılır
   - Lab 3 sonuçları notebook içinde görüntülenir

---

## 📋 Gereksinimler

### 🖥 Genel Gereksinimler
- Python 3.x (Anaconda / Miniconda önerilir)
- JupyterLab veya Jupyter Notebook
- Temel Python bilgisi

### 📦 Ana Kütüphaneler
- NumPy
- OpenCV (`opencv-python`)
- Matplotlib
- Pillow (PIL) — özellikle Lab 2

### 🧪 Ortam (ders laboratuvarı)
- Anaconda environment: `imagepr_env`
- (İsteğe bağlı, Lab 2) MATLAB image toolbox örnek görüntüleri

---

## 🎯 Öğrenme Hedefleri

Bu laboratuvar çalışmaları ile öğrenciler:

- ✅ Görüntüleri NumPy dizileri olarak işler
- ✅ OpenCV ve Pillow ile görüntü okuma/yazma yapar
- ✅ Gri, binary, renkli ve indexed görüntü türlerini ayırt eder
- ✅ BGR / RGB kanal sırası farkını açıklar ve düzeltir
- ✅ Görüntü veri tiplerini güvenli şekilde dönüştürür
- ✅ Matplotlib ve OpenCV ile görüntü gösterir
- ✅ Bit-plane analizi ve LSB steganografi temelini uygular
- ✅ Noktasal işlemler, aritmetik ve complement uygular
- ✅ Histogram, contrast stretching ve equalization kullanır
- ✅ Lookup table (`cv2.LUT`) ve CLAHE ile point processing yapar
- ✅ Lab review sorularını ve extra work deneylerini notebook üzerinde tamamlar

---

## 📁 Repo Yapısı

```
COM0418-ImageProcessing/
├── Lab 2/
│   ├── COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb
│   ├── COM0418_ImageProcessing_Week2_Lab_Instructor_Guided.pdf
│   ├── matlab_test_images/
│   └── week2_lab_output/          # çalıştırınca oluşur
├── Lab 3/
│   ├── COM0418_ImageProcessing_Week3_Lab_Student.ipynb
│   ├── tiles.png
│   ├── pout.tif
│   └── tire.tif
├── .gitignore
└── README.md
```

> Yeni laboratuvarlar eklendikçe bu yapı genişleyecektir (`Lab 4/`, …).

---

## 👨‍🏫 Ders Bilgileri

- **🏫 Üniversite:** İstanbul Kültür Üniversitesi
- **🎓 Bölüm:** Bilgisayar Mühendisliği
- **📚 Ders Kodu:** COM0418
- **📖 Ders Adı:** Image Processing

---

## 📞 İletişim

Sorularınız için:
- 📧 GitHub Issues bölümünü kullanabilirsiniz
- 🔗 [Repository Linki](https://github.com/OnurAkyuz61/COM0418-ImageProcessing)

---

## 📄 Lisans

Bu proje eğitim amaçlı oluşturulmuştur. İstanbul Kültür Üniversitesi COM0418 dersi kapsamında hazırlanmıştır.

---

**🌟 İyi çalışmalar! Happy Coding! 🚀**
