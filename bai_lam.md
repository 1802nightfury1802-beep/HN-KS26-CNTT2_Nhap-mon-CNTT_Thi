# BÀI LÀM – HACKATHON 01

- **Mã đề:** 20
- **Họ tên:Bùi Hải Đăng** 
- **Lớp:** 
- **Link repository:** 
- **Hệ điều hành (Windows/macOS):Windows** 

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
  cd .\salon-toc-website\
 pwd
 ls -Force
  mv .\lich_lam_viec.txt .\docs\
  mv .\logo_salon_toc.PNG .\media\
  cp .\media\logo_salon_toc.PNG .\backup
 rm .\temp_289.tmp
  
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit> mkdir docs, media, data, logs, backup


    Directory: C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:35 PM                docs
d-----        10/28/2026   1:35 PM                media
d-----        10/28/2026   1:35 PM                data
d-----        10/28/2026   1:35 PM                logs
d-----        10/28/2026   1:35 PM                backup


PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit> pwd

Path
----
C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit


PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit> cd .\van-phong-pham-website\
cd : Cannot find path 'C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\van-phong-pham-website\' because it
does not exist.
At line:1 char:1
+ cd .\van-phong-pham-website\
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (C:\Users\BUI HA...g-pham-website\:String) [Set-Location], ItemNotFoundE
   xception
    + FullyQualifiedErrorId : PathNotFound,Microsoft.PowerShell.Commands.SetLocationCommand

PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit> cd .\salon-toc-website\
PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> ls -Force


    Directory: C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
------        10/27/2026   1:32 AM             67 .env
-a----        10/27/2026   1:32 AM           6103 hoa_don_salon_thang_11.xlsx
-a----        10/27/2026   1:32 AM             62 lich_lam_viec.txt
-a----        10/27/2026   1:32 AM           6113 logo_salon_toc.PNG
-a----        10/27/2026   1:32 AM           1032 salon.log
------        10/27/2026   1:32 AM             22 temp_289.tmp


PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> pwd

Path
----
C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website


PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> ls -Force


    Directory: C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/28/2026   1:35 PM                backup
d-----        10/28/2026   1:40 PM                data
d-----        10/28/2026   1:35 PM                docs
d-----        10/28/2026   1:41 PM                logs
d-----        10/28/2026   1:35 PM                media
------        10/27/2026   1:32 AM             67 .env
-a----        10/27/2026   1:32 AM             62 lich_lam_viec.txt
-a----        10/27/2026   1:32 AM           6113 logo_salon_toc.PNG
------        10/27/2026   1:32 AM             22 temp_289.tmp


PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> mv .\lich_lam_viec.txt .\docs\
PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> mv .\logo_salon_toc.PNG .\media\
PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> cp .\media\logo_salon_toc.PNG .\backup\
PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> rm .\temp_289.tmp

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```shell
 Get-Content .\logs\salon.log
  Get-Content .\logs\salon.log | Select-String "ERROR"
  Get-Content .\logs\salon.log | Select-String "ERROR" > .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```text
2026-11-28 09:53:35 [ERROR] Khong tim thay trang /kieu-toc-moi (404)
2026-11-28 09:57:35 [ERROR] Khong tim thay trang /kieu-toc-moi (404)

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

```shell
 Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
 .\auto_report.ps1
```

### Kết quả hiển thị

```text

PS C:\Users\BUI HAI DANG\Downloads\starter-kit (7)\starter-kit\salon-toc-website> .\auto_report.ps1
Dang loc log...
Hoan Thanh!
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```shell
 (Get-Content .\logs\salon.log | Select-String "ERROR").count

```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```text
6

```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```shell
  "=== TONG HOP LOG ===" > .\logs\tong_hop.txt
   "cac dong chua WARNING" >> .\logs\tong_hop.txt
   et-Content .\logs\salon.log | Select-String "WARNING" >> .\logs\tong_hop.txt
    "so dong chua ERROR" >> .\logs\salon.log
     (Get-Content .\logs\salon.log | Select-String "ERROR").count >> .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```text
=== TONG HOP LOG ===
cac dong chua WARNING

2026-11-28 09:33:35 [WARNING] Anh kieu toc dung luong lon
2026-11-28 09:37:35 [WARNING] Lich toi thu sau sap kin
2026-11-28 10:01:35 [WARNING] Anh kieu toc dung luong lon
2026-11-28 10:09:35 [WARNING] Thoi gian phan hoi cham



```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/hoa_don_salon_thang_11.xlsx`, không cần ghi vào đây.
