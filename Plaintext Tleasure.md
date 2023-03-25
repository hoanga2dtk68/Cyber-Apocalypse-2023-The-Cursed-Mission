# Plaintext Tleasure
![image](https://user-images.githubusercontent.com/110059218/227737138-d363992f-51cb-4581-ac1b-016b7bfda547.png)
Đề bài cho chúng ta một file pcap về có đề cập về chuyện sử dụng HTTP và họ ghi lại được lưu lượng truy cập đó
![image](https://user-images.githubusercontent.com/110059218/227737270-21f6aab4-9ab6-43cf-9aa8-20a740f593be.png)
khi vừa mở lên mình đã thấy rất nhiều phương thức GET ở đây nên quyết định export object tất cả rồi lọc file
* Trong giao thức HTTP, phương thức GET được sử dụng để lấy thông tin từ một nguồn tài nguyên trên máy chủ web. Khi một yêu cầu GET được gửi đến máy chủ, máy chủ sẽ trả về nội dung của tài nguyên được yêu cầu trong phần thân của phản hồi HTTP. Phương thức GET có thể được sử dụng để lấy các tài liệu HTML, CSS, JavaScript, hình ảnh và các loại tệp khác từ máy chủ web.
Thử grep tất cả các file xem có file nào chứa flag không khá bất ngờ là lấy được flag luôn
![image](https://user-images.githubusercontent.com/110059218/227737394-35d5818a-a2d4-4618-a517-08c4cf062f2f.png)
