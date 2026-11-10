# BÀI LÀM –(CHỦ ĐỀ QUẢN LÝ MODEL AI)

- **Mã đề:**
- **Họ tên:**
- **Lớp:**
- **Link repository:**
- **Hệ điều hành (Windows/macOS):**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```shell
pwd
 ls -Force
 mv .\tai_lieu_ban_giao.txt .\docs\
 mkdir backup
 cp .\data\chi_phi_model_thang_11.xlsx .\backup\
 rm .\model_cache_01.tmp
 cd .\logs\
 ls -Force
 cd..
 ls -Force
```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```text

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        11/10/2026   9:24 PM                backup
d-----        11/10/2026   9:21 PM                data
d-----        11/10/2026   9:23 PM                docs
d-----        11/10/2026   9:19 PM                evidence
d-----        11/10/2026   9:21 PM                logs
d-r---        11/10/2026  12:51 PM                web
-a----        11/10/2026  12:51 PM             96 .env
-a----        11/10/2026   9:22 PM              0 bai_lam.md


```

## 4.3. Lọc log vận hành Model AI

### a) Lệnh lọc các dòng ERROR

```shell
Get-Content .\logs\inference.log | Select-String "ERROR" > .\logs\loi_model.txt

```

### 2 dòng đầu tiên trong logs/loi_model.txt

```text
 2 0 2 6 - 1 1 - 1 0   0 8 : 2 7 : 4 5   E R R O R   P O S T   / v 1 / c h a t / c o m p l e t i o n s   m o d e l = C L A U D E - 3 5 
 
 2 0 2 6 - 1 1 - 1 0   0 8 : 3 1 : 1 2   E R R O R   P O S T   / v 1 / a u d i o / t r a n s c r i p t i o n s   m o d e l = W H I S P E R - V 3 

```

### b) Lệnh đếm số dòng WARNING và kết quả

```shell
PS C:\Users\BUI HAI DANG\Downloads\MiniPrjoect\MiniPrjoect\starter-kit\quan-li-model-ai> (Get-Content .\logs\inference.log | Select-String "WARNING").count

```

```text
5

```

## 4.4. Chạy script tong_hop (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```shell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\tong_hop.ps1
```

### Nội dung file logs/tong_hop.txt

```text
=== BAO CAO VAN HANH MODEL AI ===

2026-11-10 08:09:18 WARNING POST /v1/embeddings model=LLAMA-2-OLD
2026-11-10 08:16:05 WARNING GET /v1/fine-tune/jobs-legacy
2026-11-10 08:38:29 WARNING GET /images/model-card-v1.png
2026-11-10 09:01:44 WARNING POST /v1/completions model=DAVINCI-002
2026-11-10 09:14:02 WARNING GET /v1/quota/expired-key




Count    : 6
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property : 


```

## 4.5. README.md và bảo vệ thông tin bí mật

> README.md, .gitignore và .env.example được chấm trực tiếp trên file ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.

- [ ] README.md: Heading 1, hình ảnh (`![Alt](path)`), mô tả có **in đậm**, _in nghiêng_ và `inline code`, bảng, code block, task list, blockquote
- [ ] .gitignore có dòng `.env` (tên file đúng, không có đuôi .txt)
- [ ] .env.example có đủ tên biến, giá trị để trống (tên file đúng, không có đuôi .txt)

## 4.6. Kiểm tra trang web bằng DevTools (F12) và báo cáo lỗi

### Bảng lỗi

| STT | Tab DevTools phát hiện lỗi | Tên file hoặc thông báo lỗi | Cách khắc phục |
| --- | -------------------------- | --------------------------- | -------------- |
| 1   |   network                  |   lỗi logo                  | đổi logo->logo-ai-hub               |
| 2   |   console                  |   lỗi ko hiện bảng          | đổi hienThiBangModel -> hienThiBangModelAI                |

> Ảnh chụp màn hình lưu trong thư mục `evidence/` (network.png, console.png).

### Báo cáo lỗi gửi trưởng nhóm

- **Context:** Tôi là sinh viên năm nhất chưa fix lỗi hiển thị dữ liệu của web bao giờ
- **Expected:** Bây giờ trang web AI của tôi muốn có đủ dữ liệu ở bảng hiển thị giao diện 
- **Actual:** Dữ liệu trên trang web không có gì và tôi vào tab console thấy thông báo lỗi app.js:18 Uncaught ReferenceError: hienThiBangModel is not defined
- **Log:** app.js:18 Uncaught ReferenceError: hienThiBangModel is not defined

### Câu tìm kiếm Google

```text
site:stackoverflow.com "Uncaught ReferenceError: hienThiBangModel is not defined"

```

## 4.7. Excel

> Phần Excel được chấm trực tiếp trên file `data/chi_phi_model_thang_11.xlsx`, không cần ghi vào đây.
