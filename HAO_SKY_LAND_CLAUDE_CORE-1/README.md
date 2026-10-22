# Hào Sky Land — Claude Code Operating System

Bộ cấu hình thực hành cho Claude Code, gồm file điều khiển ở gốc, tài liệu chuyên môn, mẫu dữ liệu và checklist triển khai. Các tài liệu mô tả cách làm việc; chúng **không** chứng minh giá, chính sách hoặc tình trạng dự án hiện hành.

## Bắt đầu nhanh

1. Giải nén ZIP.
2. Mở thư mục `HAO_SKY_LAND_CLAUDE_CORE` trong Claude Code, hoặc sao chép `CLAUDE.md` vào thư mục gốc repo mà bạn muốn Claude làm việc.
3. Giữ các file Markdown chuyên môn và thư mục `templates/` trong cùng thư mục để Claude có thể đọc khi cần.
4. Mở Claude Code và yêu cầu: `Đọc CLAUDE.md và README.md, kiểm tra cấu trúc thư mục, sau đó tóm tắt quy tắc và chỉ ra dữ liệu còn thiếu. Chưa sửa file nào.`
5. Khi đã sẵn sàng, giao một nhiệm vụ nhỏ để kiểm tra quy trình trước khi dùng với dữ liệu thật.

## Cấu trúc

- `CLAUDE.md`: entrypoint — luật vận hành chính, tự chủ, bảo mật và quy trình kiểm thử.
- `01_USER_PROFILE.md`: bối cảnh người dùng đã biết và các điểm cần xác minh.
- `02_CLAUDE.md`: bản sao đánh số của file vận hành chính, thuận tiện cho danh mục 15 tài liệu.
- `03_WRITING_STYLE.md`: giọng văn và nội dung.
- `04_DATA_GOVERNANCE.md`: nguồn, phiên bản, mâu thuẫn và bảo mật dữ liệu.
- `05_REAL_ESTATE_PLAYBOOK.md`: tư vấn, phân tích và bán hàng BĐS.
- `06_PROJECT_MASTER_INDEX.md`: cấu trúc kho dự án.
- `07_MARKETING_PLAYBOOK.md`: chiến dịch, nội dung và đo lường.
- `08_VIDEO_PRODUCTION_SOP.md`: quy trình video.
- `09_BRAND_GUIDELINES.md`: nhận diện thương hiệu.
- `10_TECH_STACK.md`: thiết bị, code, chuyển project và backup.
- `11_PERSONAL_FINANCE.md`: phân tích ngân sách và kịch bản.
- `12_LEARNING_SYSTEM.md`: lộ trình học.
- `13_WORKFLOW_LIBRARY.md`: quy trình lặp lại.
- `14_QA_CHECKLIST.md`: checklist chất lượng.
- `15_CHANGELOG.md`: nhật ký thay đổi.
- `templates/`: mẫu dự án, nguồn, nội dung, CRM và rà soát tuần.
- `examples/`: ví dụ dữ liệu giả để minh họa cấu trúc.

## Quy tắc an toàn

- Không đặt API key, mật khẩu, OTP hoặc dữ liệu khách hàng thật vào kho này.
- Trước khi dùng cho dự án đang bán, xác minh lại giá, chính sách, pháp lý, tiến độ, tồn kho, hotline và quyền phân phối.
- Không chạy quảng cáo, gửi tin, công khai dữ liệu, xóa dữ liệu, commit/push hoặc deploy chỉ vì file hướng dẫn nói có thể làm.
- File `CLAUDE.md` không tự cài phần mềm, cấp quyền hệ thống, kết nối tài khoản hoặc đồng bộ dữ liệu.

## Tài liệu nào được đọc khi nào?

Không cần nhồi toàn bộ tài liệu vào mọi câu hỏi. Claude nên đọc `CLAUDE.md` trước, rồi chỉ đọc tài liệu chuyên sâu liên quan đến nhiệm vụ. Ví dụ: nghiên cứu dự án đọc `04`, `05`, `06`; viết quảng cáo đọc `03`, `07`, `09`, `14`; dựng video đọc `03`, `08`, `09`, `14`; sửa code đọc `CLAUDE.md`, README của repo đích và cấu hình thực tế.

## Trạng thái dữ liệu

Các dự án được nêu trong hồ sơ là lịch sử trao đổi, không phải danh sách phân phối hiện hành. Những chi tiết chưa xác minh phải giữ nhãn `NEEDS_CONFIRMATION`, `USER-PROVIDED` hoặc `UNVERIFIED` cho đến khi có bằng chứng phù hợp.
