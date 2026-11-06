# Nhật ký thay đổi lớn

Ghi lại tại đây mỗi khi dự án có thay đổi đáng kể để người bảo trì nắm được nội dung, phạm vi ảnh hưởng và kết quả kiểm tra. Thêm mục mới lên đầu danh sách, dùng ngày `YYYY-MM-DD`.

## Khi nào cần ghi log

- Thêm, thay đổi hoặc loại bỏ chức năng chính.
- Thay đổi cấu trúc, kiến trúc, công nghệ hoặc dependency của dự án.
- Thay đổi hành vi giao diện hoặc luồng sử dụng có ảnh hưởng rộng.
- Sửa lỗi nghiêm trọng, vấn đề bảo mật, hiệu năng hoặc tương thích.
- Thay đổi cấu hình triển khai, dữ liệu hoặc quy trình build/test.

Không cần ghi các chỉnh sửa nhỏ như sửa lỗi chính tả, định dạng hoặc đổi tên nội bộ không ảnh hưởng hành vi.

## Mẫu ghi

### YYYY-MM-DD - Tên thay đổi
- **Tóm tắt:** Nội dung đã thay đổi.
- **Ảnh hưởng:** Khu vực, chức năng hoặc người dùng bị ảnh hưởng.
- **Kiểm tra:** Các bước kiểm tra đã chạy và kết quả.
- **Còn lại:** Hạn chế hoặc công việc cần tiếp tục; ghi `Không có` nếu không còn.

## Nhật ký

### 2026-11-05 - Bổ sung minh chứng responsive
- **Tóm tắt:** Chụp ảnh viewport mobile, tablet và desktop vào `docs/screenshots/`; cập nhật trạng thái và liên kết minh chứng trong `docs/test_report.md`.
- **Ảnh hưởng:** Tài liệu kiểm thử; ảnh mobile ghi nhận nội dung bị cắt ở mép phải, chưa thay đổi mã nguồn giao diện.
- **Kiểm tra:** Xem lại ba ảnh Edge headless tại 390×844, 768×1024 và 1440×1000; kiểm tra test report không có lỗi.
- **Còn lại:** Sửa lỗi responsive mobile và chụp lại để xác nhận.

### 2026-11-05 - Tạo báo cáo kiểm thử trước bàn giao
- **Tóm tắt:** Bổ sung `docs/test_report.md` với đánh giá sơ bộ theo sáu nhóm tiêu chí QA/QC, checklist, trạng thái và đề xuất bàn giao.
- **Ảnh hưởng:** Tài liệu kiểm thử và bàn giao; không thay đổi chức năng ứng dụng.
- **Kiểm tra:** Kiểm tra báo cáo bằng công cụ kiểm tra file; không phát hiện lỗi.
- **Còn lại:** Chạy kiểm thử thực tế trên trình duyệt/môi trường triển khai và bổ sung minh chứng vào báo cáo.

### 2026-11-05 - Khởi tạo quy ước AI log
- **Tóm tắt:** Tạo quy ước và mẫu để ghi lại các thay đổi lớn của dự án trong file này.
- **Ảnh hưởng:** Tài liệu bảo trì dự án; không thay đổi chức năng ứng dụng.
- **Kiểm tra:** Xác nhận file log ban đầu đang trống trước khi thêm nội dung.
- **Còn lại:** Bổ sung mục mới khi phát sinh thay đổi lớn.
