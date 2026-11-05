# Bài làm – GreenField FC

Họ và tên: ____________________  
Lớp: ____________________

## 4.2 Thao tác CLI
Lệnh đã chạy:ls -Force
mkdir backup
 cp .\data\danh-sach-cau-thu.xlsx .\backup\
 rm .\temp_002.tmp
 cd .\logs\
 ls -Force
  Directory: C:\Users\admin\Downloads\Starter_Kit_GreenField_FC\starter-k
    it\greenfield-fc\logs


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----         11/5/2026   1:31 PM            560 access.log


PS C:\Users\admin\Downloads\Starter_Kit_GreenField_FC\starter-kit\greenfield-fc\logs>
## 4.3 Lọc log
**a) Lệnh lọc status=500:*cat .\logs\access.log | Select-String "status=500" > .\logs\loi_500.txt*

Hai dòng đầu của loi_500.txt:2026-10-28 18:03:25 GET /api/players status=500
2026-10-28 18:05:12 GET /api/players status=500

**b) Lệnh đếm status=404 và kết quả:* (cat .\logs\access.log | select-string "status=404").count*
4

## 4.4 Script báo cáo
Lệnh chạy script:gc logs/access.log | Select-String "status=404" >> logs/tong_hop.txt

(gc logs/access.log | Select-String "status=500").count >> logs/tong_hop.txt

Nội dung logs/tong_hop.txt:Script: tong_hop.ps1 
Tac gia: Nguyễn Thuận Phát
Ngay tao: 05/11/2026
echo "Dang tao bao cao..."
Write-Host "Dang tao bao cao..." 

"=== BAO CAO GREENFIELD FC ===" >logs/tong_hop.txt

gc logs/access.log | Select-String "status=404" >> logs/tong_hop.txt

(gc logs/access.log | Select-String "status=500").count >> logs/tong_hop.txt

## 4.6 Kiểm tra website và báo cáo lỗi
| Tab | Tên file/thông báo | Cách khắc phục |
|---|---|---|
| Network | | |
| Console | | |

**Context:**

**Expected:**

**Actual:**

**Log:**

Câu tìm kiếm Google:

## Ghi chú Excel
Công thức/khó khăn đã gặp:
