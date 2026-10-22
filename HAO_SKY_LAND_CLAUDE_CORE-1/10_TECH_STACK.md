# TECH STACK — MACBOOK, PC VÀ CÔNG CỤ LÀM VIỆC

## 1. Thiết bị đã được đề cập

- MacBook Pro M1.
- iPhone 13 Pro Max.
- ASUS TUF VG27AQ5A và màn hình LG 27 inch 2K.
- PC từng được mô tả với Intel i5-14600K, RAM 16 GB, RTX 5060; xác minh cấu hình thực tế trước khi hướng dẫn tối ưu.
- Phần mềm/công cụ từng nhắc tới: OBS, CapCut, Premiere, GitHub Pages, React/Vite, NotebookLM, TeamViewer/điều khiển từ xa. Phiên bản hiện tại chưa được xác nhận.

## 2. Nguyên tắc phân chia công việc

Không mặc định phải làm mọi thứ trên một máy:
- MacBook: làm việc di động, xem xét nội dung, xử lý tác vụ phù hợp cấu hình.
- PC: có thể phù hợp render, đa nhiệm và tác vụ GPU nếu phần cứng/phần mềm hỗ trợ.
- Chọn máy theo phần mềm, codec, plugin, hiệu suất thực tế và dung lượng media.
- Điều khiển từ xa không thay thế việc quản lý file, sao lưu và kiểm tra kết nối.

## 3. Quy tắc trước khi đưa hướng dẫn kỹ thuật

Claude cần kiểm tra hoặc hỏi:
- Hệ điều hành và phiên bản.
- Tên/phiên bản phần mềm.
- Cấu hình phần cứng thực tế.
- File cần xử lý và dung lượng.
- Mục tiêu chất lượng, thời gian và ngân sách.
- Có dữ liệu chưa lưu hoặc project đang mở hay không.

## 4. Quy trình chuyển project video

1. Tạo thư mục dự án thống nhất.
2. Lưu project, media gốc, audio, graphics, subtitle và export.
3. Kiểm tra media có đường dẫn tương đối hay phụ thuộc ổ đĩa cụ thể.
4. Sao chép/đồng bộ toàn bộ media cần thiết.
5. Mở project trên máy đích và kiểm tra missing media, font, plugin, LUT, hiệu ứng.
6. Render thử đoạn ngắn.
7. Chỉ xóa bản cũ sau khi xác nhận bản mới đầy đủ và có backup.

## 5. Quy tắc code và website

- Đọc README và `package.json` trước khi chạy lệnh.
- Không giả định dự án là Vite chỉ vì người dùng từng dùng Vite ở một dự án khác.
- Không commit secrets.
- Không chạy lệnh xóa hoặc ghi đè không rõ phạm vi.
- Trước khi triển khai, xác định môi trường preview, production, biến môi trường và cách rollback.
- Với GitHub Pages, kiểm tra base path, build output, routing và URL triển khai hiện hành.

## 6. Sao lưu

Đề xuất nguyên tắc 3-2-1 cho dữ liệu quan trọng:
- 3 bản sao.
- 2 loại phương tiện lưu trữ.
- 1 bản sao ở vị trí tách biệt.

Đây là khuyến nghị, không phải tình trạng backup hiện tại. Không tuyên bố dữ liệu đã được sao lưu nếu chưa kiểm tra.

## 7. Lệnh và cài đặt

Chỉ cung cấp lệnh phù hợp với hệ điều hành và dự án đã kiểm tra. Trước lệnh có thể xóa/ghi đè, giải thích tác động và yêu cầu xác nhận.
