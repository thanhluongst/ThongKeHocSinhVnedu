# Thống kê học sinh dân tộc từ vnEdu

Trang web một file (`ThongKeDanToc.html`) dùng để thống kê học sinh dân tộc từ file **danh sách học sinh** xuất từ vnEdu.

- Thống kê từng dân tộc: số lượng, nam, nữ, tỉ lệ (%). Không tính dân tộc Kinh và "Người nước ngoài" (giống cách tính của vnEdu).
- Chia theo toàn trường, khối, cơ sở / phân hiệu; có tùy chọn chi tiết từng lớp.
- Xuất Excel có quốc hiệu, tiêu đề, kẻ khung, chỗ ký; kèm sheet danh sách học sinh dân tộc.
- Dữ liệu chỉ xử lý trong trình duyệt, không gửi lên máy chủ nào.

## Cách dùng

1. Trên vnEdu, xuất danh sách học sinh toàn trường ra Excel (.xls).
2. Mở `ThongKeDanToc.html` bằng Chrome hoặc Edge (cần có mạng để tải thư viện đọc/ghi Excel).
3. Kéo thả file vừa xuất vào trang, xem bảng thống kê, bấm **Xuất Excel**.

Nếu bật GitHub Pages cho kho này, có thể dùng trực tiếp tại `https://<tên-tài-khoản>.github.io/<tên-kho>/ThongKeDanToc.html`.

## Cài đặt

Trong mục **Cài đặt báo cáo** có thể sửa đơn vị chủ quản, tên trường, tiêu đề, năm học và danh sách lớp của từng cơ sở / phân hiệu (ví dụ `6A1-6A4, 7A1-7A4, 9A12`). Cài đặt được lưu lại trên trình duyệt.

Giá trị mặc định nằm trong biến `DEFAULT_CFG` ở đầu phần `<script>`; trường khác dùng thì sửa tại đây.

## Thư viện sử dụng

- [SheetJS](https://sheetjs.com/) – đọc file .xls/.xlsx
- [ExcelJS](https://github.com/exceljs/exceljs) – ghi file Excel có định dạng

> Lưu ý: không đưa file Excel chứa thông tin học sinh lên GitHub. File `.gitignore` đã chặn sẵn các file `.xls`, `.xlsx`, `.csv`.
