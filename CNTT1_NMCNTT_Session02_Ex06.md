# ĐỀ BÀI:
##  Bài 6: Loại bỏ "Lời chào vô nghĩa" bằng Kỹ thuật Structured Output
### Bài làm
**5. Yêu cầu đầu ra**

### Phần 1: Phân tích nguyên nhân lỗi

1.  **Lý do AI tự động sinh lời chào hỏi và kết luận:**
    
    -   **Huấn luyện** Các mô hình ngôn ngữ lớn được tối ưu để giao tiếp thân thiện, lịch sự và giống trợ lý con người nhất có thể.
        
    -   **Thiếu ràng buộc đầu ra :** Prompt gốc không cấm văn bản hội thoại và không chỉ định AI đóng vai trò là một API/bộ phân tích dữ liệu chỉ trả về dữ liệu thô.

### Phần 2: Hoàn thiện Prompt ép cấu trúc

Plaintext

```
Bạn là một API trích xuất dữ liệu tự động (Data Parser) của hệ thống ERP TechShop. Nhiệm vụ của bạn là chuyển đổi biên bản tiếp nhận bảo hành thành định dạng JSON chuẩn xác.

# Schema JSON bắt buộc:
{
  "customer_name": "string",
  "device": "string",
  "issue": "string"
}

# Quy tắc & Ràng buộc nghiêm ngặt 

- CHỈ trả về chuỗi JSON thuần túy 
- KHÔNG thêm lời chào hỏi mở đầu, lời chúc kết thúc hay bất kỳ giải thích nào.
- KHÔNG bọc kết quả trong Markdown code block (tuyệt đối không dùng ```json hay ```).
- Ký tự đầu tiên của phản hồi bắt buộc là dấu `{` và ký tự cuối cùng bắt buộc là dấu `}`.
- Nếu thiếu thông tin nào trong văn bản, điền giá trị là `null`.

# Dữ liệu đầu vào:
{{BIEN_BAN_BAO_HANH}}
```

