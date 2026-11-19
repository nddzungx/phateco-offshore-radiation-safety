# Lịch sử phiên bản

Định dạng theo [Keep a Changelog](https://keepachangelog.com/vi/1.1.0/); số phiên bản theo [Semantic Versioning](https://semver.org/lang/vi/).

## [1.0.0] – 2026-11-19

Phiên bản đầu tiên đưa lên GitHub Pages.

### Có trong phiên bản này

**Chung**
- Một file `index.html` chạy độc lập, offline; không gọi máy chủ, không thu thập dữ liệu.
- Ba chế độ ngôn ngữ: Tiếng Việt, English, song ngữ Việt–Anh.
- Menu dọc bên trái thu gọn được; giao diện sáng/tối; dùng được trên điện thoại.
- Trang Giới thiệu: phiên bản, bản quyền PHATECO, liên hệ.

**Bài học và kiểm tra**
- 10 bài học an toàn bức xạ cho chụp ảnh phóng xạ Ir-192 trên giàn, có đánh dấu tiến độ.
- 15 câu hỏi kiểm tra có giải thích.
- Bảng thuật ngữ song ngữ; trang công thức, hằng số và nguồn trích dẫn.

**Mô phỏng 3D**
- Bản đồ suất liều theo màu trên mặt bằng giàn; đường hàng rào 7.5 µSv/h và đường 10 µSv/h.
- Bật/tắt hiển thị tia phát ra từ nguồn; nút toàn màn hình.
- Kích đúp vào nguồn: loại nguồn, hoạt độ ban đầu theo chứng chỉ, hoạt độ tại ngày đang xem; khai báo nguồn khác.
- Kích đúp vào vách: đổi vật liệu, bề dày, khoảng cách, chiều dài.
- Bấm một điểm: suất liều, liều tích luỹ 4 tuần và 12 tuần, cảnh báo xanh / vàng / đỏ theo 90 % và 110 % ngưỡng.
- Đổi giả định số phim, phút mỗi phim, ngày mỗi tuần, số tuần, tỉ lệ có mặt; chọn ngưỡng 1 mSv, 20 mSv hoặc tự nhập.

**Tính liều**
- Không collimator / collimator giảm 10 / giảm 16; không che chắn / che chắn thép tự nhập (mặc định 10 mm).
- Bảng so sánh 6 tổ hợp collimator và che chắn; bán kính tới 7.5 và 10 µSv/h.

**So sánh liều**
- Biểu đồ thang log so sánh liều trong mô phỏng với X-quang, chuyến bay, bức xạ nền, CT và các giới hạn.

**Ứng phó sự cố**
- 6 tình huống theo quy trình ứng phó của nhà thầu; nhóm ứng phó 4 người với vai trò rõ ràng.
- Danh mục trang bị ứng phó có hình, đánh dấu mục còn thiếu cần xác nhận.
- Hình minh hoạ từng bước và clip 3D cho mỗi tình huống, có ước tính liều từng người.

### Hạn chế đã biết
- Chỉ tính cho Ir-192; collimator giảm 10 là giả định; HVL chì và bê tông cần xác nhận.
- Không tính hệ số tích luỹ (build-up) và tán xạ chi tiết.
- Mô hình một nguồn, một vách.
