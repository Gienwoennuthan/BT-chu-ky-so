Hệ Thống Xác Thực Chữ Ký Số
Giới Thiệu
Hệ thống này cung cấp chức năng tạo khóa RSA, ký điện tử vào file và xác minh chữ ký số trên file. Ứng dụng được xây dựng bằng Python với framework Flask và thư viện cryptography.

Tính Năng Chính
Tạo cặp khóa RSA:

Tạo khóa private và public key

Tải về dưới dạng file zip

Ký điện tử file:

Upload file cần ký

Tạo chữ ký số bằng private key

Tải về file chữ ký (.sig)

Xác minh chữ ký:

Upload file gốc, file chữ ký và public key

Kiểm tra tính hợp lệ của chữ ký

Hiển thị kết quả xác minh

Yêu Cầu Hệ Thống
Python 3.7+

Các thư viện Python cần thiết:

bash
pip install flask cryptography
Cài Đặt và Chạy Ứng Dụng
Clone repository hoặc tải source code

Cài đặt các thư viện cần thiết:

bash
pip install -r requirements.txt
Chạy ứng dụng:

bash
python app.py
Truy cập ứng dụng qua trình duyệt:

text
http://localhost:5000
Hướng Dẫn Sử Dụng
1. Tạo Cặp Khóa RSA
Truy cập trang chủ và nhấn nút "Tạo khóa"

Hệ thống sẽ tạo và tải về file rsa_keys.zip chứa:

private_key.pem: Khóa bí mật (giữ an toàn)

public_key.pem: Khóa công khai (có thể phân phối)

2. Ký Điện Tử File
Truy cập trang "Ký file"

Chọn file cần ký và nhấn "Tải lên"

Hệ thống sẽ tạo chữ ký và tải về file .sig

3. Xác Minh Chữ Ký
Truy cập trang "Xác minh"

Tải lên 3 file:

File gốc cần kiểm tra

File chữ ký (.sig)

Public key (.pem)

Hệ thống sẽ hiển thị kết quả xác minh:

"Chữ ký hợp lệ" nếu đúng

"Chữ ký không hợp lệ" nếu sai

Kiến Trúc và Bảo Mật
Sử dụng thuật toán RSA với độ dài khóa 2048 bit

Ký và xác minh bằng thuật toán PSS với SHA-256

Private key được lưu ở định dạng PEM không mã hóa (chỉ dùng cho mục đích demo)

Trong môi trường production, cần bảo vệ private key cẩn thận

Thư Mục và File Quan Trọng
keys/: Thư mục chứa các khóa RSA

uploads/: Thư mục tạm chứa file upload

templates/: Chứa các file template HTML

app.py: File chính chứa logic ứng dụng

Hạn Chế và Hướng Phát Triển
Hạn Chế Hiện Tại
Chưa hỗ trợ nhiều loại file cùng lúc

Giao diện người dùng cơ bản

Chưa có hệ thống quản lý khóa tập trung

Hướng Phát Triển Trong Tương Lai
Thêm chức năng ký nhiều file cùng lúc

Cải thiện giao diện người dùng

Tích hợp với hệ thống PKI

Thêm chức năng hết hạn chữ ký

Hỗ trợ các thuật toán khác như ECDSA

Bảo Mật và Lưu Ý
⚠️ Lưu ý quan trọng: Đây là ứng dụng demo, không nên sử dụng trong môi trường production.

Private key trong ứng dụng này không được mã hóa

Ứng dụng chưa có cơ chế bảo vệ chống tấn công DDoS

Luôn đảm bảo an toàn khi lưu trữ private key

Không sử dụng khóa được tạo ra từ ứng dụng này cho mục đích quan trọng

Liên Hệ
Nếu có bất kỳ câu hỏi hoặc đóng góp nào, vui lòng liên hệ qua email: huonggiang09082005@gmail.com
<img width="1198" alt="Screenshot 2025-06-12 at 14 49 29" src="https://github.com/user-attachments/assets/fda149f7-157b-4a4f-b0fb-4d12d45fd380" />

LƯU HƯƠNG GIANG CNTT17-07
