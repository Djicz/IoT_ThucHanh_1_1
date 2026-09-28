# BÀI 1: ỨNG DỤNG GỬI VÀ NHẬN THÔNG ĐIỆP MQTT CƠ BẢN

## 1. Broker sử dụng
- **Tên Broker:** Local Eclipse Mosquitto Broker
- **Host / IP:** `localhost`
- **Port:** `1883`
- **Giao thức:** MQTT TCP
- **Topic:** `iot/lab/message`

---

## 2. Cách chạy từng chương trình

Mở **2 cửa sổ Terminal**:

1. **Terminal 1 - Chạy chương trình Subscriber (Lắng nghe):**
   ```bash
   python subscriber_bai1.py
   ```
   *Chương trình sẽ kết nối tới Broker và liên tục lắng nghe topic `iot/lab/message`.*

2. **Terminal 2 - Chạy chương trình Publisher (Gửi thông điệp):**
   ```bash
   python publisher_bai1.py
   ```
   *Chương trình sẽ kết nối tới Broker, gửi thông điệp chứa Họ tên, MSV, Lời chào rồi tự động ngắt kết nối.*

---

## 3. Kết quả đạt được

### Output tại Terminal Publisher:
```text
Dang ket noi toi MQTT Broker...
[*] Ket noi thanh cong toi Broker: localhost:1883

--- DANG GUI MESSAGE ---
Topic  : iot/lab/message
Payload: Xin chao tu client Python MQTT - B23DCCN169 - Le Huy Duc
[+] Da gui message thanh cong!
[*] Da ngat ket noi.
```

### Output tại Terminal Subscriber:
```text
Dang ket noi toi MQTT Broker...
[*] Ket noi thanh cong toi Broker: localhost:1883
[*] Dang lang nghe tren topic: 'iot/lab/message'...
[*] Nhan Ctrl+C de dung chuong trinh.
========================================

Nhan duoc message:
Topic  : iot/lab/message
Payload: Xin chao tu client Python MQTT - B23DCCN169 - Le Huy Duc
Time   : 10:15:20
----------------------------------------
```

### Đánh giá:
- Kết nối thành công và ổn định tới MQTT Broker.
- Publisher publish thông điệp đúng topic và đúng định dạng yêu cầu.
- Subscriber nhận tin nhắn tức thời và hiển thị đầy đủ Topic, Payload, Thời gian nhận.
