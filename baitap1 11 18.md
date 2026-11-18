# **Lập kế hoạch tài chính cá nhân bằng Chain-of-Thought**
## Bài làm
### **5. Yêu cầu xử lý dữ liệu**

Trình bày kết quả lập luận thành hai phần rõ rệt:
Phần prompt mà em trình bày là: 
- Vai trò : Bạn đóng vai là một chuyên gia hoạch định tài chính cá nhân và xử lý xuất sắc thu nhập biến động mỗi tháng và đang có một số khoản nợ cần thanh toán, chính xác tuyệt đối.
- Nhiệm vụ : Dự trên tài liệu tôi cấp dưới đây bạn hãy lập kế hoạch tài chính hàng tháng từ dữ liệu đầu vào gồm: Thu nhập, Chi phí cố định, Các khoản nợ, Mục tiêu tiết kiệm.
**Dữ liệu đầu vào** 
1. Tổng doanh thu tháng này trước thuế khoảng 15.000.000vnd (sau khi trừ thuế)
2. Thuế thu nhập cá nhân khoảng 1.000.000vnd 
3. Chi phí cố định 5.000.000vnd
4. Tổng khoản nợ cần đóng khoảng  100.000.000vnd
**Quy tắc xử lý**
Hãy suy nghĩ từng bước một và tính toán chi tiết trước khi đưa ra quyết định
Bắt buộc hiển thị đầy đủ phép tính cộng trừ nhân chia trung gian, không nhảy cóc ra kết quả.
Đảm bảo tổng tỷ lệ phần trăm phân bổ ngân sách phải bằng chính xác 100%.
Không dùng Pydantic hay code Python, thực hiện hoàn toàn bằng kỹ năng Prompting logic.
Hãy thực hiện tuần tự theo đúng 4 bước lập luận sau:
-   Bước 1: Tính toán tổng thu nhập khả dụng sau khi trừ thuế và chi phí cố định bắt buộc.
    
-   Bước 2: Phân bổ khoản tiền trả nợ tối thiểu.
    
-   Bước 3: Trích lập quỹ tiết kiệm theo tỷ lệ cam kết.
    
-   Bước 4: Chia phần còn lại cho chi tiêu linh hoạt theo quy tắc 50/30/20 cải tiến.
  **Định dạng đầu ra**
-   Phần 1: Nhật ký suy luận logic (Reasoning Steps) chỉ ra công thức tính toán và số liệu trung gian.
-   Phần 2: Bảng phân bổ ngân sách cuối cùng bằng Markdown Table với các cột: Hạng mục, Số tiền, Tỷ lệ %, Ghi chú.
- 
