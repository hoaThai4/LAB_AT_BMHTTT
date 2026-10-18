README - LAB 4: KHẢO SÁT VÀ ĐÁNH GIÁ BỀ MẶT MẠNG BẰNG NMAP

Họ và tên: Lâm Thái Hòa
Mã số sinh viên: 1150080053
Tên bài Lab: Lab 4 - Khảo sát và đánh giá bề mặt mạng bằng Nmap

# LAB 4 – Nmap

## 1. Mục tiêu
- Phát hiện máy đang hoạt động trong mạng.
- Quét cổng TCP/UDP và nhận diện dịch vụ.
- Nhận diện hệ điều hành bằng Nmap.
- Sử dụng NSE kiểm tra thông tin SMB và dấu hiệu lỗ hổng.
- Thực hành hardening và so sánh kết quả trước/sau.

## 2. Môi trường
- VMware Workstation
- Kali Linux: `10.0.0.3`
- Metasploitable 2: `10.0.0.20`
- LAN Segment: `lab4-nmap`
- Nmap: `7.99`

## 3. Các lệnh chính
```bash
sudo nmap -sn 10.0.0.0/24
sudo nmap -sS 10.0.0.20
sudo nmap -sT 10.0.0.20
sudo nmap -sV 10.0.0.20
sudo nmap -O 10.0.0.20
sudo nmap -A 10.0.0.20
sudo nmap -p 445 --script smb-os-discovery 10.0.0.20
sudo nmap -p 445 --script smb-vuln-ms17-010 10.0.0.20