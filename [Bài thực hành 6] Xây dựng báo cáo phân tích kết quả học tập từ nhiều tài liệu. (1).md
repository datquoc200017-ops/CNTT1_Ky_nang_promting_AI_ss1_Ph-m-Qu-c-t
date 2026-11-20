# \[Bài thực hành 6\] Xây dựng báo cáo phân tích kết quả học tập từ nhiều tài liệu\.

### 4\. Yêu cầu đầu ra



Sinh viên phải nộp:



**Các Prompt dùng để đọc và xử lý 4 file\.**

1. bạn là trợ lý đào tạo tại trung tâm CNTT, bạn tổng hợp kết quả học tập của 1 lớp 30 sinh viên khi hết học phần Java cơ bản nhiệm vụ đầu tiên đọc và xử lý 4file tôi gửi và đưa ra kết quả chuẩn nhất không dự đoán chỉ tìm dữ liệu ở đúng file đó thôi\.

    

**Prompt đối chiếu dữ liệu\.**

tiếp theo bạn hãy trích xuất dữ liệu thành bảng có cấu trúc và Đối chiếu dữ liệu\.



**Bảng kết quả tổng hợp 30 sinh viên gồm: Mã SV, Họ tên, Chuyên cần, Bài tập, Giữa kỳ, Cuối kỳ, Tổng kết, Kết quả**





- Báo cáo thống kê tỷ lệ đạt và chưa đạt\.

    

- Danh sách các trường hợp bất thường\.

    #### A\. Bất thường về dữ liệu \& kỹ thuật nhập liệu

    1. **Dữ liệu khuyết \(****`Null`****\) \& bỏ học/bỏ thi giữa chừng:**

        - **JV020 – Trịnh Văn Phong \(CNTT\-K21C\):** Vắng 5 buổi \(cao nhất lớp\), điểm bài tập giảm dần về 0 \(`BT1 = 3.0`, `BT2 = 4.0`, `BT3 = 0.0`\), khuyết hoàn toàn điểm giữa kỳ \(`Diem_Ly_Thuyet = Null`, `Diem_Thuc_Hanh = Null`\)\(\) và điểm cuối kỳ bằng 0 \(`Diem_Do_An = 0.0`, `Diem_Van_Dap = 0.0`\) với nhận xét giảng viên: *"Bỏ thi cuối kỳ, không nộp bài đồ án"*\.   

    2. **Trùng lặp bản ghi trong tệp điểm quá trình \(****`Diem_qua_trinh.xlsx`****\):**

        - **JV004 – Phạm Minh Dũng \(CNTT\-K21A\):** Xuất hiện 2 dòng giống hệt nhau \(dòng 4 và dòng 5 trong file Excel\)\.

        - **JV019 – Đinh Thị Nhung \(CNTT\-K21C\):** Xuất hiện 2 dòng giống hệt nhau \(dòng 20 và dòng 21 trong file Excel\)\.

    3. **Sai chuẩn định dạng mã sinh viên \(****`Ket_qua_giua_ky.txt`****\):**

        - **JV008 – Bùi Quang Hải:** Mã thi ghi chữ thường `jv008`\(\)\.   

        - **JV022 – Lương Minh Quân:** Mã thi ghi chữ thường `jv022`\(\)\.   

    4. **Trùng họ tên đầy đủ giữa nhiều sinh viên \(rủi ro nhầm lẫn khi ghép bảng bằng tên\):**

        - **Nguyễn Văn An \(3 sinh viên\):** `JV001` \(CNTT\-K21A\), `JV015` \(CNTT\-K21B\), `JV030` \(CNTT\-K21D\)\.

        - **Trần Thị Lan \(2 sinh viên\):** `JV012` \(CNTT\-K21B\), `JV023` \(CNTT\-K21C\)\.

    #### B\. Bất thường về kết quả học tập \& chuyên cần

    1. **Nhóm vắng nhiều buổi \(**$\ge 3$** buổi\) và điểm số dưới ngưỡng an toàn:**

        - **JV010 – Dương Văn Hùng \(CNTT\-K21B\):** Vắng **4 buổi**, tất cả các đầu điểm đều dưới 5,0 \(`BT1=4.0, BT2=5.0, BT3=4.5, GK_LT=4.5, GK_TH=4.0, Đồ án=4.0, Vấn đáp=4.5`\(\)\)\. Nhận xét giảng viên: *"Hổng kiến thức cơ bản về vòng lặp và mảng, cần học lại\."*   

        - **JV006 – Vũ Đức Giang \(CNTT\-K21A\):** Vắng **3 buổi**, điểm dao động từ `5.0` đến `6.0`\(\)\. Nhận xét giảng viên: *"Nghỉ nhiều ảnh hưởng đến tiến độ, cần cố gắng hơn\."*   

        - **JV026 – Tạ Đức Thắng \(CNTT\-K21D\):** Vắng **3 buổi**, điểm giữa kỳ thực hành và cuối kỳ đồ án đều dưới trung bình \(`4.5`\)\(\)\. Nhận xét giảng viên: *"Chưa đạt yêu cầu phần quản lý danh sách đối tượng\."*   

    

- Báo cáo nhận xét tình hình học tập dài khoảng 500 từ\.

Qua quá trình rà soát, đối chiếu và tổng hợp dữ liệu từ 4 nguồn hồ sơ đào tạo gồm danh sách lớp, bảng điểm quá trình, kết quả thi giữa kỳ \(`15/10/2026`\(\)\) và báo cáo đánh giá cuối kỳ của giảng viên đối với **30 sinh viên** \(thuộc 4 lớp hành chính `CNTT-K21A`, `CNTT-K21B`, `CNTT-K21C`, `CNTT-K21D`\), tình hình học tập của lớp được ghi nhận cụ thể như sau:   

Ket\_qua\_giua\_ky\.txt

1. **Đánh giá chung về kết quả và mức độ hoàn thành học phần** Nhìn chung, mặt bằng chất lượng học tập của lớp ở mức khá và duy trì sự ổn định xuyên suốt ba giai đoạn đánh giá\. Xét trên 29 sinh viên có đầy đủ dữ liệu điểm số, điểm trung bình các thành phần đều đạt mức **7,50 điểm** \(trung bình bài tập đạt 7,49; giữa kỳ đạt 7,50; cuối kỳ đạt 7,50\)\. Áp dụng công thức trọng số hiện hành nhưng chưa cộng 10% chuyên cần do chưa có quy định quy đổi từ số buổi vắng, có **25/30 sinh viên \(83,33%\)** đã đạt ngưỡng từ **5,26 đến 8,65 điểm** ở riêng phần 90% tổng điểm, đảm bảo chắc chắn đạt học phần\. Nổi bật trong số này là nhóm sinh viên xuất sắc đạt từ 9,0 điểm trở lên ở cả ba giai đoạn quá trình, giữa kỳ và cuối kỳ gồm **JV003 \(Lê Hoàng Cường\)**, **JV012 \(Trần Thị Lan \- CNTT\-K21B\)**, **JV018 \(Phan Quốc Nghĩa\)** và **JV027 \(Đoàn Thị Thảo\)**\. Theo nhận xét của giảng viên, nhóm sinh viên khá giỏi nắm vững kiến thức Java Core, Collection, xử lý ngoại lệ, File I/O và biết áp dụng tư duy hướng đối tượng \(OOP\) cũng như mô hình MVC vào đồ án thực tế\.

2. **Mối tương quan giữa chuyên cần và kết quả học tập** Dữ liệu cho thấy sự gắn kết chặt chẽ giữa thái độ chuyên cần và kết quả tiếp thu kiến thức\. Toàn bộ **13 sinh viên đi học đầy đủ \(0 buổi vắng\)** đều đạt điểm trung bình các thành phần từ 8,00 điểm trở lên và hoàn thành tốt đồ án cuối kỳ\. Ngược lại, tình trạng nghỉ học từ 3 buổi trở lên kéo theo sự sa sút rõ rệt về điểm số và kỹ năng thực hành:

- **JV010 \(Dương Văn Hùng \- CNTT\-K21B\):** Vắng 4 buổi, toàn bộ các đầu điểm đều dưới trung bình \(từ 4,0 đến 5,0\)\(\), hổng kiến thức cơ bản về vòng lặp và mảng\. Với tổng 90% đạt 3,88 điểm, trường hợp này chắc chắn chưa đạt học phần\.   

- Ket\_qua\_giua\_ky\.txt

- 

- **JV006 \(Vũ Đức Giang \- CNTT\-K21A\)** và **JV026 \(Tạ Đức Thắng \- CNTT\-K21D\):** Cùng vắng 3 buổi, điểm trung bình các phần chỉ dao động quanh mức 4,75 – 5,50\(\), gặp khó khăn ở phần quản lý danh sách đối tượng\. Kết quả cuối cùng của hai sinh viên này cùng với **JV030 \(Nguyễn Văn An \- CNTT\-K21D, vắng 2 buổi, tổng 90% đạt 4,99 điểm\)** đang phụ thuộc trực tiếp vào quy tắc quy đổi điểm chuyên cần \(10%\) của trung tâm\.   

- Ket\_qua\_giua\_ky\.txt

- 

3. **Các trường hợp đặc biệt và khuyến nghị quản lý đào tạo** Trường hợp nghiêm trọng nhất lớp là **JV020 \(Trịnh Văn Phong \- CNTT\-K21C\)** với 5 buổi vắng, điểm bài tập giảm dần về 0, khuyết dữ liệu thi giữa kỳ \(`Null`\)\(\) và bỏ thi cuối kỳ, không nộp đồ án\. Bên cạnh đó, nhóm sinh viên trung bình \(điểm quanh mức 5,5 – 6,5\) vẫn còn hạn chế về kỹ năng debug, xử lý ngoại lệ nhập liệu, tính kế thừa và đa hình trong Java\.   

Ket\_qua\_giua\_ky\.txt

Để hoàn tất chốt điểm chính thức và nâng cao chất lượng đào tạo, bộ phận giáo vụ cần bổ sung quy định quy đổi cột `So_Buoi_Vang` sang điểm chuyên cần \(10%\), xác nhận lại trạng thái học vụ của **JV020**, đồng thời chuẩn hóa quy trình nhập liệu \(tránh trùng lặp bản ghi như ở `JV004`, `JV019` hay sai định dạng chữ thường `jv008`, `jv022`\(\), và luôn dùng `Ma_SV` làm khóa định danh thay cho họ tên do lớp có 5 sinh viên trùng tên\)\.   

Ket\_qua\_giua\_ky\.txt



