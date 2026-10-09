**Bài 3 : Kiến trúc sư hạ tầng server chuyên nghiệp** 

\*Bản phác thảo sơ đồ luồng IPO (Input – Process – Output) của việc khởi tạo hạ tầng này.

\-Input: Tên thư mục, tên file, đường dẫn  
\-Process: Dùng PowerShell để tạo thư mục, tạo file và sao chép file sang thư mục khác bằng lệnh Copy-Item  
\-Output: Hoàn thành cây thư mục có tên Smart-Farm và sao chép bản sao trong backup\\code\_v1 

\*Danh sách các câu lệnh **PowerShell** đã sử dụng.
 New-Item \-ItemType Directory \-Force \-Path  "smart-farm\\data\\logs","smart-farm\\code"     
 New-Item \-ItemType File \-Force \-Path "smart-farm\\code\\config.json","smart-farm\\code\\[sensors.py](http://sensors.py)","smart-farm\\code\\.env"  
 attrib \+h "smart-farm\\code\\.env"  
New-Item \-ItemType Directory \-Force \-Path "backup"  
 Copy-Item \-Path "smart-farm\\code" \-Destination "backup\\code\_v1" \-Recurse \-Force  
