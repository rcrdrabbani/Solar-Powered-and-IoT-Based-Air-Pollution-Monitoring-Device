# Perangkat Pemantau Polusi Udara Berbasis IoT & Tenaga Surya 🇮🇩

[![IoT](https://img.shields.io/badge/IoT-Platform-blue.svg)]()
[![Hardware](https://img.shields.io/badge/Hardware-ESP32%20%7C%20ESP8266-orange.svg)]()
[![Language](https://img.shields.io/badge/Language-C++%20%7C%20Python-green.svg)]()

[← Kembali ke Menu Utama](./README.md)

### 📌 Ringkasan Proyek
Proyek ini mengintegrasikan efisiensi daya perangkat keras dengan analisis data berbasis cloud. Dirancang sebagai proyek tugas akhir teknik, perangkat ini menggunakan sistem pembangkit listrik tenaga surya (PV) mandiri untuk menjaga waktu aktif (*uptime*) 24/7 di area terbuka, menyusun telemetri gas dan partikulat ke dalam paket data ringkas yang dikirim langsung ke infrastruktur cloud.

### 🏗️ Arsitektur Sistem
*Firmware* dirancang menggunakan struktur **Finite State Machine (FSM)** untuk mencegah terjadinya *stuck/error loop* dan menangani proses pemanasan sensor (*warm-up*), terputusnya jaringan, serta mode hemat daya secara sistematis.

* **Edge Device:** Mikrokontroler ESP32 / ESP8266 membaca data analog/digital dari sensor lingkungan.
* **Pipeline Data:** Metrik mentah dikemas ke dalam format data `JSON` yang ringan.
* **Cloud Gateway:** Skrip Python mengelola jabat tangan (*handshake*) REST API, memasukkan aliran telemetri ke database.
* **Dasbor:** Terintegrasi menggunakan Google Sheets API untuk visualisasi langsung dan pencatatan riwayat data.

### 🛠️ Spesifikasi Teknologi
* **Perangkat Keras & Daya:** ESP32, Panel Surya, Solar Charge Controller (SCC), Baterai Li-ion, Sensor Elektrokimia.
* **Firmware:** C/C++ (Arduino IDE), Arsitektur FSM, Manajemen Daya Teroptimasi.
* **Perangkat Lunak & Integrasi:** Python Scripting, JSON Parser, REST API, Google Sheets API.
* **Mekanis & Desain:** EasyEDA (Desain PCB), Autodesk CAD (Skema Casing Perangkat).

### 🚀 Cara Penggunaan
1. **Konfigurasi Perangkat Keras:** Pastikan sistem PV Anda menyalurkan daya yang stabil ke mikrokontroler. Hubungkan sensor melalui Pin Analog atau protokol I2C/SPI yang ditentukan.
2. **Penyebaran Firmware:** Buka file kode sumber perangkat keras di Arduino IDE, instal pustaka (*library*) sensor yang diperlukan, konfigurasikan kredensial Wi-Fi Anda, dan unggah ke ESP32.
3. **Middleware Backend:** Jalankan skrip Python di komputer *host* atau server cloud Anda untuk mulai menerima kiriman data dan meneruskannya ke dasbor Google Sheets API Anda.
