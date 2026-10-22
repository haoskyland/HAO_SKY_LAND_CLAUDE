# CHECKLIST CÀI ĐẶT VÀ KIỂM TRA

## A. Cài đặt
- [ ] Giải nén ZIP vào thư mục dễ tìm.
- [ ] Đặt `CLAUDE.md` ở gốc repository mà Claude Code sẽ làm việc.
- [ ] Giữ tài liệu liên quan trong cùng kho hoặc cập nhật đường dẫn trong `CLAUDE.md` nếu tổ chức lại.
- [ ] Xem `.gitignore.example`; chỉ đổi tên thành `.gitignore` sau khi rà soát với repo đích, không ghi đè `.gitignore` đang có.
- [ ] Không chép dữ liệu khách hàng hoặc secrets vào kho hướng dẫn.

## B. Kiểm tra ban đầu bằng Claude Code
Dùng prompt:

> Đọc `CLAUDE.md`, `README.md` và các tài liệu liên quan. Chỉ kiểm tra, chưa sửa file. Hãy báo: (1) cấu trúc hiện tại; (2) quy tắc bạn sẽ tuân theo; (3) dữ liệu còn thiếu; (4) rủi ro bảo mật; (5) đề xuất 3 bước tiếp theo.

## C. Thử nghiệm an toàn
- [ ] Giao một việc chỉ đọc/đánh giá trước.
- [ ] Giao một việc nhỏ có thể đảo ngược.
- [ ] Kiểm tra báo cáo có nói đúng file và test thực tế không.
- [ ] Chỉ sau đó mới dùng trên repo hoặc dữ liệu quan trọng.

## D. Không tự động được cấu hình bởi gói này
Gói này không cài Claude Code, không cấp quyền OS, không đăng nhập tài khoản, không kết nối Google Drive/CRM, không tạo API key, không bật quảng cáo và không tự đồng bộ dữ liệu. Các tích hợp đó phải thiết lập riêng và cần quyền rõ ràng.
