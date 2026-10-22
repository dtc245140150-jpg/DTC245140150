# ĐỀ TÀI 5: HỆ THỐNG QUẢN LÝ KHO HÀNG (INVENTORY)

* **Họ và tên sinh viên:** Lê Sơn Bá[cite: 6, 7]
* **Mã số sinh viên:** DTC245140150[cite: 6, 7]
* **Lớp / Khóa:** Công nghệ Thông tin – K23C[cite: 6, 7]
* **Hệ điều hành thực hành:** Ubuntu Server / Desktop trên VMware Workstation[cite: 6, 7]

---

## 🏗️ 1. Cấu trúc và Kiến trúc hệ thống
Hệ thống được đóng gói và triển khai bằng Docker Compose gồm các dịch vụ chính[cite: 6, 7]:
- **Nginx Reverse Proxy:** Định tuyến request, áp dụng Security Headers chống lỗ hổng bảo mật (Port 80)[cite: 6, 7].
- **Web App Inventory & phpMyAdmin:** Giao diện quản lý kho và công cụ quản trị MySQL Database (Port 8080)[cite: 6, 7, 8].
- **Prometheus & Grafana:** Thu thập chỉ số tài nguyên và trực quan hóa Dashboard giám sát (Port 9090, 3000)[cite: 6, 7, 8].
- **Loki & Promtail:** Thu thập và truy vấn log tập trung bằng ngôn ngữ LogQL[cite: 6, 7].

---

## ⚙️ 2. Hướng dẫn Khởi chạy hệ thống

### Bước 1: Clone Repository về máy ảo Ubuntu
```bash
git clone [https://github.com/dtc245140150-jpg/DTC245140150.git](https://github.com/dtc245140150-jpg/DTC245140150.git)
cd DTC245140150
