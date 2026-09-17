# 🌦️ Thời Tiết TP.HCM

Dashboard thời tiết trực tiếp cho TP. Hồ Chí Minh — nhiệt độ hiện tại và dự báo 24 giờ tới, cập nhật theo thời gian thực.

**🔗 Xem trực tiếp:** [thoi-tiet-tphcm-1.onrender.com](https://thoi-tiet-tphcm-1.onrender.com)

![status](https://img.shields.io/badge/status-active-brightgreen)
![license](https://img.shields.io/badge/license-MIT-blue)

## ✨ Tính năng

- Nhiệt độ, cảm giác thực tế, độ ẩm, gió, lượng mưa hiện tại
- Dự báo chi tiết theo từng giờ trong 24 giờ tới
- Biểu đồ diễn biến nhiệt độ và xác suất mưa
- Tự làm mới dữ liệu bằng một nút bấm, không cần tải lại trang
- Giao diện tối, tối ưu cho cả điện thoại lẫn máy tính

## 🧱 Công nghệ sử dụng

- HTML/CSS/JavaScript thuần — không framework, không bước build
- [Open-Meteo](https://open-meteo.com/) — nguồn dữ liệu thời tiết miễn phí, không cần API key
- [Render](https://render.com/) — hosting static site

## 🚀 Chạy thử ở máy local

Không cần cài đặt gì — chỉ cần mở file bằng trình duyệt:

```bash
git clone https://github.com/Trakiequa/thoi-tiet-tphcm.git
cd thoi-tiet-tphcm
open thoi-tiet-tphcm.html   # hoặc double-click file trong Finder/Explorer
```

## 🗺️ Dự định phát triển tiếp

- [ ] Cảnh báo giông/mưa lớn nổi bật ngay đầu trang
- [ ] Cảnh báo nguy cơ ngập đường dựa trên lượng mưa/giờ
- [ ] Thêm chỉ số UV và chất lượng không khí (AQI)
- [ ] Gợi ý nhanh "có nên đi xe máy không" theo thời tiết hiện tại
- [ ] Cài được như app trên điện thoại (PWA), xem lại được khi mất mạng
- [ ] Xuất ảnh chia sẻ nhanh lên mạng xã hội
