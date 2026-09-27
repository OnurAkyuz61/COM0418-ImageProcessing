# 🖼️ COM0418 - Image Processing Laboratuvar Çalışmaları

## 🎓 İstanbul Kültür Üniversitesi - Bilgisayar Mühendisliği Bölümü

Bu repository, **COM0418 - Image Processing** dersi kapsamında gerçekleştirilen laboratuvar çalışmalarını içermektedir.

---

## 📚 Laboratuvar İçerikleri

### 🔬 Lab 2 - NumPy Arrays, Image I/O & Bit-Plane Steganography
Bu laboratuvar, NumPy dizileri, MATLAB test görüntüleri, OpenCV I/O, veri tipleri, görüntü gösterimi ve bit-plane steganografi konularını kapsamaktadır.

- **📄 Dosyalar:**
  - `COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb` - Öğrenci notebook'u (alıştırma hücreleri)
  - `COM0418_ImageProcessing_Week2_Lab_Instructor_Guided.pdf` - Instructor kılavuzu / PDF
  - `lab2_test_images/` - MATLAB örnek görüntülerinin yerel kopyaları

- **📁 Test Görüntüleri (`lab2_test_images/`):**
  - `cameraman.tif` - Gri seviye görüntü (binary, data type, bit-plane, LSB steganografi)
  - `baby.jpg` - True-color görüntü (OpenCV ile okuma)
  - `sherlock.jpg` - True-color görüntü (Pillow ile karşılaştırma)
  - `trees.tif` - Indexed / palette renkli görüntü
  - `astronaut_rgb.png`, `camera_gray.png`, `camera_binary.png`, `gradient16.png`, `indexed_palette.gif` - Ek örnek görüntüler

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
- OpenCV ile görüntü kaydetme

#### 🧩 Bölüm 8 - Bit Planes
- 8-bit gri görüntünün bit-plane'lerini çıkarma
- Seçili bit-plane'lerden görüntü yeniden oluşturma

#### 🕵️ Bölüm 9 - LSB Steganography
- LSB düzlemine mesaj gömme
- Değişimi ölçme ve görselleştirme
- Stego görüntüyü kaydetme / yeniden yükleme

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

## 🚀 Nasıl Kullanılır

1. **📥 Repository'yi klonlayın:**
   ```bash
   git clone https://github.com/OnurAkyuz61/COM0418-ImageProcessing.git
   cd COM0418-ImageProcessing
   ```

2. **📂 İlgili laboratuvar klasörüne gidin:**
   ```bash
   cd "Lab 2"
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
   - `COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb`
   - Önce setup hücrelerini çalıştırın
   - Her exercise hücresinde `# Write your code below this line.` altına kodunuzu yazın
   - **Shift+Enter** ile çalıştırıp çıktıyı kontrol edin

5. **🖼️ Test görüntüleri:**
   - Lab bilgisayarlarında öncelik MATLAB image data dizinidir
   - MATLAB yoksa notebook, `lab2_test_images/` klasörünü fallback olarak kullanır

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
- Pillow (PIL)

### 🧪 Ortam (ders laboratuvarı)
- Anaconda environment: `imagepr_env`
- (İsteğe bağlı) MATLAB image toolbox örnek görüntüleri

---

## 🎯 Öğrenme Hedefleri

Bu laboratuvar çalışmaları ile öğrenciler:

- ✅ Görüntüleri NumPy dizileri olarak işler
- ✅ OpenCV ve Pillow ile görüntü okuma/yazma yapar
- ✅ Gri, binary, renkli ve indexed görüntü türlerini ayırt eder
- ✅ BGR / RGB kanal sırası farkını açıklar ve düzeltir
- ✅ Görüntü veri tiplerini güvenli şekilde dönüştürür
- ✅ Matplotlib ve OpenCV ile görüntü gösterir
- ✅ Bit-plane analizi yapar
- ✅ LSB steganografi temelini uygular
- ✅ ROI seçimi, threshold ve temel görüntü manipülasyonu yapar

---

## 📁 Repo Yapısı

```
COM0418-ImageProcessing/
├── Lab 2/
│   ├── COM0418_ImageProcessing_Week2_Lab_Student_Guided.ipynb
│   ├── COM0418_ImageProcessing_Week2_Lab_Instructor_Guided.pdf
│   └── lab2_test_images/
├── .gitignore
└── README.md
```

> Yeni laboratuvarlar eklendikçe bu yapı genişleyecektir (`Lab 3/`, `Lab 4/`, …).

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
