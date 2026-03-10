# FaceRecognition_GoogLeNet
Project 1 - Indonesia AI

# Face Recognition: Multi-Task Learning (Gender, Smile, Age)

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0+-ee4c2c.svg)](https://pytorch.org/)
[![Gradio](https://img.shields.io/badge/UI-Gradio-orange.svg)](https://gradio.app/)

## 📌 Deskripsi Proyek
Proyek ini mengimplementasikan sistem pengenalan wajah berbasis **Multi-Task Learning**. Menggunakan satu input gambar wajah, model ini mampu memprediksi tiga atribut sekaligus:
1. **Gender**: Mengklasifikasikan pria atau wanita.
2. **Smiling**: Mendeteksi apakah wajah dalam keadaan tersenyum atau tidak.
3. **Age**: Memberikan estimasi kategori usia (Muda/Tua).

Sistem ini didasarkan pada arsitektur **GoogLeNet (Inception v1)** yang dimodifikasi dengan tiga jalur output (*multi-head*) untuk menangani setiap tugas secara bersamaan.

## 🛠️ Fitur & Spesifikasi Teknis
* **Base Model**: GoogLeNet (Pre-trained).
* **Custom Architecture**: Modifikasi lapisan terakhir menjadi tiga cabang: `fc_gender`, `fc_smile`, dan `fc_age`.
* **Akselerasi Hardware**: Menggunakan **Mixed Precision Training (AMP)** untuk performa maksimal pada GPU NVIDIA RTX 5050.
* **Interface**: Dilengkapi dengan UI interaktif berbasis **Gradio** untuk pengujian langsung oleh pengguna.

## 📊 Dataset
Proyek ini menggunakan dataset **CelebA (CelebFaces Attributes Dataset)**.
* Proses sinkronisasi data dilakukan untuk memastikan file gambar sesuai dengan atribut di `list_attr_celeba.csv`.
* Data dibersihkan dari entri yang tidak memiliki file gambar fisik.
* Subset data digunakan untuk efisiensi komputasi selama fase pengembangan.

## 💻 Instalasi & Penggunaan
1. **Clone Repository**:
   ```bash
   git clone [https://github.com/piopanjaitan/FaceRecognition_GoogLeNet.git](https://github.com/piopanjaitan/FaceRecognition_GoogLeNet.git)
   cd FaceRecognition_GoogLeNet
