# Artifacts of Dangerous Sightings
![image](https://user-images.githubusercontent.com/110059218/227738253-74da176a-b8ce-435b-aabb-2855b9e4a064.png)
Bài cho mình một file disk mình dùng FTK Imager để phân tích disk

Đầu bài có đề cập đến việc có thể đã bị xóa event log và mình nghĩ họ đã xóa bằng cách nào và xóa để làm gì, sau khi search google thì mình có thấy đề cập đến việc xóa bằng powershell thì có thể xem lại thông qua lịch sử của nó
* Bài viết bạn có thể tham khảo tại [đây](https://g2.by/9TmvKh) hoặc tại [đây](https://anonyviet.com/xoa-tat-ca-event-logs-tren-windows/)
![image](https://user-images.githubusercontent.com/110059218/227738766-ac170520-4168-415e-aaef-88509318e35e.png)
về vị trí của file mình thực hiện google và nhận được path để dẫn đến file
![image](https://user-images.githubusercontent.com/110059218/227738793-84fa1704-bff3-485f-adec-fe39ffe3b46e.png)
sau khi đọc lại nội dung của các lệnh chạy trên powershell thì phát hiện có một file đã được nhúng vào trong file ActiveSyncProvider.dll
![image](https://user-images.githubusercontent.com/110059218/227739059-fe1271b7-02e0-4f9e-99a2-869ff7021628.png)
Trích xuất file được nhúng ra  thì nhận thấy nó là một đoạn base64 thử ném lên cyberchef để decode thì nhận ra tác giả đã obfuscate
![image](https://user-images.githubusercontent.com/110059218/227739124-4f6d5d46-34c2-4773-9047-79e5fdd49bef.png)
Sau khi mất thời gian một lúc làm sao để deobfuscate thì mình có hỏi idol **51LV3R KN16H7 KM4** thì mình nhận được một tool la PSDECODE để xử lý các bài tác giả sử dụng obfuscate

**Obfuscate là quá trình sửa đổi mã nguồn một chương trình máy tính để làm cho nó khó hiểu và khó khăn trong việc phân tích, ngăn chặn việc sao chép hoặc sửa đổi code. Quá trình này thường được sử dụng để bảo vệ các ứng dụng của công ty tránh khỏi việc sao chép bởi các đối thủ cạnh tranh hoặc những kẻ tấn công độc hại.
Việc obfuscate có thể bao gồm việc thay đổi tên biến, phương thức, lớp, hoặc thậm chí là việc sử dụng các kỹ thuật mã hóa khác nhau để che giấu mã nguồn. Mã obfuscated vẫn có thể chạy được bình thường nhưng rất khó hiểu và khó được giải mã.
Tuy nhiên, việc obfuscate không phải là một giải pháp an toàn tuyệt đối, vì sau khi mã đã được obfuscated, có thể sử dụng các công cụ để giải mã lại mã nguồn ban đầu.**

Bạn có thể tải tool tại [đây](https://www.youtube.com/watch?v=iQ0zj1RnaMs) hoặc ở [đây](https://github.com/Malandrone/PowerDecode)

sau khi ném file lên tool thì mình nhận được flag luôn
![image](https://user-images.githubusercontent.com/110059218/227739422-89ca37aa-6c6e-442b-96ce-7145fb0549a4.png)
flag: HTB{Y0U_C4nt_St0p_Th3_Alli4nc3}
