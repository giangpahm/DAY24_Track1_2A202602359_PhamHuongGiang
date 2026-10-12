# Lab 24 — CS9 Workshop: AI Economics / ROI / Pricing (bài nhóm)

Bài nhóm của buổi Day 24, Track 1 — AI Product Management. Câu hỏi cả buổi: **sản phẩm AI này có lãi không, bán giá bao nhiêu và có đáng bỏ tiền làm không?**

## Các file trong thư mục

|File|Là gì|
|-|-|
|`DAY24\_Track1\_2A202602359\_PhamHuongGiang.xlsx`|**Bài cá nhân để nộp** trên VLearn|
|`CS9\_Workshop\_PhamHuongGiang\_2A202602359.xlsx`|Bài cá nhân làm trên dự án riêng (AI dựng concept nội thất), giữ nguyên, không nộp cho bài nhóm|
|`CS9\_Workshop\_Mau.xlsx`|Bản mẫu của lớp để xem cách điền, không nộp|

## Nhóm chọn đề nào

Các thành viên ngồi chung bàn nhưng không có dự án chung. Theo runbook, trường hợp này phải chọn 1 trong 3 đề bài giả định (`CS9\_DeBai\_GiaDinh.pdf`) và dùng xuyên suốt buổi. Nhóm chọn:

> \*\*Đề bài 1 — SổSạch:\*\* trợ lý AI đọc hoá đơn đầu vào cho văn phòng kế toán dịch vụ.
> \*\*1 việc\*\* = 1 hoá đơn đầu vào được đọc, đối chiếu mã số thuế và nhập vào phần mềm kế toán.
> \*\*Khách trả tiền:\*\* văn phòng kế toán dịch vụ. \*\*Điểm cần chú ý:\*\* chi phí người kiểm tra lớn; văn phòng lớn thấy đắt.

Mọi số ở sheet 1–3 lấy đúng từ đề. Cột "Nguồn / lý do" ghi rõ "Đề bài 1, Trang X". Giá token và tỷ giá là dữ liệu bài tập (trang 9 của file), không phải báo giá nhóm tự kiểm chứng.

## Đã làm gì

Bài nhóm được dựng từ file cá nhân. Phần A giữ nguyên, các sheet sản phẩm thay hoàn toàn bằng số của Đề 1.

|Sheet|Nội dung|
|-|-|
|`0\_Đầu vào`|Đánh dấu 6 đầu vào là "Chưa" (nhóm dùng đề giả định, không có số đo thật từ buổi trước) và ghi nguồn thay thế|
|`A\_Tài chính căn bản`|Ba báo cáo tài chính (Trợ Lý Xanh, chung cho mọi nhóm): kết quả kinh doanh, cân đối kế toán, lưu chuyển tiền tệ, câu hỏi 1–4, bài mua hay thuê máy chủ. Mọi ô kiểm tra "Đạt"|
|`1\_Chi phí mỗi việc`|Claude Haiku 4.5, 2 lần gọi, 2.500 / 400 token, gọi lại 8%, 20% hoá đơn cần kế toán viên kiểm tra 1,5 phút|
|`2\_Định giá`|Gói kết hợp 1.990.000 đ/tháng gồm 1.000 hoá đơn, vượt 2.200 đ/hoá đơn; 70% văn phòng nhỏ (800 hoá đơn), 30% văn phòng lớn (4.000 hoá đơn); lương người được thay 8 triệu; không chia đối tác|
|`3\_Giả định`|Cột Cơ sở theo đề (12 khách mới, tăng 5%/tháng, rời bỏ 3%, CAC 9 triệu, cố định 200 triệu, xây dựng 900 triệu, tiền mặt 2,5 tỷ). Cột Lạc quan / Xấu giữ mặc định của file|
|`4`, `5`|Tự tính: chỉ số mỗi khách, dòng tiền 24 tháng, độ nhạy (B54 = 20%), mức cảnh báo tự tính|
|`6\_Hiệu quả nội bộ`|Không áp dụng (bán ra ngoài)|
|`7\_Quyết định`|5 câu quyết định, có trả lời 3 câu hỏi riêng của đề|

Định dạng: các ô chữ dài được bật xuống dòng, chiều cao hàng căn theo nội dung, các bảng có viền đồng nhất. Các sheet vẫn khoá như bản gốc.

## Kết quả chính

|Chỉ số|Cơ sở|Xấu|
|-|-|-|
|Chi phí mỗi hoá đơn|704 đ (gọi AI 254 · người kiểm tra 250 · khác 200)||
|Biên lợi nhuận gộp|68,8%|53,2%|
|LTV ÷ CAC|10,1|2,6|
|Hoàn vốn chi phí có khách|3,3 tháng|8,0 tháng|
|NPV 24 tháng|+935 triệu (IRR 47%/năm)|−5,0 tỷ|
|Tiền mặt thấp nhất|173 triệu|−3,09 tỷ|
|Hoàn vốn dự án / hết tiền|hoàn vốn tháng 21|**hết tiền tháng 7**|

* **Biến nguy hiểm nhất:** doanh thu bình quân / khách. Giảm 20% thì NPV còn −1.965 triệu. Chỉ cần giảm 6,5% (dưới 3,71 triệu) là về hoà vốn.
* **Phụ thuộc văn phòng lớn:** nhóm này mang về 65% doanh thu và trả 8,59 triệu/tháng, bằng 107% lương một nhân viên nhập liệu (vượt mốc 70%). Nếu họ bỏ đi và được thay bằng văn phòng nhỏ, NPV còn −3,83 tỷ.
* **Gói không giới hạn** làm tiền AI ÷ doanh thu của văn phòng lớn lên 1,42 (nguy), nên không dùng.

## Quyết định: THỬ NGHIỆM NHỎ

Kịch bản cơ sở có lãi nhưng kịch bản xấu hết tiền ở tháng 7, nên không chọn "Làm". Từng khách vẫn có lãi (LTV ÷ CAC 10,1), nên cũng không chọn "Dừng".

* Thử 3 tháng với 12 văn phòng (giữ tỷ lệ 70% nhỏ / 30% lớn).
* Mở rộng khi doanh thu bình quân ≥ 3,71 triệu và rời bỏ ≤ 3%/tháng.
* **Luật xử lý:** NẾU doanh thu bình quân < 3.714.000 đ hoặc rời bỏ > 4,8%/tháng TRONG 2 tháng liên tiếp trên ít nhất 12 văn phòng THÌ dừng ký văn phòng mới, cắt đội 6 → 4 người, phỏng vấn lại các văn phòng lớn trong 2 tuần. KHÔNG THÌ: cấm hạ phí vượt dưới giá sàn 2.113 đ/hoá đơn và cấm bán gói không giới hạn.
* Đã chạy thử trên file: chỉ cắt đội còn 4 người (chi phí cố định 140 triệu) thì kịch bản xấu vẫn hết tiền, chỉ lùi sang tháng 9. Vì vậy phải dừng cả chi phí bán hàng cho khách mới (\~81 triệu/tháng ở kịch bản xấu).

**Trả lời 3 câu hỏi riêng của đề**

1. Chi phí gọi AI (254 đ) và người kiểm tra (250 đ) gần bằng nhau. AI lớn hơn một chút, chỉ chiếm khoảng 36% chi phí mỗi hoá đơn.
2. Văn phòng lớn trả 107% lương một nhân viên nhập liệu nên có lý do bỏ đi hoặc ép giá. Cần phỏng vấn xem 4.000 hoá đơn/tháng đang tốn mấy nhân viên.
3. Kịch bản xấu hết tiền ở tháng 7, nên nhóm chọn Thử nghiệm nhỏ kèm kế hoạch cắt giảm ở trên.

## Trình bày (3 slide, tối đa 3 phút + 2 phút phản biện)

1. **Kết luận:** "Nhóm đề xuất Thử nghiệm nhỏ, với giá 1.990.000 đ/tháng gồm 1.000 hoá đơn, vượt 2.200 đ/hoá đơn, vì cơ sở có lãi (NPV +935 triệu) nhưng kịch bản xấu hết tiền ở tháng 7."
2. **Bằng chứng:** bảng Kết quả chính ở trên (sheet 1 dòng 24, sheet 4, sheet 5 dòng 44–48).
3. **Rủi ro:** biến nguy hiểm nhất, phụ thuộc văn phòng lớn, luật xử lý (sheet 5 dòng 66, 68, 72–77; sheet 7 câu 3–5).

## Còn cần nhóm làm

* \[ ] Cả nhóm soát lại sheet 7, nhất là ngưỡng rời bỏ 4,8% và quy mô thử 12 văn phòng (đây là lựa chọn, không phải số của đề)
* \[ ] Nộp `DAY24\_Track1\_2A202602359\_PhamHuongGiang.xlsx` trên VLearn trước 12:00 và mở lại tệp đã nộp để xác nhận đúng bản
* \[ ] Làm 3 slide và tập nói dưới 3 phút
* \[ ] Chuẩn bị 2 câu hỏi có con số để phản biện nhóm kế tiếp

