# 🌦️ Thời Tiết TP.HCM

Dashboard thời tiết trực tiếp cho TP. Hồ Chí Minh — nhiệt độ hiện tại và dự báo 24 giờ tới, cập nhật theo thời gian thực.

**🔗 Xem trực tiếp:** [đường-link-cloudflare-pages-của-bạn](https://thay-bang-link-cloudflare-cua-ban.pages.dev) <!-- TODO: thay bằng link Cloudflare Pages thật -->

![status](https://img.shields.io/badge/status-active-brightgreen)
![license](https://img.shields.io/badge/license-MIT-blue)

<!--
📸 Chèn ảnh/GIF demo ở đây trước khi đăng lên GitHub — đây là thứ đầu tiên
người xem repo nhìn thấy. Chụp màn hình dashboard lúc đã tải xong dữ liệu:

![demo](./demo.gif)
-->

## ✨ Tính năng

- Nhiệt độ, cảm giác thực tế, độ ẩm, gió, lượng mưa, UV và chất lượng không khí (AQI) hiện tại
- Cảnh báo nổi bật ngay đầu trang khi có dông hoặc mưa lớn trong 24 giờ tới
- Dự báo chi tiết theo từng giờ: nhiệt độ, % khả năng mưa và lượng mưa (mm)
- Mốc chuyển ngày rõ ràng trong dải dự báo 24 giờ, vuốt mượt trên điện thoại (scroll-snap)
- Biểu đồ diễn biến nhiệt độ và xác suất mưa
- Màu sắc các chỉ số tự đổi theo mức độ đáng chú ý (bình thường / cần lưu ý / cảnh báo)
- Tự lưu lại dữ liệu lần gần nhất — vẫn hiển thị được khi mất mạng, kèm ghi chú "dữ liệu cũ"
- Tự làm mới dữ liệu bằng một nút bấm, không cần tải lại trang
- Giao diện tối, tối ưu cho cả điện thoại lẫn máy tính

## 🧱 Công nghệ sử dụng

- HTML/CSS/JavaScript thuần — không framework, không bước build
- [Open-Meteo](https://open-meteo.com/) — dữ liệu thời tiết và chất lượng không khí, miễn phí, không cần API key
- [Cloudflare Pages](https://pages.cloudflare.com/) — hosting static site, miễn phí vĩnh viễn

## 🚀 Chạy thử ở máy local

Không cần cài đặt gì — chỉ cần mở file bằng trình duyệt:

```bash
git clone https://github.com/Trakiequa/thoi-tiet-tphcm.git
cd thoi-tiet-tphcm
open thoi-tiet-tphcm.html   # hoặc double-click file trong Finder/Explorer
```

## 🗺️ Dự định phát triển tiếp

- [x] Cảnh báo giông/mưa lớn nổi bật ngay đầu trang
- [x] Thêm chỉ số UV và chất lượng không khí (AQI)
- [x] Lưu dữ liệu gần nhất để xem khi mất mạng
- [ ] Cảnh báo nguy cơ ngập đường dựa trên lượng mưa/giờ
- [ ] Gợi ý nhanh "có nên đi xe máy không" theo thời tiết hiện tại
- [ ] Cài được như app trên điện thoại (PWA)
- [ ] Xuất ảnh chia sẻ nhanh lên mạng xã hội

## 🤖 Được xây dựng cùng AI

Dự án là một thử nghiệm phối hợp giữa hai trợ lý AI: **Claude** phụ trách review giao diện, trải nghiệm người dùng và nội dung hiển thị; **ChatGPT/Codex** phụ trách lập trình và triển khai. Repo này là kết quả của vài vòng góp ý — triển khai qua lại giữa hai bên.

## 📄 Giấy phép

Chưa có license — nếu muốn cho phép người khác tự do sử dụng/sửa đổi, thêm file `LICENSE` với nội dung [MIT License](https://choosealicense.com/licenses/mit/) là lựa chọn phổ biến nhất.
