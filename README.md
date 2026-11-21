# PHATECO Offshore Radiation Safety

Ứng dụng tính toán và minh hoạ các biện pháp an toàn bức xạ, dành cho PHATECO và khách hàng của PHATECO.

Ứng dụng phục vụ đào tạo an toàn bức xạ cho công việc chụp ảnh phóng xạ công nghiệp bằng nguồn Ir-192 trên giàn khai thác ngoài khơi. Người học là cả nhân viên bức xạ lẫn người làm việc khác trên giàn, người Việt và người nước ngoài.

**Xem trực tuyến:** https://nddzungx.github.io/phateco-offshore-radiation-safety/

**Mã nguồn:** https://github.com/nddzungx/phateco-offshore-radiation-safety

**Phiên bản hiện tại:** 1.0.1 (21/11/2026) – xem [CHANGELOG.md](CHANGELOG.md)

> Ứng dụng dùng nội bộ. Số liệu tính toán chỉ để đào tạo và minh hoạ, không thay thế đánh giá an toàn bức xạ chính thức, giấy phép hay số đo thực tế tại hiện trường.

## Tính năng

- **Ba ngôn ngữ:** Tiếng Việt, English, song ngữ Việt–Anh; đổi ngay mà không mất trạng thái đang làm.
- **10 bài học** về bức xạ, đơn vị liều, thời gian – khoảng cách – che chắn, vùng kiểm soát, giới hạn liều theo Nghị định 332/2025/NĐ-CP, ALARA, quy trình làm việc; có đánh dấu tiến độ.
- **Mô phỏng 3D mặt bằng giàn:**
  - bản đồ suất liều theo màu, đường hàng rào 7.5 µSv/h và đường 10 µSv/h;
  - bật/tắt hiển thị tia phát ra từ nguồn;
  - kích đúp vào nguồn để xem loại nguồn, hoạt độ theo chứng chỉ, hoạt độ tại ngày bất kỳ, hoặc khai báo nguồn khác;
  - kích đúp vào vách để đổi vật liệu, bề dày, khoảng cách, chiều dài;
  - bấm một điểm để xem suất liều và liều tích luỹ 4 tuần / 12 tuần, cảnh báo xanh (dưới 90 % ngưỡng), vàng (90–110 %), đỏ (trên 110 %).
- **Tính liều:** chọn không dùng collimator, collimator giảm 10 hoặc giảm 16; không che chắn hoặc che chắn thép với bề dày tự nhập; đổi số phim, phút mỗi phim, ngày mỗi tuần, số tuần.
- **So sánh liều** với chụp X-quang, chuyến bay, bức xạ nền, giới hạn liều.
- **Ứng phó sự cố:** 6 tình huống, nhóm ứng phó 4 người, trang bị theo danh sách thiết bị dự án, hình minh hoạ từng bước và clip 3D có ước tính liều từng người.
- **Kiểm tra** 15 câu hỏi có giải thích; **thuật ngữ** song ngữ; **trang công thức** với hằng số và nguồn trích dẫn.
- Giao diện sáng/tối, dùng được trên máy tính và điện thoại, **chạy offline** sau khi tải về.

## Cách dùng

**Trực tuyến:** mở link ở trên bằng Chrome, Edge, Firefox hoặc Safari bản mới.

**Không có Internet (ví dụ trên giàn):** tải file `index.html` về máy rồi mở bằng trình duyệt. Mọi thư viện đã nằm sẵn trong file, không cần kết nối mạng.

**Gợi ý khi đào tạo:**

1. Chọn ngôn ngữ ở góc trên bên phải (VI, EN, VI–EN).
2. Đi lần lượt các bài học trong menu bên trái.
3. Mở **Mô phỏng 3D**, bấm lên sàn để đặt người, xem màu cảnh báo; kích đúp vào nguồn hoặc vách để đổi thông số.
4. Dùng **Tính liều** cho các câu hỏi "nếu… thì sao" (đổi collimator, bề dày thép, khối lượng công việc).
5. Xem **Ứng phó sự cố** và phát clip 3D của từng tình huống.
6. Kết thúc bằng phần **Kiểm tra**.

**Yêu cầu:** trình duyệt hỗ trợ WebGL (hầu hết máy tính và điện thoại hiện nay). Nếu không có WebGL, các phần khác vẫn dùng được, chỉ phần 3D báo không hiển thị.

## Giả định chính

| Nội dung | Giá trị | Ghi chú |
| --- | --- | --- |
| Nguồn | Ir-192, 20 Ci (740 GBq) | Giá trị thiết kế dự án; đổi được trong ứng dụng |
| Hằng số suất liều Γ | 0.13 mSv·m²/(h·GBq) | IAEA SSG-11; Working Safely in Radiography |
| HVL thép | 12.7 mm | Chì 5.1 mm và bê tông 43 mm cần xác nhận |
| Collimator | giảm 10 lần ngoài chùm chính | Giả định, cần xác nhận theo model |
| Khối lượng | 30 phim × 3 phút = 1.5 h/ngày, 7 ngày/tuần, 4 hoặc 12 tuần/năm | Đổi được trong ứng dụng |
| Tiêu chí | 7.5 µSv/h tại hàng rào, 10 µSv/h tại vị trí thợ chụp | Tiêu chí vận hành của dự án |
| Giới hạn | Công chúng 1 mSv/năm; nhân viên bức xạ 20 mSv/năm | Nghị định 332/2025/NĐ-CP, Phụ lục I |

## Cấu trúc kho

```
index.html     Ứng dụng (một file, chạy độc lập)
README.md      Giới thiệu
CHANGELOG.md   Lịch sử phiên bản
LICENSE        Giấy phép sử dụng
```

## Bản quyền

© 2026 PHATECO. Bảo lưu mọi quyền. Xem [LICENSE](LICENSE).
Ứng dụng có dùng thư viện three.js (giấy phép MIT).

## Liên hệ

nddzungx@gmail.com
