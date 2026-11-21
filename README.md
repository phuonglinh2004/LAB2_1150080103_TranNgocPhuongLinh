# LAB 2 - MÃ HÓA ĐỐI XỨNG HIỆN ĐẠI

## Thông tin sinh viên
- **Họ và tên:** Trần Ngọc Phương Linh
- **MSSV:** 1150080103
- **Lớp:** 11_ĐH_CNPM2
- **Học phần:** An toàn và Bảo mật thông tin

---

## Cấu trúc thư mục
- `LAB2_MaHoaHienDai/`: Mã nguồn dự án Java Swing (Maven), bao gồm `pom.xml`, các tệp script `.sql`, các lớp xử lý thuật toán (`DESCipher`, `TripleDESCipher`, `AESCipher`, `RC4Cipher`, `TwofishCipher`, `AESCTRCipher`), các lớp kết nối SQL Server (`DbConfig`, `HistoryDao`, `UserDao`) và giao diện (`.java`, `.form`).
- `LAB2_Python/`: Chương trình mã hóa/giải mã AES-256-CBC viết bằng Python Tkinter (`aes_cbc_gui.py`).
- `11CNPM2-LAB11_1150080103-TranNgocPhuongLinh_2.docx`: Báo cáo và hình ảnh minh chứng kết quả thực hiện các bài 2.1 – 2.6.

---

## Hướng dẫn cài đặt và chạy chương trình

### 1. Cơ sở dữ liệu SQL Server
1. Mở **SQL Server Management Studio (SSMS)**, kết nối bằng Windows Authentication.
2. Mở và chạy lần lượt 2 tệp trong thư mục `LAB2_MaHoaHienDai`: `01_Tao_CSDL.sql` và `02_Tao_Tai_Khoan_SQL.sql` để tạo CSDL `LAB2_MaHoaHienDai`, các bảng `dbo.app_users`, `dbo.crypto_history` và tài khoản thực hành `lab2_user`.
3. Đảm bảo SQL Server Express mở cổng TCP/IP `14333` và bật chế độ xác thực hỗn hợp (*SQL Server and Windows Authentication mode*).

### 2. Ứng dụng Java Swing (Bài 2.1 – 2.6)
1. Mở **Apache NetBeans** (JDK 17 trở lên), chọn **File -> Open Project...** và mở thư mục `LAB2_MaHoaHienDai`.
2. Nhấn phải project chọn **Clean and Build** (`Shift + F11`) để Maven tải thư viện `mssql-jdbc` và `bcprov-jdk18on`.
3. Nhấn **Run** (`F6`) để mở giao diện menu chính `frm_Menu`.
4. Chọn **Kết nối SQL Server**, nhập thông tin kết nối (`127.0.0.1`, port `14333`, database `LAB2_MaHoaHienDai`, user `lab2_user` và mật khẩu thực hành đã cấu hình) rồi bấm **Test Connection** trước khi thao tác các bài 2.1 – 2.6 và xem lịch sử.

### 3. Ứng dụng Python AES-CBC (Bài 2.6 - Bài 02)
1. Mở **Command Prompt (CMD)** và cài đặt thư viện `cryptography`:
   ```bash
   py -m pip install cryptography
   ```
2. Di chuyển vào thư mục `LAB2_Python` và chạy tự kiểm thử:
   ```bash
   py aes_cbc_gui.py --self-test
   ```
3. Chạy giao diện đồ họa Tkinter:
   ```bash
   py aes_cbc_gui.py
   ```
