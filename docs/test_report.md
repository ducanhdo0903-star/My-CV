# BÁO CÁO KIỂM THỬ VÀ ĐÁNH GIÁ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Giá trị |
|---|---|
| Tên dự án | My-CV - Portfolio cá nhân |
| Phiên bản | v1.0 (cần xác nhận với chủ dự án) |
| Ngày đánh giá | 2026-11-05 |
| Người thực hiện | [Điền tên QA/QC] |
| Người đánh giá/phê duyệt | [Điền tên người đánh giá] |
| Phạm vi | Đánh giá sơ bộ mã nguồn HTML/CSS và cấu trúc repository; chụp kiểm tra responsive tại ba viewport |
| Môi trường kiểm thử | Microsoft Edge headless, mở trang local; 390×844, 768×1024, 1440×1000. Chưa kiểm thử trên môi trường triển khai; phiên bản Edge chưa ghi nhận. |

> **Lưu ý:** Đây là đánh giá sơ bộ dựa trên nội dung repository và ảnh chụp responsive bằng Edge headless. Các hạng mục chưa được thực thi hoặc chưa có đủ minh chứng được đánh dấu **Cần cải thiện**. Ảnh chụp không thay thế kiểm thử trên thiết bị thật hoặc môi trường triển khai.

## 2. Quy ước trạng thái

- **Đạt:** Có đủ kết quả kiểm tra/minh chứng cho thấy hạng mục đáp ứng tiêu chí.
- **Chưa đạt:** Đã phát hiện lỗi hoặc nội dung chưa đáp ứng yêu cầu.
- **Cần cải thiện:** Chưa đủ minh chứng, cần kiểm tra thêm hoặc cần hoàn thiện trước khi bàn giao.

## 3. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | Chưa đạt | Có điều hướng nội bộ; các liên kết dự án còn là placeholder và thông tin tác giả không nhất quán. Chưa có tài liệu yêu cầu để đối chiếu đầy đủ. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | Chưa đạt | Ảnh mobile 390×844 cho thấy menu và nội dung mô tả bị cắt ở mép phải; tablet/desktop đã chụp nhưng chưa kiểm tra trên thiết bị thật hoặc các trình duyệt khác. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | Cần cải thiện | Chưa có kết quả chạy thử, đo hiệu năng hoặc kiểm tra lỗi khi tải tài nguyên/mạng. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | Cần cải thiện | Chưa có đánh giá trên môi trường triển khai hoặc rà soát bảo mật đầy đủ; cần xác nhận dữ liệu liên hệ và cấu hình hosting. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | Chưa đạt | HTML/CSS được tách riêng, nhưng README trống và nội dung tên tác giả chưa đồng nhất. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | Cần cải thiện | Đã lưu ảnh responsive mobile/tablet/desktop; chưa có hướng dẫn triển khai, log kiểm thử hoặc minh chứng cho các nhóm kiểm tra còn lại. |

## 4. Chi tiết kiểm tra

### 4.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Các mục Giới thiệu, Kỹ năng, Dự án, Liên hệ có trong trang | Đạt | Đối chiếu cấu trúc section trong `index.html`; chưa có tài liệu yêu cầu được phê duyệt để xác nhận tính đầy đủ. |
| Điều hướng menu và nút CTA trỏ tới section tương ứng | Đạt | Các liên kết `#about`, `#skills`, `#projects`, `#contact` có section đích tương ứng trong `index.html`. Cần xác nhận thao tác thực tế trên trình duyệt. |
| Liên kết “Xem chi tiết” của từng dự án hoạt động | Chưa đạt | Các thẻ dự án đang dùng `href="#"`, chưa dẫn tới trang/dự án thật. |
| Liên kết GitHub và LinkedIn hoạt động | Chưa đạt | Hai liên kết liên hệ đang dùng `href="#"`; URL hiển thị là dữ liệu mẫu. |
| Nội dung nhận diện tác giả nhất quán | Chưa đạt | Tên hiển thị là “Đỗ Đức Anh”, trong khi `meta author`, email, tài khoản liên hệ và footer dùng thông tin “Nguyễn Văn An”/dữ liệu mẫu. Cần chủ dự án xác nhận thông tin đúng. |
| Email mở đúng trình xử lý thư | Cần cải thiện | Có liên kết `mailto:an.nguyen@example.com`, nhưng địa chỉ có vẻ là dữ liệu mẫu; cần xác nhận trước bàn giao. |

### 4.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Bố cục có quy tắc responsive | Đạt | `styles.css` khai báo bố cục mobile-first, breakpoint từ 768px và 1280px. Đây là xác nhận từ mã nguồn, chưa thay thế kiểm thử hiển thị thực tế. |
| Tài nguyên ảnh đại diện tồn tại và có văn bản thay thế | Đạt | Có `assets/img/avatar.jpg`; thẻ ảnh trong `index.html` có thuộc tính `alt`. Chưa xác nhận ảnh hiển thị đúng trên trình duyệt. |
| Menu, lưới dự án và nội dung không tràn ở màn hình nhỏ | Chưa đạt | Ảnh [mobile 390×844](screenshots/responsive-mobile.png) cho thấy menu điều hướng và dòng mô tả hero bị cắt ở mép phải. Cần sửa và chụp lại để xác nhận. |
| Thao tác bằng bàn phím và trạng thái focus | Cần cải thiện | CSS có `:focus-visible`; chưa kiểm tra thứ tự Tab, khả năng nhận biết focus và thao tác đầy đủ không dùng chuột. |
| Độ tương phản, khả năng đọc và hỗ trợ trình đọc màn hình | Cần cải thiện | Chưa đo tương phản màu hoặc kiểm tra bằng công cụ hỗ trợ tiếp cận/trình đọc màn hình. |
| Tương thích trên các trình duyệt mục tiêu | Cần cải thiện | Đã chụp bằng Edge headless; chưa có kết quả trên Chrome, Firefox, Safari hoặc thiết bị di động thật. Ảnh [tablet 768×1024](screenshots/responsive-tablet.png) và [desktop 1440×1000](screenshots/responsive-desktop.png) là minh chứng viewport. |

### 4.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Trang tải được cùng stylesheet và ảnh cục bộ | Cần cải thiện | Các đường dẫn tương ứng có trong repository; chưa chạy trang để xác nhận không có lỗi 404 hoặc lỗi tải tài nguyên. |
| Trải nghiệm khi tài nguyên không tải được | Cần cải thiện | Chưa kiểm tra trường hợp mất ảnh, stylesheet hoặc kết nối mạng; chưa ghi nhận hành vi dự phòng. |
| Thời gian tải và hiệu năng cơ bản | Cần cải thiện | Chưa đo bằng Lighthouse, DevTools hoặc công cụ tương đương; cần lưu kết quả đo khi thực hiện. |
| Hành vi cuộn, điều hướng và giảm chuyển động | Cần cải thiện | Mã nguồn khai báo cuộn mượt và hỗ trợ `prefers-reduced-motion`; chưa xác nhận hành vi thực tế trên trình duyệt. |

### 4.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Không đưa bí mật/credential vào mã nguồn công khai | Cần cải thiện | Chưa thực hiện quét secret trên toàn bộ repository; cần quét trước khi public hoặc bàn giao. |
| Dữ liệu cá nhân và thông tin liên hệ chính xác, được phép công bố | Cần cải thiện | Trang chứa tên, email và liên kết hồ sơ; cần chủ dự án xác nhận tính chính xác và quyền công bố. |
| Cấu hình bảo mật khi triển khai HTTPS/headers | Cần cải thiện | Chưa có cấu hình máy chủ/hosting trong phạm vi đánh giá; cần xác minh HTTPS và các security headers tại môi trường đích. |
| Luồng gửi dữ liệu hoặc lưu trữ dữ liệu nhạy cảm | Đạt | Không thấy biểu mẫu gửi dữ liệu hoặc logic lưu trữ trong trang HTML được xem xét. Kết luận chỉ giới hạn ở mã nguồn hiện tại, không bao gồm cấu hình hosting. |

### 4.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| HTML và CSS được tổ chức thành tài nguyên riêng | Đạt | `index.html` liên kết tới `assets/css/styles.css`; cấu trúc tài nguyên ảnh nằm trong `assets/img/`. |
| Cấu trúc HTML và nhãn nội dung cơ bản | Đạt | Có `lang="vi"`, metadata, các vùng `header`, `nav`, `main`, `section` và `footer`; chưa chạy HTML validator hoặc audit accessibility. |
| Thông tin và tài liệu hướng dẫn dự án | Chưa đạt | `README.md` hiện trống; thiếu hướng dẫn chạy, cấu hình, triển khai và phạm vi chức năng. |
| Tính nhất quán của nội dung và tài liệu | Chưa đạt | Tên tác giả trong metadata/footer không khớp nội dung nhận diện; repository có cả `RELEASENNOTE.md` và `RELEASENOTE.md`, cần xác định tên file chuẩn và loại bỏ nhầm lẫn khi bàn giao. |
| Kiểm tra cú pháp và chất lượng mã tự động | Cần cải thiện | Chưa có kết quả validator/linter hoặc quy trình CI được cung cấp trong phạm vi đánh giá. |

### 4.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú / Minh chứng |
|---|---|---|
| Có hướng dẫn chạy/triển khai rõ ràng | Chưa đạt | `README.md` trống; chưa có hướng dẫn mở trang hoặc cấu hình hosting. |
| Có checklist và kết quả kiểm thử được lưu lại | Cần cải thiện | Báo cáo này là checklist đánh giá sơ bộ; chưa có biên bản chạy test thực tế hoặc người thực hiện/phê duyệt được điền. |
| Có minh chứng cho kết quả kiểm thử | Cần cải thiện | Chưa đính kèm ảnh chụp, log trình duyệt, kết quả Lighthouse, validator hoặc URL môi trường staging. |
| Có quy trình triển khai và xác nhận sau triển khai | Cần cải thiện | Chưa có thông tin pipeline, môi trường staging/production, rollback hoặc smoke test sau triển khai. |

## 5. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm hiện có cấu trúc portfolio tĩnh bằng HTML/CSS, các section chính và bố cục responsive được thể hiện trong mã nguồn. Tuy nhiên, chưa có tài liệu yêu cầu được phê duyệt, chưa chạy kiểm thử trên trình duyệt/môi trường triển khai và chưa có minh chứng kiểm thử. Vì vậy, **chưa đủ cơ sở xác nhận sản phẩm sẵn sàng bàn giao**.

### Vấn đề cần xử lý trước bàn giao

1. Xác nhận và đồng bộ tên, email, GitHub, LinkedIn giữa nội dung trang, metadata và footer.
2. Thay các liên kết `href="#"` bằng URL thật hoặc loại bỏ nếu chức năng chưa được cung cấp.
3. Hoàn thiện `README.md` với yêu cầu, cách chạy, cấu hình và hướng dẫn triển khai.
4. Chạy kiểm thử chức năng và giao diện trên desktop/mobile, các trình duyệt mục tiêu; kiểm tra bàn phím, focus và độ tương phản.
5. Kiểm tra lỗi tải tài nguyên, xác thực HTML/CSS và đo hiệu năng cơ bản; lưu log/kết quả làm minh chứng.
6. Xác nhận cấu hình HTTPS/security headers và quét secret trước khi phát hành công khai.
7. Xác định file release note đúng tên (`RELEASENOTE.md` hoặc `RELEASENNOTE.md`) để tránh hai tài liệu trùng mục đích.

### Điều kiện đề xuất để phê duyệt bàn giao

- Các mục **Chưa đạt** đã được xử lý hoặc có chấp thuận ngoại lệ bằng văn bản.
- Các mục **Cần cải thiện** quan trọng đã được kiểm thử và cập nhật trạng thái dựa trên minh chứng.
- Điền thông tin người kiểm thử/người phê duyệt, môi trường và thời điểm chạy test.
- Đính kèm minh chứng và ghi rõ phiên bản/commit được đánh giá.

## 6. Minh chứng kiểm thử

| Mã minh chứng | Nội dung | Vị trí liên kết / ghi chú |
|---|---|---|
| E-01 | Ảnh chụp responsive mobile, 390×844 | [responsive-mobile.png](screenshots/responsive-mobile.png) |
| E-02 | Ảnh chụp responsive tablet, 768×1024 | [responsive-tablet.png](screenshots/responsive-tablet.png) |
| E-03 | Ảnh chụp responsive desktop, 1440×1000 | [responsive-desktop.png](screenshots/responsive-desktop.png) |
| E-04 | Kết quả kiểm tra trình duyệt/console | [Bổ sung log hoặc ghi chú] |
| E-05 | Kết quả validator/accessibility/performance | [Bổ sung báo cáo công cụ] |
| E-06 | URL môi trường kiểm thử và commit được đánh giá | [Bổ sung thông tin] |
