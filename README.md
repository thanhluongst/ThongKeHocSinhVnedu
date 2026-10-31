# Thống kê số lượng học sinh từ vnEdu

Trang web một file (`ThongKeDanToc.html`) lập bảng **thống kê số lượng học sinh** theo mẫu vnEdu từ file **danh sách học sinh** xuất từ vnEdu.

- Các cột: Tổng số HS, Nữ, Dân tộc, chi tiết từng dân tộc (SL, nam, nữ, tỉ lệ %), Nữ dân tộc, Khuyết tật, Diện chính sách.
- Không tính dân tộc Kinh và "Người nước ngoài" (giống cách tính của vnEdu).
- Chuyển đi, chuyển đến, thôi học không có trong file danh sách nên không thống kê.
- Chia theo toàn trường, khối, cơ sở / phân hiệu; có tùy chọn chi tiết từng lớp.
- Xuất **danh sách học sinh từng lớp theo mẫu A4** (mỗi lớp một sheet): nơi sinh ghi theo tỉnh sau sáp nhập, chỗ ở dạng "ấp, xã", bảng thống kê theo năm sinh, dân tộc, chỗ ký; chọn lớp theo cơ sở; tùy chọn lấy lại số đăng bộ, lưu ban, bỏ học từ file A4 cũ; kèm sheet "Kiểm tra dữ liệu" (thiếu mã định danh, nơi sinh, năm sinh bất thường…).
- Xuất Excel có quốc hiệu, tiêu đề, kẻ khung, chỗ ký; kèm sheet danh sách học sinh dân tộc, khuyết tật, diện chính sách để đối chiếu.
- Dữ liệu chỉ xử lý trong trình duyệt, không gửi lên máy chủ nào.

## Thống kê giáo viên

Tab **Giáo viên** đọc file xuất bằng "Xuất Excel Cấp 2 Mẫu CSDL Bộ" và xuất file Excel gồm 4 sheet:

- **Thống kê chung**: theo toàn trường, CBQL, giáo viên, nhân viên (SL, nữ): dân tộc, tôn giáo, Đảng, Đoàn, độ tuổi, số năm công tác, hợp đồng, chức vụ, ngạch/hạng, các loại trình độ, bồi dưỡng, đánh giá viên chức, giáo viên giỏi.
- **Giáo viên theo môn**: số lượng, trình độ, hạng, tiết dạy trung bình, dạy giỏi, đánh giá theo từng môn (chỉ tính vị trí "Giáo viên").
- **Danh sách**: để đối chiếu, không kèm CCCD, BHXH, điện thoại, email.
- **Cần thông báo bổ sung**: người thiếu hoặc nhập sai thông tin, kèm sẵn nội dung thông báo cho từng người.

Mục **Cần thông báo bổ sung** trên trang liệt kê người thiếu, sai thông tin; lọc theo vị trí hoặc từng mục, sao chép nội dung thông báo cho từng người hoặc cả danh sách, xuất riêng danh sách ra Excel. Ngạch/hạng, hệ số lương, ngày hưởng không kiểm tra với hợp đồng theo nghị định; môn dạy, số tiết chỉ kiểm tra với giáo viên; tin học, ngoại ngữ chỉ kiểm tra với giáo viên và CBQL.

## Cách dùng

1. Trên vnEdu, xuất danh sách học sinh toàn trường ra Excel (.xls).
2. Mở `ThongKeDanToc.html` bằng Chrome hoặc Edge (cần có mạng để tải thư viện đọc/ghi Excel).
3. Kéo thả file vừa xuất vào trang, xem bảng thống kê, bấm **Xuất Excel**.

Dùng trực tiếp trên web: **https://thanhluongst.github.io/ThongKeHocSinhVnedu/**

## Cài đặt

Trong mục **Cài đặt báo cáo** có thể sửa đơn vị chủ quản, tên trường, tiêu đề, năm học và danh sách lớp của từng cơ sở / phân hiệu (ví dụ `6A1-6A4, 7A1-7A4, 9A12`). Cài đặt được lưu lại trên trình duyệt.

Giá trị mặc định nằm trong biến `DEFAULT_CFG` ở đầu phần `<script>`; trường khác dùng thì sửa tại đây.

## Thư viện sử dụng

- [SheetJS](https://sheetjs.com/) – đọc file .xls/.xlsx
- [ExcelJS](https://github.com/exceljs/exceljs) – ghi file Excel có định dạng

> Lưu ý: không đưa file Excel chứa thông tin học sinh lên GitHub. File `.gitignore` đã chặn sẵn các file `.xls`, `.xlsx`, `.csv`.
