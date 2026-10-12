# Bộ test 20 case

- **Tổng:** 20 case, 5 lĩnh vực, mỗi lĩnh vực 4 case
- **Phân bố đáp án:** A=5, B=5, C=5, D=5 (tránh model đoán theo vị trí)
- **Cách chạy:** copy khối prompt trong code block, so output với "Đáp án đúng"
- **Gợi ý:** thêm câu `Chỉ trả lời bằng một chữ cái.` vào System nếu muốn chấm tự động
- **Độ ổn định:** mỗi case nên chạy 3-5 lần mỗi model (temperature > 0)

---

## Lĩnh vực 1: Customer Support

### Test 1 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách hàng phàn nàn bị trừ tiền 2 lần, mỗi lần 450.000đ, cho gói đăng ký tháng và yêu cầu hoàn tiền ngay.

Options:
A) Lỗi kỹ thuật
B) Thanh toán & hoàn tiền
C) Góp ý tính năng
D) Hủy tài khoản
```

**Đáp án đúng: B** — Thanh toán & hoàn tiền

### Test 2 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách báo app bị văng ra mỗi lần bấm vào mục "Lịch sử đơn hàng", đã thử gỡ và cài lại 3 lần vẫn bị.

Options:
A) Lỗi kỹ thuật
B) Thanh toán & hoàn tiền
C) Góp ý tính năng
D) Hủy tài khoản
```

**Đáp án đúng: A** — Lỗi kỹ thuật

### Test 3 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách nhắn: "Tôi không dùng dịch vụ nữa, hãy xóa tài khoản và toàn bộ dữ liệu cá nhân của tôi."

Options:
A) Lỗi kỹ thuật
B) Thanh toán & hoàn tiền
C) Góp ý tính năng
D) Hủy tài khoản
```

**Đáp án đúng: D** — Hủy tài khoản

### Test 4 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách nhắn: "App dùng ổn, nhưng nếu có chế độ nền tối và cho xuất báo cáo ra Excel thì tuyệt hơn."

Options:
A) Lỗi kỹ thuật
B) Thanh toán & hoàn tiền
C) Góp ý tính năng
D) Hủy tài khoản
```

**Đáp án đúng: C** — Góp ý tính năng

---

## Lĩnh vực 2: Tài chính & đầu tư

### Test 5 — Bẫy (kỷ luật vs cảm tính)

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Nhà đầu tư mua cổ phiếu giá 70.000đ, kế hoạch giao dịch đặt stoploss -8% (tức 64.400đ). Giá hiện tại 63.500đ, thanh khoản bình thường, không có tin tức bất thường. Kế hoạch yêu cầu tuân thủ kỷ luật stoploss.

Options:
A) Mua thêm để trung bình giá
B) Giữ lại, chờ giá hồi phục
C) Bán cắt lỗ theo kế hoạch
D) Bán hết cổ phiếu khác để mua dồn vào mã này
```

**Đáp án đúng: C** — Bán cắt lỗ theo kế hoạch (giá 63.500đ đã thủng mốc 64.400đ)

### Test 6 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Báo cáo tài chính ngân hàng X quý này: doanh thu tăng 12% nhưng lợi nhuận sau thuế giảm 30% do chi phí trích lập dự phòng nợ xấu tăng mạnh. Tín hiệu chính cần cảnh báo là gì?

Options:
A) Tăng trưởng tín dụng mạnh
B) Hiệu quả quản lý chi phí cải thiện
C) Ngân hàng vừa tăng vốn điều lệ
D) Chất lượng tài sản suy giảm
```

**Đáp án đúng: D** — Chất lượng tài sản suy giảm (dự phòng nợ xấu tăng mạnh)

### Test 7 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Cổ phiếu Y có P/E = 8, trung bình ngành P/E = 15, ROE = 22%, nợ vay/vốn chủ sở hữu = 0,3, lợi nhuận tăng trưởng đều 3 năm liên tiếp. Đánh giá định giá tương đối so với ngành?

Options:
A) Định giá thấp tương đối so với ngành, nền tảng tốt
B) Định giá cao so với ngành
C) Công ty đang thua lỗ
D) Không đủ dữ liệu để đánh giá
```

**Đáp án đúng: A** — Định giá thấp tương đối so với ngành, nền tảng tốt (P/E 8 < 15, ROE cao, nợ thấp, tăng trưởng đều)

### Test 8 — Bẫy (rủi ro margin)

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Nhà đầu tư dùng margin 80% tài khoản. VN-Index giảm 4% trong phiên, tỷ lệ ký quỹ đã sát ngưỡng call margin.

Options:
A) Vay thêm margin để mua bắt đáy
B) Nạp thêm tiền hoặc bán bớt để giảm dư nợ
C) Không làm gì, chờ thị trường tự hồi
D) Mua thêm phái sinh để bù lỗ
```

**Đáp án đúng: B** — Nạp thêm tiền hoặc bán bớt để giảm dư nợ

---

## Lĩnh vực 3: IT / DevOps

### Test 9 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Production API trả lỗi 500 cho 100% request, bắt đầu ngay sau lần deploy cách đây 10 phút. Phiên bản trước đó chạy ổn định.

Options:
A) Dành vài ngày điều tra log chi tiết rồi mới xử lý
B) Gửi email báo cáo cho cả team
C) Rollback về phiên bản trước ngay lập tức
D) Scale up thêm server
```

**Đáp án đúng: C** — Rollback về phiên bản trước ngay lập tức

### Test 10 — Bẫy (severity)

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Server staging dùng nội bộ cho dev có CPU 85% trong 5 phút. Không có người dùng thật nào bị ảnh hưởng. Chọn mức độ ưu tiên phù hợp.

Options:
A) P1 - Sự cố nghiêm trọng, gọi on-call ngay
B) P2 - Mức cao, xử lý trong 1 giờ
C) Tắt toàn bộ hệ thống để kiểm tra
D) P4 - Mức thấp, ghi nhận và theo dõi
```

**Đáp án đúng: D** — P4 - Mức thấp, ghi nhận và theo dõi

### Test 11 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Phát hiện AWS access key bị commit nhầm lên GitHub public repo cách đây 2 giờ.

Options:
A) Revoke/rotate key ngay và kiểm tra log truy cập
B) Chỉ xóa commit chứa key
C) Đổi tên repo sang private
D) Chờ xem có bị lạm dụng không rồi mới xử lý
```

**Đáp án đúng: A** — Revoke/rotate key ngay và kiểm tra log truy cập (key đã lộ thì phải coi là compromised)

### Test 12 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Người dùng đăng ký nhưng không nhận được email OTP, email cũng không nằm trong spam. Log hệ thống ghi SMTP trả lỗi 550.

Options:
A) Yêu cầu hoàn tiền
B) Lỗi cấu hình/hạ tầng gửi email
C) Đề xuất tính năng mới
D) Người dùng nhập sai mật khẩu
```

**Đáp án đúng: B** — Lỗi cấu hình/hạ tầng gửi email

---

## Lĩnh vực 4: Y tế (triage)

### Test 13 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Bệnh nhân nam 58 tuổi đau thắt ngực lan ra cánh tay trái, vã mồ hôi, khó thở, triệu chứng bắt đầu cách đây 20 phút.

Options:
A) Hẹn khám ngoại trú tuần sau
B) Uống thuốc giảm đau và nghỉ ngơi
C) Tư vấn điều chỉnh chế độ ăn
D) Cấp cứu ngay, gọi 115
```

**Đáp án đúng: D** — Cấp cứu ngay, gọi 115 (nghi nhồi máu cơ tim)

### Test 14 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Người dùng sốt nhẹ 37,8°C, ngạt mũi, đau họng 2 ngày, vẫn ăn uống và sinh hoạt bình thường, không khó thở.

Options:
A) Chăm sóc tại nhà: nghỉ ngơi, bù nước, theo dõi; đi khám nếu nặng hơn
B) Gọi cấp cứu
C) Nhập viện điều trị nội trú
D) Chỉ định phẫu thuật
```

**Đáp án đúng: A** — Chăm sóc tại nhà, theo dõi

### Test 15 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Bệnh nhân tiểu đường type 2, đang dùng metformin, đường huyết đói 11,5 mmol/L trong 3 ngày liên tiếp.

Options:
A) Giữ nguyên, không cần làm gì
B) Tự tăng gấp đôi liều thuốc
C) Tái khám để bác sĩ đánh giá và điều chỉnh phác đồ
D) Ngưng thuốc hoàn toàn
```

**Đáp án đúng: C** — Tái khám để bác sĩ đánh giá và điều chỉnh phác đồ

### Test 16 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách hàng hỏi lịch tiêm vaccine cúm hằng năm cho người 65 tuổi.

Options:
A) Tư vấn phòng bệnh / tiêm chủng
B) Cấp cứu
C) Hỏi giá viện phí
D) Khiếu nại dịch vụ
```

**Đáp án đúng: A** — Tư vấn phòng bệnh / tiêm chủng

---

## Lĩnh vực 5: Logistics & Thương mại điện tử

### Test 17 — Bẫy (nhiều phương án nghe hợp lý)

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Đơn hàng hiển thị "Giao thành công" nhưng khách khẳng định chưa nhận được hàng, shipper không liên lạc được.

Options:
A) Hoàn tiền ngay, không cần điều tra
B) Từ chối vì hệ thống ghi đã giao
C) Mở khiếu nại với đơn vị vận chuyển, xác minh bằng chứng giao hàng
D) Tặng voucher rồi đóng ticket
```

**Đáp án đúng: C** — Mở khiếu nại với đơn vị vận chuyển, xác minh bằng chứng giao hàng

### Test 18 — Bẫy (nhiều phương án nghe hợp lý)

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách đặt 500 áo, kho hiện chỉ còn 320 chiếc, 180 chiếc còn lại dự kiến về sau 10 ngày.

Options:
A) Hủy toàn bộ đơn
B) Cam kết giao đủ 500 như đã đặt
C) Giao 320 mà không thông báo gì thêm
D) Giao 320 trước, thông báo rõ và hỏi khách về 180 còn lại
```

**Đáp án đúng: D** — Giao 320 trước, thông báo rõ và hỏi khách về 180 còn lại

### Test 19 — Trung bình

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Hàng dễ vỡ, tuyến Hà Nội → TP.HCM, còn 2 ngày nữa là Tết Nguyên Đán. Khách cần nhận hàng trước Tết.

Options:
A) Vận chuyển đường bộ thường (4-5 ngày)
B) Vận chuyển hàng không kèm đóng gói chống sốc
C) Gửi tàu hỏa, không bảo hiểm
D) Gửi sau Tết
```

**Đáp án đúng: B** — Vận chuyển hàng không kèm đóng gói chống sốc (đáp ứng cả thời hạn lẫn hàng dễ vỡ)

### Test 20 — Dễ

```
System: Bạn là một mô hình ra quyết định. Hãy chọn một chữ cái của phương án tốt nhất (kèm nội dung của phương án đó).

Context/State: Khách muốn đổi size áo sau 5 ngày. Chính sách đổi trả là 7 ngày, áo còn nguyên tem mác, chưa giặt.

Options:
A) Từ chối vì quá hạn
B) Chấp nhận đổi size
C) Chỉ hoàn tiền, không đổi
D) Chuyển lên CSKH cấp cao
```

**Đáp án đúng: B** — Chấp nhận đổi size (5 ngày < 7 ngày, đủ điều kiện)

---

## Bảng đáp án tổng hợp

| Test | Lĩnh vực       | Đáp án | Test | Lĩnh vực  | Đáp án |
| ---- | ---------------- | --------- | ---- | ----------- | --------- |
| 1    | Customer Support | B         | 11   | IT / DevOps | A         |
| 2    | Customer Support | A         | 12   | IT / DevOps | B         |
| 3    | Customer Support | D         | 13   | Y tế       | D         |
| 4    | Customer Support | C         | 14   | Y tế       | A         |
| 5    | Tài chính      | C         | 15   | Y tế       | C         |
| 6    | Tài chính      | D         | 16   | Y tế       | A         |
| 7    | Tài chính      | A         | 17   | Logistics   | C         |
| 8    | Tài chính      | B         | 18   | Logistics   | D         |
| 9    | IT / DevOps      | C         | 19   | Logistics   | B         |
| 10   | IT / DevOps      | D         | 20   | Logistics   | B         |

## Bảng chấm điểm

| Test                | Jev | Tev1 | Test | Jev | Tev1 |
| ------------------- | --- | ---- | ---- | --- | ---- |
| 1                   |     |      | 11   |     |      |
| 2                   |     |      | 12   |     |      |
| 3                   |     |      | 13   |     |      |
| 4                   |     |      | 14   |     |      |
| 5                   |     |      | 15   |     |      |
| 6                   |     |      | 16   |     |      |
| 7                   |     |      | 17   |     |      |
| 8                   |     |      | 18   |     |      |
| 9                   |     |      | 19   |     |      |
| 10                  |     |      | 20   |     |      |
| **Tổng /20** |     |      |      |     |      |
