# LenaHash<sup>TM</sup>
> **NOTE:** Vietnamese only.

![Big picture](images/lenahash.png)
<p>
Mấy ngày gần đây giới mộ điệu học máy xôn xao về Apple CSAM và cụ thể hơn là NeuralHash<sup>TM</sup>. Đại loại là Apple sẽ trích xuất các bức ảnh dưới dạng 1 hash(96 bits) tạo ra bởi neural network (cụ thể trong bản demo là MobileNetV3, 200 layers) để phát hiện các bức hình gần trùng lặp (kể cả resize, crop, xoay ảnh, filtering như đổi màu). Chi tiết kỹ thuật ở đây [1]</p>

<p>
Thực ra việc quét ảnh/photos trên các dịch vụ cloud không mới đối với các Big Tech như Google, Facebook, Microsoft. Điểm khác biệt là Apple xử lý việc so trùng này trên thiết bị người dùng bằng cách nạp vào 1 bộ cơ sở dữ liệu cần so khớp được mã hoá, để tạo ra các voucher gửi lên iCloud. Nhiều người lo lắng về khả năng mở rộng truy quét trên các loại dữ liệu khác như văn bản, tin nhắn khi có các yêu cầu từ Big Bros khác, ảnh hưởng đến quyền riêng tư cá nhân.</p>

<p>
Một số nhóm kỹ thuật đã tìm ra các phiên bản thử nghiệm và khai thác thành công việc tạo nên các hash giống nhau từ những bức hình hoàn toàn trông có vẻ khác nhau. Ví dụ như Lena và Lion đều cùng mã hash 32da5083d4f9db9d45b4c397 trong thí nghiệm của tôi. Các bạn có thể thử nghiệm dựa trên các repo này.[2]</p>

<p>
Thực ra phương pháp tấn công này khá là thô sơ, nhưng hệ thống CSAM detection sẽ bị quá tải bởi false alarm, cảnh báo giả dẫn đến chi phí tài nguyên để hỗ trợ hậu kiểm cho các báo cáo sau này.</p>

### References

1. ![CSAM](https://www.apple.com/child-safety/pdf/CSAM_Detection_Technical_Summary.pdf)
2. ![NeuralHashCollider](https://github.com/anishathalye/neural-hash-collider)

