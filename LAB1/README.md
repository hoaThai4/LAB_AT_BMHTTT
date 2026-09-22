# LAB_AT_BMHTTT
# README – Lab 1: Bắt gói tin Telnet – SSH

Họ và tên: Lâm Thái Hòa
MSSV:1150080053
Tên bài Lab: Lab 1 – Bắt gói tin Telnet – SSH

## Nội dung thực hiện
- Sử dụng 3 máy ảo: Kali Linux, Windows 11 và Windows Server 2025.
- Windows 11 đóng vai trò Client, Windows Server 2025 đóng vai trò Server.
- Kali Linux sử dụng Wireshark để bắt và phân tích gói tin.
- Thực hiện kết nối SSH từ Windows 11 đến Windows Server 2025.
- Bắt gói SSH bằng Wireshark với bộ lọc: tcp.port == 22.

## Kết quả
- Kết nối SSH giữa Client và Server thành công.
- Wireshark bắt được các gói tin SSH.
- Nội dung phiên SSH được mã hóa và hiển thị dưới dạng Encrypted Packet.

## Lưu ý
- 3 máy ảo phải cùng mạng và kết nối được với nhau.
- SSH Server phải đang chạy và mở cổng 22.
- Kali Linux chọn đúng card mạng khi bắt gói.
- Để chạy lại bài: mở 3 máy ảo → kiểm tra IP → khởi động SSH Server → mở Wireshark → thực hiện SSH từ Client.