# CRM — BỘ TRƯỜNG TỐI THIỂU

Thiết kế theo nguyên tắc tối thiểu hóa dữ liệu, có quyền truy cập phù hợp và ghi lại nguồn/đồng ý liên hệ khi cần. Không nhập dữ liệu khách thật vào ví dụ công khai.

## Trường gợi ý
| Trường | Bắt buộc? | Mục đích | Lưu ý |
|---|---|---|---|
| lead_id | Có | Mã duy nhất | Không dùng số giấy tờ cá nhân làm ID |
| display_name | Có nếu có | Tên hiển thị | Có thể dùng tên gọi |
| contact_channel | Có | Zalo/điện thoại/email/form | Hạn chế quyền truy cập |
| contact_value | Khi cần liên hệ | Thông tin liên hệ | Dữ liệu cá nhân; bảo vệ phù hợp |
| source_campaign | Khuyến nghị | Biết nguồn lead | Lưu tên chiến dịch, không suy đoán |
| created_at | Có | Thời điểm tạo | ISO 8601 nếu có thể |
| purpose | Có | Nhu cầu chính | Mua ở/đầu tư/thuê/chuyển nhượng |
| budget_range | Không | Sàng lọc phương án | Chỉ ghi khi khách tự cung cấp |
| preferred_area | Không | Khu vực ưu tiên | Ghi nguyên văn nếu chưa rõ |
| project_interest | Không | Dự án quan tâm | Không coi là cam kết mua |
| stage | Có | Trạng thái xử lý | New/Contacted/Qualified/Meeting/Negotiation/Won/Lost/Nurture |
| last_contact_at | Không | Theo dõi chăm sóc | Không ghi nội dung thừa |
| next_action | Có khi đang xử lý | Việc tiếp theo | Một hành động rõ ràng |
| next_followup_at | Có khi hẹn | Nhắc follow-up | Không gửi tự động nếu chưa được phép |
| consent_status | Khi áp dụng | Quản lý đồng ý liên hệ | Ghi nguồn/thời điểm/phạm vi nếu cần |
| data_source | Khuyến nghị | Truy xuất nguồn | Form, khách tự gửi, nguồn hợp pháp |
| access_class | Có | Phân quyền | Internal/Restricted |
| notes | Không | Ghi chú cần thiết | Không ghi suy đoán nhạy cảm |

## Quy tắc
- Chỉ thu thập dữ liệu cần thiết cho mục đích rõ ràng.
- Cho phép sửa/xóa theo chính sách và nghĩa vụ áp dụng; không hứa xóa khi chưa biết hệ thống lưu ở đâu.
- Tách dữ liệu khách hàng khỏi repo code công khai.
- Trước khi tích hợp CRM với email/Zalo/quảng cáo, xác minh quyền truy cập, phạm vi gửi và cơ chế dừng.
