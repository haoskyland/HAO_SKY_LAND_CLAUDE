# DATA GOVERNANCE — QUẢN TRỊ DỮ LIỆU

## 1. Mục tiêu

Giữ dữ liệu chính xác, có nguồn, có mốc thời gian và có thể truy vết. Áp dụng cho dự án bất động sản, CRM, marketing, tài chính và code.

## 2. Nhãn trạng thái dữ liệu

- `VERIFIED`: đã đối chiếu với nguồn phù hợp, còn hiệu lực tại mốc ghi nhận.
- `USER-PROVIDED`: người dùng cung cấp; chưa mặc nhiên được xác minh độc lập.
- `ASSUMPTION`: giả định dùng để phân tích hoặc mô phỏng.
- `UNVERIFIED`: có thông tin nhưng chưa đủ căn cứ.
- `UNKNOWN`: chưa có dữ liệu.
- `EXPIRED`: đã hết hiệu lực hoặc cần kiểm tra lại.
- `CONFLICT`: các nguồn đang mâu thuẫn.

Không được đổi `USER-PROVIDED` thành `VERIFIED` nếu chưa kiểm chứng.

## 3. Trường thông tin tối thiểu cho dữ liệu quan trọng

- Tên dữ liệu.
- Nội dung/giá trị.
- Dự án hoặc phạm vi áp dụng.
- Nguồn và đường dẫn/tên tài liệu.
- Ngày ban hành (nếu có).
- Ngày nhận.
- Ngày xác minh gần nhất.
- Ngày hiệu lực/hết hiệu lực (nếu có).
- Trạng thái dữ liệu.
- Người cập nhật (nếu biết).
- Ghi chú mâu thuẫn/giới hạn.

## 4. Thứ tự đánh giá nguồn

Không dùng một thứ tự cứng cho mọi trường hợp. Chọn nguồn theo loại thông tin:
- Pháp lý: văn bản/đơn vị có thẩm quyền, hồ sơ pháp lý có thể kiểm tra.
- Giá và chính sách: thông báo chính thức còn hiệu lực hoặc hệ thống bán hàng được xác nhận.
- Tiến độ: thông báo chính thức có ngày, hình ảnh có thời điểm hoặc xác nhận đáng tin cậy.
- Hạ tầng/quy hoạch: cơ quan có thẩm quyền, hồ sơ công bố chính thức; báo chí đáng tin cậy chỉ dùng bổ trợ.
- Ý kiến thị trường: phân biệt nhận định, tin đồn và dữ kiện.

Nếu mâu thuẫn, ghi lại cả hai nguồn, thời điểm và nội dung khác nhau; không tự chọn số thuận lợi hơn.

## 5. Quy tắc cập nhật phiên bản

- Không xóa dữ liệu cũ có giá trị lịch sử; chuyển vào `archive` hoặc đánh dấu hết hiệu lực.
- Tên file có thể dùng ngày ISO: `YYYY-MM-DD`.
- Bảng giá nên có cột ngày cập nhật và trạng thái hiệu lực.
- Chỉ có một file được đánh dấu “CURRENT” cho mỗi loại dữ liệu đang hoạt động; file khác phải ghi `ARCHIVE` hoặc `SUPERSEDED`.
- Không coi ngày sửa file là ngày chính sách có hiệu lực.

## 6. Quy tắc cho Claude Code

- Trước khi sửa dữ liệu gốc, đọc file và mô tả thay đổi.
- Ưu tiên tạo bản mới hoặc diff khi thay đổi có rủi ro.
- Không tự điền ô trống bằng phỏng đoán.
- Không hợp nhất bảng nếu chưa kiểm tra cột, đơn vị, mã căn và bản ghi trùng.
- Không dùng dữ liệu thử nghiệm làm dữ liệu thật.
- Khi tạo báo cáo, ghi rõ khoảng thời gian và phạm vi dữ liệu.

## 7. Quyền riêng tư

- Không lưu mật khẩu, OTP, API key, token, thông tin thanh toán đầy đủ trong Markdown.
- Dùng dữ liệu khách hàng đã ẩn danh cho ví dụ và kiểm thử.
- Chỉ thu thập dữ liệu cá nhân cần thiết cho mục đích công việc hợp pháp.
- Không đưa tài liệu có dữ liệu khách hàng thật vào repository công khai.
- Trước khi đẩy GitHub, kiểm tra `.gitignore`, lịch sử Git và file có thông tin nhạy cảm.

## 8. Mẫu ghi nhận dữ kiện

| Trường | Giá trị |
|---|---|
| Dữ kiện | `[mô tả]` |
| Trạng thái | `USER-PROVIDED` |
| Nguồn | `[tên file/URL/người cung cấp]` |
| Ngày nhận | `YYYY-MM-DD` |
| Ngày xác minh | `Chưa xác minh` |
| Hiệu lực | `Chưa rõ` |
| Ghi chú | `[mâu thuẫn/giới hạn]` |
