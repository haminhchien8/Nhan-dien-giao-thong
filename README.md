# 🛡️ HỆ THỐNG LƯU TRỮ VÀ XÁC THỰC VI PHẠM GIAO THÔNG KHÔNG ĐỘI MŨ BẢO HIỂM

<div align="center">

<p align="center">
  <img src="logo_truong.png" alt="Logo Trường" width="180"/>
  <img src="logo_khoa.png" alt="Logo Khoa" width="180"/>
</p>

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-WebApp-red?logo=streamlit)
![Blockchain](https://img.shields.io/badge/Blockchain-Ethereum-blueviolet)
![SQLite](https://img.shields.io/badge/SQLite-Database-green)

</div>

<h3 align="center">🚦 Giải pháp phát hiện và xác thực vi phạm giao thông bằng AI và Blockchain</h3>

<p align="center">
<strong>
Hệ thống sử dụng mô hình YOLOv8 để phát hiện người điều khiển xe máy không đội mũ bảo hiểm từ hình ảnh và video. Dữ liệu vi phạm được lưu trữ bằng SQLite, tạo mã băm SHA-256 và xác thực trên Blockchain nhằm đảm bảo tính toàn vẹn, minh bạch và chống giả mạo bằng chứng vi phạm.
</strong>
</p>

---

# 🏗️ Kiến trúc hệ thống

<p align="center">
  <img src="assets/architecture.png" alt="System Architecture" width="800"/>
</p>

Hệ thống gồm các thành phần chính:

1. 📹 Thu nhận dữ liệu từ ảnh hoặc video.
2. 🧠 YOLOv8 phát hiện người có mũ và không đội mũ bảo hiểm.
3. 📸 Lưu ảnh bằng chứng vi phạm.
4. 🔐 Tạo mã băm SHA-256 cho ảnh vi phạm.
5. ⛓️ Ghi nhận hash lên Blockchain.
6. 💾 Lưu thông tin vi phạm vào SQLite.
7. 📱 Gửi cảnh báo qua Telegram Bot.
8. 📊 Hiển thị thống kê và xác thực dữ liệu trên Web Dashboard.

---

# ✨ Tính năng chính

## 🧠 Trí tuệ nhân tạo

* Phát hiện người đội mũ bảo hiểm.
* Phát hiện người không đội mũ bảo hiểm.
* Nhận diện từ hình ảnh và video.
* Hỗ trợ xử lý nhiều đối tượng trong cùng khung hình.

## 🔐 Blockchain & Bảo mật

* Tạo mã băm SHA-256 cho ảnh bằng chứng.
* Lưu hash lên Blockchain.
* Kiểm tra tính toàn vẹn dữ liệu.
* Phát hiện dữ liệu bị chỉnh sửa hoặc giả mạo.

## 📊 Quản lý dữ liệu

* Lưu trữ vi phạm bằng SQLite.
* Quản lý ảnh bằng chứng.
* Tìm kiếm theo SHA-256.
* Xác thực dữ liệu vi phạm.

## 📱 Thông báo thời gian thực

* Gửi ảnh vi phạm qua Telegram Bot.
* Gửi thông tin SHA-256.
* Gửi mã giao dịch Blockchain.

---

# 🔧 Công nghệ sử dụng

<div align="center">

![Python](https://img.shields.io/badge/Python-3776AB?logo=python\&logoColor=white)
![YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-orange)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit)
![SQLite](https://img.shields.io/badge/SQLite-003B57?logo=sqlite)
![Ethereum](https://img.shields.io/badge/Ethereum-627EEA?logo=ethereum)
![Web3.py](https://img.shields.io/badge/Web3.py-F16822)
![Telegram](https://img.shields.io/badge/Telegram-26A5E4?logo=telegram)

</div>

### Công nghệ cốt lõi

* Python
* YOLOv8
* OpenCV
* Streamlit
* SQLite
* SHA-256
* Ethereum Blockchain
* Web3.py
* Telegram Bot API

---

# 📥 Cài đặt

## Yêu cầu hệ thống

* Python 3.10+
* Git
* Streamlit
* YOLOv8
* SQLite

## Clone dự án

```bash
git clone https://github.com/USERNAME/helmet-detection-blockchain.git
cd helmet-detection-blockchain
```

## Cài đặt thư viện

```bash
pip install -r requirements.txt
```

## Cấu hình Telegram

Tạo file:

```text
app/.env
```

```env
TELEGRAM_TOKEN=YOUR_BOT_TOKEN
TELEGRAM_CHAT_ID=YOUR_CHAT_ID
```

## Chạy hệ thống

```bash
streamlit run app/main.py
```

---

# 🚀 Quy trình hoạt động

<p align="center">
  <img src="assets/workflow.png" width="800"/>
</p>

1. Người dùng tải ảnh hoặc video lên hệ thống.
2. YOLOv8 thực hiện phát hiện đối tượng.
3. Xác định người không đội mũ bảo hiểm.
4. Lưu ảnh bằng chứng.
5. Tạo SHA-256.
6. Ghi hash lên Blockchain.
7. Lưu dữ liệu vào SQLite.
8. Gửi cảnh báo Telegram.
9. Hiển thị kết quả trên Dashboard.

---

# 📊 Cơ sở dữ liệu

Bảng chính:

```sql
CREATE TABLE violations (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    timestamp TEXT,
    camera TEXT,
    violation_type TEXT,
    image_path TEXT,
    confidence REAL,
    image_hash TEXT,
    blockchain_tx TEXT,
    ipfs_uri TEXT
);
```

---

# 🔮 Hướng phát triển

* Tích hợp IPFS lưu trữ ảnh vi phạm.
* Mở rộng nhiều loại vi phạm giao thông.
* Triển khai Blockchain công khai.
* Tích hợp Camera IoT thời gian thực.
* Xây dựng nền tảng Smart City.

---

# 👨‍🎓 Tác giả

**Đề tài:** Hệ thống lưu trữ và xác thực vi phạm giao thông không đội mũ bảo hiểm

**Công nghệ:** AI + Blockchain + IoT + Computer Vision
