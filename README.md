# 💬 Multi-Client TCP Chat Application

> Ứng dụng truyền thông điệp thời gian thực giữa máy chủ (Server) và nhiều máy khách (Client) dựa trên giao thức truyền tải tin cậy TCP/IP.

---

## 🛠️ Công nghệ & Kỹ thuật sử dụng

![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Network Protocol](https://img.shields.io/badge/TCP/IP-Networking-blue?style=for-the-badge)

---

## 🌟 Tính năng chính

- ⚡ **Truyền tin thời gian thực:** Kết nối ổn định và đảm bảo toàn vẹn dữ liệu nhờ giao thức hướng kết nối TCP.
- 🧵 **Xử lý đa luồng (Multi-threading):** Server quản lý đồng thời nhiều Client cùng lúc mà không bị treo hay nghẽn luồng.
- 👥 **Quản lý phòng chat:** 
  * Tự động thông báo khi có thành viên tham gia (`Join`) hoặc rời phòng (`Leave`).
  * Broadcast tin nhắn từ 1 user tới toàn bộ các user khác trong hệ thống.
  * Hiển thị trạng thái hoạt động và danh sách người dùng đang online.
- 🛡️ **Xử lý ngoại lệ mạng:** Nhận diện và ngắt kết nối an toàn khi Client đột ngột ngắt kết nối (Disconnect/Crash).

---

## 💡 Thách thức & Giải pháp kỹ thuật

- **Tránh tranh chấp tài nguyên (Race Condition):** Sử dụng `Mutex` (hoặc Semaphore) để khóa danh sách socket khi nhiều luồng Client đồng thời gửi/nhận dữ liệu.
- **Quản lý vùng đệm (Buffer Overflow):** Đặt kích thước gói tin tiêu chuẩn và kiểm tra cờ kết thúc chuỗi để tránh việc đè dữ liệu giữa các gói tin TCP.

---

## 🚀 Hướng dẫn biên dịch & Chạy local

1. **Clone repository:**
   ```bash
   git clone [https://github.com/qhuong-287/tcp-chat-application.git](https://github.com/qhuong-287/tcp-chat-application.git)
   cd tcp-chat-application
