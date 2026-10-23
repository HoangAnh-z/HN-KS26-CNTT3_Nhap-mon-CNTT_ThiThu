# BÀI LÀM – THI THỬ HACKATHON 01

- **Mã đề:** Thi thử
- **Họ tên: Bùi Hoàng Anh
- **Lớp:** HN_K26-CNTT3
- **Link repository:** https://github.com/HoangAnh-z/HN-KS26-CNTT3_Nhap-mon-CNTT_ThiThu.git
- **Hệ điều hành (Windows/macOS):** MacOS

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```bash
pwd
ls -la
mv nhap_hang.txt docs
mv logo_van_phong_pham.png
rm tempt_131.tmp
cd logs ; ls -la ; cd ..

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text
.			.env			data			logs
..			backup			docs			media
.DS_Store		bai_lam.md		logo_van_phong_pham.png	nhap_hang.txt

./backup:
.	..

./data:
.			..			don_ban_thang_10.xlsx

./docs:
.	..

./logs:
.		..		shop.log

./media:
.	..

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```bash
grep "ERROR" logs/shop.log > logs/daily_report.txt
cat logs/daily_report.txt
```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```bash
bash auto_report.sh
```

### Nội dung file logs/auto_report.txt

```text
=== BAO CAO LOI ===
2025-10-28 08:24:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:30:28 [ERROR] Thanh toan bi tu choi
2025-10-28 08:33:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:39:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 08:42:28 [ERROR] Ket noi kho du lieu that bai
2025-10-28 09:12:28 [ERROR] Thanh toan bi tu choi
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```bash
grep "ERROR" logs/shop.log | wc -l
```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```bash
touch ./logs/tong_hop.txt
echo "=== TONG HOP LOG ===" > logs/tong_hop.txt
grep "WARNING" logs/shop.log >> logs/tong_hop.txt
grep -c "ERROR" logs/shop.log >> logs/tong_hop.txt
```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===
2025-10-28 08:51:28 [WARNING] Thoi gian tai trang cham
2025-10-28 08:54:28 [WARNING] Anh san pham dung luong lon
2025-10-28 08:57:28 [WARNING] Thoi gian tai trang cham
6
```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/don_ban_thang_10.xlsx`, không cần ghi vào đây.
