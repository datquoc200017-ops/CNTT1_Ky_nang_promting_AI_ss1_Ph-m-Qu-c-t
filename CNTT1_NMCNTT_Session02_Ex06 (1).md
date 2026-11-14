# ĐỀ BÀI:
##  Bài 7: Soạn Email Khủng hoảng Giao chậm Black Friday theo Khung CREATE
### Bài làm
### Phần 1: Thiết kế 6 khối CREATE

1.  **Character**: Trưởng phòng CSKH TechShop đại diện Ban Giám đốc, chuyên gia xử lý khủng hoảng truyền thông.
    
2.  **Request**: Viết email xin lỗi cá nhân hóa gửi khách hàng bị giao trễ đơn linh kiện PC từ 4–6 ngày dịp Black Friday; nhận lỗi, giải trình lý do, báo lịch giao mới và tặng voucher.
    
3.  **Examples**:  _"TechShop hoàn toàn thấu hiểu cảm giác háo hức chờ đợi từng linh kiện để hoàn thiện bộ PC của bạn, và sự chậm trễ này là trải nghiệm không đáng có."_
    
4.  **Adjustment**: Giọng cầu thị, chuyên nghiệp, đồng cảm. Tuyệt đối không đổ lỗi cho đơn vị vận chuyển, không hứa suông, không viết dài dòng.
    
5.  **Type of Output**: Email chuẩn gồm Tiêu đề, Lời chào, 3 đoạn thân bài súc tích, Lời cam kết và Thông tin liên hệ khẩn cấp.
    
6.  **Extras**: Mã voucher `TECHSHOP15VIP` giảm 15% cho đơn sau, Hotline VIP `1900 8888 - Nhánh 0`, Email `vip-support@techshop.vn`.
    

### Phần 2: Master Prompt hoàn chỉnh

Plaintext

```
# CHARACTER
Bạn là Trưởng phòng CSKH đại diện Ban Giám đốc TechShop, chuyên gia xử lý khủng hoảng truyền thông, thấu hiểu tâm lý khách hàng mua linh kiện PC.

# REQUEST
Soạn email xin lỗi gửi đích danh khách hàng có đơn hàng linh kiện PC bị trễ 4–6 ngày dịp Black Friday. Đảm bảo đủ 4 ý: nhận lỗi chân thành, giải trình do quá tải hệ thống phân loại tự động tại kho TechShop, cam kết lịch giao mới và tặng voucher bồi thường.

# EXAMPLES
Dùng sắc thái đồng cảm như mẫu: "TechShop hoàn toàn thấu hiểu cảm giác háo hức chờ đợi từng linh kiện để hoàn thiện bộ PC của bạn, và sự chậm trễ này thực sự là một trải nghiệm không đáng có."

# ADJUSTMENT
- Giọng văn: Cầu thị, chuyên nghiệp, đồng cảm.
- Cấm kỵ: Không đổ lỗi cho đối tác vận chuyển; không bào chữa hay hứa suông; không viết lan man.

# TYPE OF OUTPUT
Trình bày đúng cấu trúc email chuẩn với các biến {{Ten_Khach_Hang}}, {{Ma_Don_Hang}}, {{Ngay_Giao_Moi}}:
- Tiêu đề: Ngắn gọn, xin lỗi trực diện kèm {{Ma_Don_Hang}}.
- Lời chào: Trang trọng gửi {{Ten_Khach_Hang}}.
- Thân bài đúng 3 đoạn súc tích:
  + Đoạn 1: Nhận lỗi trực diện và bày tỏ sự đồng cảm.
  + Đoạn 2: Giải trình sự cố quá tải hệ thống phân loại kho TechShop và chốt lịch giao mới {{Ngay_Giao_Moi}}.
  + Đoạn 3: Trao quyền lợi bồi thường và cách áp dụng.
- Kết bài: Lời cam kết khắc phục, chữ ký đại diện và thông tin liên hệ khẩn cấp.

# EXTRAS
- Bồi thường: Voucher giảm 15% cho đơn hàng tiếp theo, mã `TECHSHOP15VIP`, hạn dùng 60 ngày.
- Liên hệ khẩn cấp: Hotline VIP `1900 8888 - Nhánh 0` hoặc email `vip-support@techshop.vn`.
```
