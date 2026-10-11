# README – LAB 5: Cấu hình Firewall pfSense

## 1. Thông tin sinh viên
- **Họ và tên:** Lâm Thái Hòa
- **Mã số sinh viên:1150080053
- **Tên bài Lab:** Lab 5 – Cấu hình Firewall pfSense

## 2. Môi trường thực hiện
- **Firewall:** pfSense CE 2.7.2
- **Máy Domain Controller:** Windows Server 2025
- **Máy DMZ-Web:** Windows Server 2025-2, cài IIS
- **Máy kiểm thử:** Kali Linux
- **Phần mềm ảo hóa:** VMware Workstation

## 3. Nội dung đã thực hiện
- Cấu hình các interface WAN, LAN và DMZ trên pfSense.
- Thiết lập firewall rules cho phép hoặc chặn lưu lượng theo địa chỉ IP, giao thức và cổng.
- **Tình huống 1:** Chặn ICMP nhưng vẫn cho phép DNS và HTTP/HTTPS.
- **Tình huống 2:** Chỉ cho phép Domain Controller truy cập Internet, chặn các host LAN còn lại.
- **Tình huống 3:** Cấu hình rule cô lập DMZ khỏi LAN nhưng vẫn cho phép DMZ truy cập Internet.
- **Tình huống 4:** Cấu hình NAT Port Forward từ WAN port 8080 đến máy DMZ-Web port 80.
- **Tình huống 5:** Bật logging trên rule Block và kiểm tra Firewall Log.
- Thực hiện kiểm thử bằng ping, nslookup, curl và kiểm tra log trên pfSense.

## 4. Kết quả thực hiện
- Cấu hình và kiểm thử các rule firewall theo từng tình huống.
- Kiểm tra việc chặn ICMP, cho phép DNS/Web và phân quyền truy cập Internet.
- Thực hiện cấu hình Port Forward và kiểm tra dịch vụ IIS.
- Quan sát log để xác định lưu lượng bị firewall chặn.

**Lưu ý:** Kết quả Port Forward WAN → DMZ cần được xác nhận bằng truy cập thực tế; không ghi nhận thành công nếu chưa hiển thị được trang IIS qua cổng 8080.

## 5. Cách kiểm tra lại bài Lab
1. Khởi động pfSense và các máy ảo cần thiết cho từng tình huống.
2. Kiểm tra IP, gateway và trạng thái các interface.
3. Vào Firewall → Rules để kiểm tra rule và thứ tự rule.
4. Thực hiện lại các lệnh ping, nslookup hoặc curl theo yêu cầu.
5. Vào Status → System Logs → Firewall để kiểm tra các gói tin bị chặn.

## 6. Lưu ý
- Giữ Anti-Lockout Rule để tránh mất quyền truy cập WebGUI.
- Reset States sau khi thay đổi rule trước khi kiểm thử lại.
- Không bật rule Pass tổng quát khi tình huống yêu cầu chặn lưu lượng cụ thể.
- Đảm bảo rule Block nằm trên rule Pass tổng quát.
- Chỉ bật các máy ảo cần thiết để tiết kiệm RAM.