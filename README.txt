========================================================================
BÀI 1: ỨNG DỤNG GỬI VÀ NHẬN THÔNG ĐIỆP MQTT CƠ BẢN
========================================================================

1. BROKER SỬ DỤNG:
- Tên Broker: Local Eclipse Mosquitto Broker
- Host / IP: localhost
- Cổng (Port): 1883
- Topic: iot/lab/message

2. CÁCH CHẠY TỪNG CHƯƠNG TRÌNH:
(Mở 2 cửa sổ Terminal)

- Terminal 1: Chạy Subscriber để lắng nghe thông điệp trước
  Lệnh chạy: python subscriber_bai1.py

- Terminal 2: Chạy Publisher để phát thông điệp
  Lệnh chạy: python publisher_bai1.py

3. KẾT QUẢ ĐẠT ĐƯỢC:
- Kết nối tới Broker thành công tại địa chỉ localhost:1883.
- Publisher gửi thành công thông điệp Le Huy Duc, B23DCCN169 và lời chào lên topic 'iot/lab/message'.
- Subscriber nhận thông điệp ngay lập tức và hiển thị đầy đủ thông tin:
  + Topic nhận được: iot/lab/message
  + Nội dung Payload: Xin chao tu client Python MQTT - B23DCCN169 - Le Huy Duc
  + Thời điểm nhận: Giờ:Phút:Giây (HH:MM:SS)
========================================================================
