# COM0418 — Image Processing

Bu repo, **COM0418 Image Processing** dersinin lab çalışmalarını içerir.

Her haftanın lab dosyaları kendi klasöründe tutulur (ör. `Lab 2/`). Notebook’lar, test görüntüleri ve ilgili materyaller bu klasörlerde yer alır.

## Yapı

```
COM0418-ImageProcessing/
├── Lab 2/
│   ├── *.ipynb
│   ├── lab2_test_images/
│   └── ...
└── README.md
```

## Çalıştırma

Lab’lar Jupyter Notebook ile yazılmıştır. Ortamı hazırlamak için:

```bash
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install jupyter numpy matplotlib opencv-python pillow scikit-image
jupyter notebook
```

Gereksinimler lab’a göre değişebilir; ilgili notebook’taki import’lara bakın.

## Not

Bu repo kişisel lab çözümleri ve ders materyalleri için kullanılmaktadır.
