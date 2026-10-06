# 🌦️ Thời Tiết TP.HCM

Dashboard thời tiết cho **từng phường/xã của TP. Hồ Chí Minh**: tự nhận phường theo GPS của thiết bị, xem nhanh phường khác bằng ô tìm kiếm, kèm dự báo 24 giờ tới và trợ lý AI diễn giải.

**🔗 Xem trực tiếp:** [thoi-tiet-tphcm.pages.dev](https://thoi-tiet-tphcm.pages.dev/thoi-tiet-tphcm)

## ✨ Tính năng

- **Theo phường/xã:** 168 đơn vị hành chính của TP.HCM (từ 01/07/2025), tự nhận phường bằng GPS, tìm kiếm gõ không dấu, nhớ lựa chọn lần trước
- **Hiện tại:** nhiệt độ, cảm giác thực tế, độ ẩm, gió, lượng mưa, UV và chất lượng không khí (AQI) kèm nhãn mức độ
- **Dự báo 24 giờ:** nhiệt độ và lượng mưa (mm) từng giờ, mốc chuyển ngày, **dải mưa** nhìn nhanh giờ nào mưa, biểu đồ nhiệt độ
- **Cảnh báo** nổi bật khi có dông hoặc mưa lớn (ghi rõ hôm nay/ngày mai)
- **Trợ lý thời tiết AI:** tóm tắt xu hướng và gợi ý giờ ra ngoài/đi xe máy theo đúng phường đang xem. Giờ mưa do thuật toán tính, AI chỉ diễn giải bằng lời
- **Xem được khi mất mạng:** lưu dữ liệu gần nhất của phường, kèm ghi chú "dữ liệu cũ"
- Giao diện tối, tối ưu cho điện thoại và máy tính

> ⚠️ Số liệu lấy từ mô hình thời tiết toàn cầu có độ phân giải khoảng 10 km (chất lượng không khí có thể thô hơn), nên các phường gần nhau thường cho kết quả giống nhau. Khác biệt rõ nhất thấy giữa các vùng xa nhau (Cần Giờ, Củ Chi, Vũng Tàu, Côn Đảo...).

## 🔒 Quyền riêng tư

Tọa độ GPS chỉ được xử lý trên thiết bị của bạn để tìm phường. Chỉ tọa độ tâm của phường được gửi tới Open-Meteo; chỉ dữ liệu thời tiết và tên phường được gửi tới trợ lý AI.

## 🧱 Cấu trúc & công nghệ

| Thành phần | Nội dung |
|---|---|
| `thoi-tiet-tphcm.html` | Toàn bộ giao diện và logic (HTML/CSS/JS thuần, không framework) |
| `wards-geo.json` | Ranh giới phường/xã đã đơn giản hóa, dùng để xác định phường từ GPS. **Phải để cùng thư mục với file html.** Thiếu file này, trang vẫn chạy nhưng chỉ chọn phường có tâm gần nhất (kém chính xác hơn) |
| `index.html` | Chuyển hướng tới trang chính |
| Trợ lý AI | Cloudflare Worker riêng (giữ API key bí mật), **không nằm trong repo này** |

- [Open-Meteo](https://open-meteo.com/): dữ liệu thời tiết và chất lượng không khí, miễn phí, không cần API key
- [Cloudflare Pages](https://pages.cloudflare.com/): hosting trang tĩnh; Cloudflare Workers + Google Gemini API: trợ lý AI

## 🚀 Chạy thử ở máy local

Cần chạy qua một máy chủ cục bộ (GPS và việc tải `wards-geo.json` không hoạt động khi mở trực tiếp bằng `file://`):

```bash
git clone https://github.com/Trakiequa/thoi-tiet-tphcm.git
cd thoi-tiet-tphcm
python -m http.server 8000
# mở http://localhost:8000/thoi-tiet-tphcm.html
```

Muốn dùng trợ lý AI, tự deploy Worker của bạn rồi điền URL vào biến `AI_WORKER_URL` trong file html. Không bao giờ để API key trong file html hay commit lên repo.

## 🗺️ Dự định phát triển tiếp

- [x] Cảnh báo giông/mưa lớn, UV, AQI, xem khi mất mạng
- [x] Thời tiết theo phường/xã, tự nhận vị trí bằng GPS
- [x] Trợ lý AI diễn giải theo phường
- [ ] Phường hay xem (ghim nhà/cơ quan)
- [ ] Cảnh báo nguy cơ ngập đường dựa trên lượng mưa/giờ
- [ ] Cài được như app trên điện thoại (PWA)
- [ ] Xuất ảnh chia sẻ nhanh lên mạng xã hội

## 🙏 Nguồn dữ liệu & ghi công

- Thời tiết, chất lượng không khí: [Open-Meteo](https://open-meteo.com/)
- Ranh giới phường/xã: [Long Ngo (lqtue/phuongnao)](https://github.com/lqtue/phuongnao)
- Danh sách đơn vị hành chính: thư viện [vietnam-provinces](https://github.com/sunshine-tech/VietnamProvinces)

## 🤖 Được xây dựng cùng AI

Dự án là thử nghiệm phối hợp giữa **Claude** (thiết kế, review, backend AI) và **ChatGPT/Codex** (lập trình, triển khai).
