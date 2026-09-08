# Day 01 — Introduction to IoT

## 🎯 Objective

Memahami konsep dasar Internet of Things (IoT)
dan perbedaannya dengan embedded system.

## 📚 What I Learned

- Pengertian IoT
- Sensor
- Processing
- Communication
- Actuator
- Perbedaan IoT dan embedded system

## 🔄 Basic IoT Architecture

Sensor
↓
Microcontroller
↓
Network
↓
Server
↓
Application

## 🔧 Components Related to My IoT Project

- ESP32 DevKit
- DHT22
- HC-SR04
- TCRT5000
- Servo
- DC Motor
- L298N
- LCD I2C
- Buzzer
- RGB LED

## 🧪 Experiment

Melakukan analisis terhadap beberapa contoh
sistem IoT dan mengidentifikasi bagian sensor,
processing, communication, dan actuator/output.

## 🧠 Analysis

1. Kasus 1: ESP32 + DHT22 + LCD
    - Sensor: DHT22 (mengukur suhu dan kelembapan).
    - Processing: Microcontroller ESP32 (membaca data sensor dan memprosesnya).
    - Communication: Tidak digunakan untuk pengiriman data ke sistem luar/jaringan (hanya sebagai komunikasi lokal I2C ke LCD).
    - Actuator/Output: LCD I2C (menampilkan data hasil pengukuran).
    - Status: Belum menjadi sistem IoT penuh karena tidak ada pengiriman data melalui jaringan/internet, melainkan sebatas embedded system.

2. Kasus 2: Smart Trash Can (ESP32 + HC-SR04 + Servo + Blynk)
    - Sensor: HC-SR04 (mendeteksi jarak objek/tangan).
    - Processing: Microcontroller ESP32 (membaca data sensor dan memprosesnya).
    - Communication: Wi-Fi internal ESP32 ke Blynk Cloud via protokol Blynk/MQTT.
    - Actuator/Output: Servo (membuka/menutup tutup tempat sampah) dan dashboard aplikasi Blynk.
    - Status: Sistem IoT penuh karena data status tempat sampah dikirim ke cloud dan dapat dipantau/dikontrol jarak jauh.

## ❓ Questions

1. Apakah ESP32 + DHT22 + LCD termasuk IoT?
2. Apakah perangkat IoT harus menggunakan internet?
3. Apa perbedaan IoT dengan embedded system?

## 📝 Conclusion

1. Embedded system merupakan fondasi dasar dari IoT yang berfokus pada pemrosesan lokal antara sensor dan aktuator.
2. Sebuah sistem baru bisa dikategorikan sebagai sistem IoT apabila terdapat elemen konektivitas (communication layer) yang menghubungkan device ke jaringan   atau server untuk transmisi data.