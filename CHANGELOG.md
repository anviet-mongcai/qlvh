# CHANGELOG — app QLVH (khung PWA + giao diện + máy chủ)

Mỗi đợt ghi 1 mục: phiên bản · ngày · đã đổi gì · cách quay về. Chi tiết nội bộ nằm ở tài liệu A của project.

## App v4.8 + khung v1.6 · 17/11/2026 · đợt 3 (QĐ-D375 a · QĐ-D376 a · QĐ-D389 a)
- v4.7 (16/11): «+1 ngày» 2 chạm ở Hôm nay · QR nhận tiền (VietQR tạo trong máy, tài khoản lưu trong máy).
- v4.8: chụp ảnh ngay trong app 1 chạm/ảnh, tự sang ô kế tiếp (giữ «Máy ảnh của máy» và 🖼 Thư viện) · mọi ảnh ≤ 250 KB.
- Khách quen tự điền: tra theo số giấy tờ vừa đọc, hoặc tìm SĐT / số giấy tờ / tên (lệnh đọc mới V81_khachQuen).
- Hoàn tác 10 giây cho trả xe, gia hạn/đổi gói, chiết khấu, kiểm xe, đóng hồ sơ, sửa chữa, ghi chú/trạng thái xe. Bật/tắt ở tab Sổ.
- Kiểm xe tuần: mở phiếu là vào máy ảnh; nút «Tất cả đạt · Ghi kết quả».
- Mã ký điện tử: hạn 24 giờ; mở lại màn QR dùng lại mã còn hạn nếu phiếu không đổi (máy chủ zz_v57).
- Khung v1.6: trả xe mất mạng → giữ cả ảnh trong máy (IndexedDB), tự gửi khi có mạng. sw khung v13. Cổng: Phiên bản 53.

## App v4.6 + khung v1.5 · 15/11/2026 · đợt 2 (QĐ-D387 a · QĐ-D388 a)
- Màn «Hôm nay» (mở app vào đây): 6 ô xe, việc cần làm xếp theo mức gấp, mỗi việc 1 nút.
- Thanh dưới: Hôm nay · Xe · [+] · Việc · Sổ. Kiểm xe, Nhắc việc mở từ [+], Hôm nay, Sổ.
- Chữ hiển thị bỏ mã nội bộ. «Có gì mới» hiện 1 lần sau cập nhật.
- Trả xe: các bước app tự ghi khi đóng lượt không còn ô tick tay.
- 3 lượt đọc nền lúc mở app gộp thành 1 (máy chủ nen.gs · V80_nen). sw khung v12. Cổng: Phiên bản 51.

## Khung v1.4 · 13/11/2026 · đợt 2 (QĐ-D370 a)
- Mở app bấm được ngay bằng số lần trước trong máy (bỏ lớp chặn chạm); số mới tải ngầm, dải báo nhỏ trên đầu.
- Mở app khi không có mạng: xem được số lần trước; chưa ghi được; tự thử lại khi có mạng.
- Lệnh ghi chỉ gửi khi số đang xem khớp sổ: chưa có số mới → chờ; sổ đã đổi → không ghi, báo nạp số mới rồi làm lại.
- sw khung v11. Không cần triển khai cổng.

## Đợt 1 «Nền an toàn» · 13/11/2026
| Phần | Phiên bản | Thay đổi | Quay về |
|---|---|---|---|
| Khung PWA (kho này) | v1.3 · sw `qlvh-khung-v10` | Lệnh ghi mang mã thao tác; cổng đã chống trùng thì mạng chập chờn tự gửi lại đúng mã (≤ 2 lần), mất mạng hẳn thì giữ thao tác trong máy (≤ 300 KB, ≤ 24 giờ) và tự gửi khi có mạng · lỗi trang tự báo về máy chủ (không kèm dữ liệu khách) · `/qlvh/?thu` = app thử, lưu riêng, nhãn «BẢN THỬ» | hoàn tác commit này |
| Giao diện (Index.html) | v4.5 | Thêm › «Góp ý / báo vướng» (chữ + ảnh tuỳ chọn). Phần còn lại giữ nguyên từng ký tự so với v4.4 | chọn lại phiên bản triển khai cổng trước |
| Máy chủ (Apps Script) | đợt 1 | Chống ghi trùng mọi lệnh ghi · lỗi → nhật ký + Telegram · gộp 11 lịch chạy thành 5 · gỡ 23 tệp một lần (đã lưu trữ) | chọn lại phiên bản triển khai trước; lịch chạy: nút quay về trong dự án |
| Bot nhắc việc | v3.1 | Nhận nút/lệnh mỗi phút trong 30 phút sau tin có nút hoặc lệnh, còn lại 10 phút (đêm như cũ) | bản sao lưu mã trước đợt 1 |

## Trước đợt 1
- Khung v1.2 · 07/11/2026: khoá app vân tay/khuôn mặt + PIN 6 số.
- Khung v1.1 · 07/10/2026: app cài điện thoại (PWA) gọi cổng Apps Script.
