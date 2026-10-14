# **EXERCISE 01**  
## Phần 1. Phân tích  
Hai sai lầm trong tư duy của Nam  
- Nhầm lẫn mục đích sử dụng giữa tài liệu định dạng dòng đời cuối (End-user Document) và tài liệu mã nguồn (Source Control/Documentation): Nam sử dụng file .docx đưa lên Git – hệ thống quản lý mã nguồn vốn tối ưu cho văn bản thuần túy (plain text). Bản chất .docx là một tệp nén ZIP chứa các file XML cấu trúc phức tạp và dữ liệu nhị phân. Khi lưu trữ trên Git, hệ thống không thể đọc hiểu sự thay đổi từng dòng (line-by-line diff) mà chỉ coi đó là một cục dữ liệu nhị phân lớn. Chỉ cần thay đổi một dấu phẩy, Git buộc phải lưu lại toàn bộ phiên bản mới hoặc báo xung đột toàn bộ file.  
- Đánh đồng "văn bản thô" với "thiếu chuyên nghiệp": Nam cho rằng giao diện WYSIWYG (What You See Is What You Get) của Word mới tạo ra tài liệu chuyên nghiệp. Thực tế, Markdown sử dụng các ký hiệu cú pháp tối giản nhưng được các nền tảng như GitHub, GitLab hỗ trợ hiển thị tự động thành các định dạng chuẩn hóa, trực quan, hỗ trợ biểu đồ, bảng biểu, đoạn mã nguồn (code blocks) và công thức toán học vô cùng chuyên nghiệp mà không bị phụ thuộc vào phần mềm soạn thảo độc quyền.  
Tại sao Markdown an toàn và nhẹ hơn?  
- Trọng lượng (Lighter): File Markdown (.md) chỉ chứa các ký tự văn bản thuần túy (Plain Text), dung lượng thường chỉ vài kilobyte, giúp thao tác clone, push, pull trên Git diễn ra tức thì.  
- Độ bền vững chống hư hại (Safer): Định dạng .docx cấu thành từ cấu trúc nén XML. Nếu một lỗi mạng xảy ra làm mất hoặc hỏng dù chỉ 1 byte ở vùng tiêu đề hoặc trung tâm tệp, cấu trúc giải nén bị phá vỡ và toàn bộ file .docx sẽ hỏng hoàn toàn (không thể mở bằng Microsoft Word). Ngược lại, tệp Markdown là văn bản thuần túy; nếu mất một vài byte dữ liệu, phần lớn văn bản còn lại vẫn đọc được bình thường bằng bất kỳ trình soạn thảo văn bản nào, cho phép dễ dàng khôi phục thủ công.  
## Phần 2. Hoàn thiện  
Dưới đây là đoạn giới thiệu dự án mẫu được chuyển đổi sang định dạng Markdown (.md) qua StackEdit:  
Markdown  
# Dự án Quản lý Kho Thông minh (PTIT)  
## 1. Mẫu giới thiệu  
Hệ thống tự động hóa kiểm kê kho hàng, giúp giảm thiểu sai sót thủ công và tối ưu thời gian vận hành.  
## 2. Công nghệ & Thành viên  
- **Công nghệ:** ReactJS, Node.js, MongoDB, Git.  
- **Thành viên:**   
  - Nguyễn Văn Nam (B23DCVT001) - Lead  
  - Trần Thị Hoa (B23DCVT002) - Dev  
## 3. Khởi chạy nhanh  
```bash  
git clone [https://github.com/ptit-group/smart-warehouse.git](https://github.com/ptit-group/smart-warehouse.git)  
npm install && npm run dev  
   
