# Phần 1. Phân tích 

## 1. Phân tích (Input/Output)

Input (Đầu vào): Bao gồm tên và mô tả CLB Lập trình PTIT, danh sách các ban và trưởng ban, địa chỉ email liên hệ, hướng dẫn gia nhập, các nhiệm vụ thành viên mới cần hoàn thành, thời hạn đăng ký và quy tắc ứng xử. Toàn bộ nội dung được viết bằng cú pháp Markdown.

Output (Đầu ra): Một file `README.md` hoàn chỉnh được lưu trên GitHub. Khi render, tài liệu hiển thị thành trang Wiki có tiêu đề phân cấp, chữ in đậm, bảng thông tin, email có thể nhấp vào, danh sách hướng dẫn, khối lệnh Git, checklist và phần lưu ý quan trọng. Thành viên có thể đọc trực tiếp trên trình duyệt mà không cần Microsoft Word.

## 2. Đề xuất giải pháp

|Phần|Nội dung|Cú pháp Markdown|
|-|-|-|
|1|Giới thiệu CLB|Heading `#`, `##`, Bold `**`
|2|Danh sách Ban|Table `\|`, Link `mailto:`|
|3|Hướng dẫn gia nhập|Ordered List `1.`, Code Block ` ```bash`|
|4|Checklist nhiệm vụ|Task List `- [x]`, `- [ ]`|
|5|Lưu ý quan trọng|Blockquote `>`, Bold `**`|

## 3. Thiết kế các bước thực hiện

1.  Thu thập thông tin CLB, các ban, trưởng ban và nội dung hướng dẫn.
    
2.  Tạo repository trên GitHub và tạo file `README.md`.
    
3.  Chia tài liệu thành 5 phần bằng Heading H1/H2.
    
4.  Viết nội dung giới thiệu, bảng thông tin và hướng dẫn gia nhập.
    
5.  Thêm Code Block chứa lệnh Git, Task List và Blockquote.
    
6.  Kiểm tra email `mailto:`, URL và cú pháp Markdown.
    
7.  Sử dụng GitHub Preview để kiểm tra giao diện trước khi hoàn thiện.
    
8.  Commit file lên GitHub và phân công người chịu trách nhiệm cập nhật.
    

# Phần 2. Triển khai và chống lỗi

## 4. Source file CLB Lập Trình PTIT hoàn chỉnh

Đã tạo file gồm đầy đủ 5 phần theo yêu cầu, có bảng email `mailto:`, Code Block Git, Task List và Blockquote.

**[CLB Lập Trình PTIT](https://github.com/lucasfpsne/HNKS26CNTT1_NMCNTT_Session09_Ex09/blob/main/README.md)**

Các tên trưởng ban, địa chỉ email và thời hạn trong file là thông tin minh họa, cần thay bằng thông tin chính thức trước khi đăng lên GitHub.

## 5. Trả lời hai bẫy dữ liệu

Bẫy 1: Email phải là liên kết bấm được

Sử dụng cú pháp:

`[kythuat@example.com](mailto:kythuat@example.com)`

Khi người dùng nhấp vào, hệ thống sẽ yêu cầu mở ứng dụng email được cấu hình trên thiết bị để soạn thư gửi đến địa chỉ đó. Nếu chỉ ghi email thông thường, không thể bảo đảm nó sẽ trở thành liên kết bấm được.

Bẫy 2: URL không hợp lệ

Nếu thành viên viết `[GitHub](github.com)` mà thiếu `https://`, Markdown thường hiểu `github.com` là đường dẫn tương đối. Khi nhấp vào, trình duyệt có thể chuyển đến đường dẫn thuộc website hiện tại thay vì GitHub.

Nếu URL sai định dạng nghiêm trọng, liên kết có thể không được render đúng. Nếu URL đúng cú pháp nhưng trỏ đến trang không tồn tại, người dùng có thể gặp lỗi 404.

Cách khắc phục: Sử dụng URL đầy đủ như `[GitHub](https://github.com/)` và kiểm tra liên kết bằng GitHub Preview trước khi công bố.
