# Thời Tiết TP.HCM

Dashboard thời tiết trực tiếp cho TP. Hồ Chí Minh — nhiệt độ hiện tại và dự báo 24 giờ tới, cập nhật theo thời gian thực.

** Xem trực tiếp:** (https://thoi-tiet-tphcm.pages.dev/thoi-tiet-tphcm)

## Tính năng

- Nhiệt độ, cảm giác thực tế, độ ẩm, gió, lượng mưa, UV và chất lượng không khí (AQI) hiện tại
- Cảnh báo nổi bật ngay đầu trang khi có dông hoặc mưa lớn trong 24 giờ tới
- Dự báo chi tiết theo từng giờ: nhiệt độ, % khả năng mưa và lượng mưa (mm)
- Mốc chuyển ngày rõ ràng trong dải dự báo 24 giờ, vuốt mượt trên điện thoại (scroll-snap)
- Biểu đồ diễn biến nhiệt độ và xác suất mưa
- Màu sắc các chỉ số tự đổi theo mức độ đáng chú ý (bình thường / cần lưu ý / cảnh báo)
- Tự lưu lại dữ liệu lần gần nhất — vẫn hiển thị được khi mất mạng, kèm ghi chú "dữ liệu cũ"
- Tự làm mới dữ liệu bằng một nút bấm, không cần tải lại trang
- Giao diện tối, tối ưu cho cả điện thoại lẫn máy tính

## Công nghệ sử dụng

- HTML/CSS/JavaScript thuần — không framework, không bước build
- [Open-Meteo](https://open-meteo.com/) — dữ liệu thời tiết và chất lượng không khí, miễn phí, không cần API key
- [Cloudflare Pages](https://pages.cloudflare.com/) — hosting static site, miễn phí vĩnh viễn

## Chạy thử ở máy local

Không cần cài đặt gì — chỉ cần mở file bằng trình duyệt:

```bash
git clone https://github.com/Trakiequa/thoi-tiet-tphcm.git
cd thoi-tiet-tphcm
open thoi-tiet-tphcm.html   # hoặc double-click file trong Finder/Explorer
```

## Dự định phát triển tiếp

- [x] Cảnh báo giông/mưa lớn nổi bật ngay đầu trang
- [x] Thêm chỉ số UV và chất lượng không khí (AQI)
- [x] Lưu dữ liệu gần nhất để xem khi mất mạng
- [ ] Cảnh báo nguy cơ ngập đường dựa trên lượng mưa/giờ
- [ ] Gợi ý nhanh "có nên đi xe máy không" theo thời tiết hiện tại
- [ ] Cài được như app trên điện thoại (PWA)
- [ ] Xuất ảnh chia sẻ nhanh lên mạng xã hội
