# ĐỀ BÀI:
## Bài 1: Hiểu đúng bản chất "Máy dự đoán từ tiếp theo" (Next Token Prediction) của LLM
### Bài làm
**4. Yêu cầu đầu ra**

- **Phần 1 (Bóc tách nhận thức sai):** Dựa vào Mục 2.1 Lesson 01, hãy chỉ ra 2 điểm sai lầm trong báo cáo của Nam. Trích dẫn thuật ngữ "Next Token Prediction" và "Pre-training" từ bài đọc để giải thích tại sao LLM lại tính sai phép cộng trên.
- Điểm sai thứ 1 là: Nam cho rằng AI bị hỏng bị lỗi tính toán là hoàn toàn sai, trên thực tế hệ thống hoạn động hoàn toàn bình thường, việc ra sai số là đặc tính tự nhiên của mô hình AI thuần túy.
- Điểm sai thử 2 là: Nam đang bị lầm tưởng rằng ngôn ngữ lớn (LLM) với bộ xử lí của máy tính có khả năng thực hiện phép toán số học, khi trả AI có thể dùng cơ chế Next token predition để ghép các con số có xác suất hợp lý về mặt chữ nên dễ sai lệch.

- **Phần 2 (Sửa lỗi & Prompting):** Đề xuất câu lệnh (Prompt) chuẩn giúp ChatGPT kích hoạt công cụ bổ trợ (ví dụ: Code Interpreter / Python) hoặc yêu cầu AI suy luận để cho ra kết quả số học chính xác 100%.
- Prompt chuẩn giúp ChatGPT là: bạn hãy sử dùng ngôn ngữ lập trình Python để tính bài toán sau 15480 + 28750 không được tự ước tính xác suất kết quả chỉ trả về khi mã được thực thi.
