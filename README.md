<div align="center">

# ⚡ Self Bot V3.2 ⚡

![Python](https://img.shields.io/badge/Python-3.11-blue?logo=python&logoColor=white)
![Discord.py](https://img.shields.io/badge/Discord.py--self-purple?logo=discord&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)
![Version](https://img.shields.io/badge/Version-3.2-orange)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)
![Download](https://img.shields.io/badge/Download-Zip-blue?style=for-the-badge&logo=github)

**Discord Self Bot với Auto-reply, AFK Mode, Copycat và nhiều tính năng khác.**

[📥 **Tải code (.zip)**](https://github.com/vVnK-wh0i4m/self-bot-v-3-2/archive/refs/heads/main.zip) • [📦 **Clone repo**](https://github.com/vVnK-wh0i4m/self-bot-v-3-2.git)

</div>

---

## ⚠️ Cảnh báo quan trọng

> **Công cụ này được cung cấp cho mục đích giải trí, thử nghiệm và nghiên cứu.** Người dùng **chịu toàn bộ trách nhiệm** khi sử dụng. **KHÔNG** sử dụng cho mục đích vi phạm pháp luật hoặc gây hại đến người khác.

> **Sử dụng self-bot vi phạm [Discord Terms of Service](https://discord.com/terms).** Tài khoản của bạn **có thể bị khóa vĩnh viễn**.

> **Yêu cầu Python 3.11** - Không chạy được trên version khác.

---

## 📋 Mục lục

- [Giới thiệu](#-giới-thiệu)
- [Tính năng](#-tính-năng)
- [Yêu cầu hệ thống](#-yêu-cầu-hệ-thống)
- [Cài đặt và chạy](#-cài-đặt-và-chạy)
- [Cấu hình](#-cấu-hình)
- [Cách sử dụng](#-cách-sử-dụng)
- [Cấu trúc dự án](#-cấu-trúc-dự-án)
- [FAQ](#-câu-hỏi-thường-gặp)
- [Bản quyền](#-bản-quyền)

---

## 🌟 Giới thiệu

**Self Bot V3.2** là Discord Self Bot Python được xây dựng bằng **discord.py-self** với hệ thống auto-reply, AFK mode, copycat và remote user management. Bot chạy trên prefix `.` và hỗ trợ cấu hình qua file JSON.

**Điểm nổi bật:**
- 🤖 Auto-reply tin nhắn
- 💤 AFK Mode với tin nhắn tùy chỉnh
- 📋 Copycat - sao chép tin nhắn từ user được chỉ định
- 👥 Remote Users management
- ⚙️ Cấu hình dễ dàng qua JSON

---

## 🚀 Tính năng

### 🤖 Auto-reply

| Tính năng | Mô tả |
|-----------|--------|
| Tin nhắn | Tự trả lời khi gặp tin nhắn chứa từ khóa |
| Kênh | Giới hạn auto-reply theo kênh |
| User | Giới hạn auto-reply theo user |

### 💤 AFK Mode

| Tính năng | Mô tả |
|-----------|--------|
| Bật/tắt | Dễ dàng bật/tắt AFK |
| Tin nhắn | Tùy chỉnh tin nhắn AFK |
| Tự động | Tự động trả lời khi có người tag |

### 📋 Copycat

| Tính năng | Mô tả |
|-----------|--------|
| Sao chép | Giống hệt tin nhắn từ user được chỉ định |
| Multi-user | Hỗ trợ nhiều user cùng lúc |

### 👥 Remote Users

| Tính năng | Mô tả |
|-----------|--------|
| Quản lý | Danh sách user từ xa |
| Tùy chỉnh | Thêm/xóa user dễ dàng |

---

## 💻 Yêu cầu hệ thống

| Thành phần | Yêu cầu |
|------------|----------|
| Python | **3.11 (BẮT BUỘC)** |
| RAM | Tối thiểu 512MB |
| Mạng | Kết nối internet ổn định |

---

## 📥 Cài đặt và chạy

### Bước 1: Clone repo

```bash
git clone https://github.com/vVnK-wh0i4m/self-bot-v-3-2.git
cd self-bot-v-3-2
```

### Bước 2: Tạo virtual environment

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

### Bước 3: Cài đặt thư viện

```bash
pip install -r requirements.txt
```

### Bước 4: Cấu hình

Sửa file `config/config.json` theo nhu cầu (xem phần [Cấu hình](#-cấu-hình)).

### Bước 5: Chuẩn bị token

Tạo file `tokens.txt` và thêm Discord User Token:

```
MTQ2ODIzOTA1NzM1MDk1NTA5OQ.G1xxxxx.xxxxxxxxxxxxxxxxxxxxxxxx
```

### Bước 6: Chạy bot

```bash
python main.py
```

---

## ⚙️ Cấu hình

### File `config/config.json`

```json
{
    "prefix": ".",
    "remote-users": [],
    "autoreply": {
        "messages": [
            "https://github.com/",
            "https://discord.gg/"
        ],
        "channels": [],
        "users": []
    },
    "afk": {
        "enabled": false,
        "message": "I am currently AFK. I will respond as soon as possible!"
    },
    "copycat": {
        "users": []
    }
}
```

### Giải thích

| Trường | Mô tả |
|--------|-------|
| `prefix` | Prefix cho lệnh (mặc định: `.`) |
| `remote-users` | Danh sách user từ xa |
| `autoreply.messages` | Tin nhắn kích hoạt auto-reply |
| `autoreply.channels` | Kênh auto-reply (trống = tất cả) |
| `autoreply.users` | User auto-reply (trống = tất cả) |
| `afk.enabled` | Bật/tắt AFK mode |
| `afk.message` | Tin nhắn AFK |
| `copycat.users` | Danh sách user cần copycat |

---

## 📖 Cách sử dụng

### Bật AFK

Sửa `config/config.json`:
```json
{
    "afk": {
        "enabled": true,
        "message": "Tôi đang AFK, sẽ quay lại sau!"
    }
}
```

### Thêm Auto-reply

Thêm tin nhắn vào `autoreply.messages`:
```json
{
    "autoreply": {
        "messages": [
            "hello",
            "xin chào",
            "chào bạn"
        ]
    }
}
```

### Bật Copycat

Thêm user ID vào `copycat.users`:
```json
{
    "copycat": {
        "users": ["1234567890", "0987654321"]
    }
}
```

---

## 📁 Cấu trúc dự án

```
selfbot-v3.2/
├── main.py              # Code chính (obfuscated)
├── config/
│   └── config.json      # Cấu hình bot
├── img/                 # Hình ảnh
├── tokens.txt           # User tokens (gitignore)
├── requirements.txt     # Dependencies
├── pyproject.toml       # Python project config
├── uv.lock              # Lock file
├── .replit              # Replit config
├── .gitignore
├── LICENSE
└── README.md
```

---

## ❓ Câu hỏi thường gặp

### Tool cần Python version nào?

**Python 3.11 BẮT BUỘC**. Không chạy được trên 3.10, 3.12 hay các version khác.

### Lỗi `ModuleNotFoundError`?

Chạy: `pip install -r requirements.txt`

### Bot không hoạt động?

1. Kiểm tra token có đúng format không
2. Kiểm tra Python version có phải 3.11 không
3. Kiểm tra file `config/config.json` có đúng format không

### Auto-reply không hoạt động?

1. Kiểm tra `autoreply.messages` có chứa tin nhắn kích hoạt không
2. Kiểm tra `autoreply.channels` (để trống = tất cả kênh)
3. Kiểm tra `autoreply.users` (để trống = tất cả user)

### AFK không trả lời?

Kiểm tra `afk.enabled` có phải `true` không.

---

## 📜 Bản quyền

**MIT License** - Xem file [LICENSE](LICENSE) để biết chi tiết.

Điều khoản sử dụng:

| ✅ Được phép | ❌ Không được phép |
|-------------|-------------------|
| Giải trí cá nhân | Quấy rối người khác |
| Nghiên cứu, học tập | Spam, gây phiền |
| Thử nghiệm | Vi phạm pháp luật |

---

<div align="center">

**⭐ Star repo nếu thấy hữu ích! ⭐**

Made with ❤️ by vVnK

</div>
