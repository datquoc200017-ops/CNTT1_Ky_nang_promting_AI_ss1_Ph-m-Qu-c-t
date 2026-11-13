# ĐỀ BÀI:
##  Bài 6: Phân tích cơ chế "Tràn cốc ngữ cảnh" (Truncation) trong luồng tư vấn CSKH
### Bài làm
**4. Yêu cầu đầu ra**

- **Phần 1: Giải thích hình tượng Chiếc cốc nước**

Dùng hình ảnh ẩn dụ "Chiếc cốc nước" giải thích cho nhân viên lý do AI quên thông tin ở Lượt 1.
  
- Hãy tưởng tượng rằng Context Window như một chiếc cốc thủy tinh có có dung tích cố định 32000 ml tương đương 32000 token ở lượt 1 Trần Văn B đơn #MTX-9988 đổ vào cốc và còn trống bộ nhớ khoảng 95% và sau 40 lượt chat đổ vào cốc bao nhiêu dữ liệu rồi đã tích lũy khoảng 32000 token và đến lượt 42 với một câu hỏi dĩ nhiễu sẽ bị tràn vì vốn dĩ 32000 token là đầy cốc rồi khi bổ sung thêm dữ liệu, dữ liệu cũ sẽ tràn và thay cho dữ liệu mới vào.

- **Phần 2: Phương án quản lý RAM bộ nhớ**

Đề xuất 2 phương án (thao tác người dùng & thiết kế hệ thống) để luồng tư vấn không bị tràn cốc.

- Tóm tắt phiên chat mới: khi nhận thấy cuộc hội thoại đã kéo dài 15-20 lượt  chuyển sang chủ đề mới  và yêu cầu AI tóm tắt đơn hàng, khách hàng bằng các gạch đầu dòng ngắn gọn, sau đó mở phiên chat mới và dán vào tiếp tục hội thoại  từ đó giải phóng được bộ nhớ.
-  Không bắt AI nhớ thông tin đơn hàng bằng bộ nhớ RAM hội thoại. Thay vào đó lưu hồ sơ khách hàng và trạng thái đơn `#MTX-9988` vào Database riêng  khi khách hỏi về hoàn tiền ở Lượt 42 hệ thống tự động truy xuất dữ liệu từ Database và nạp trực tiếp vào ngữ cảnh của lượt trả lời đó.



