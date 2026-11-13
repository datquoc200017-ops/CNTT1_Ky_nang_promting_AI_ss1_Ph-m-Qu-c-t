# ĐỀ BÀI:
## [BTTH] Cẩm nang sử dụng AI hiệu quả cho tân sinh viên
### Bài làm
**3. Yêu cầu đầu ra**

Nộp: (1) Sơ đồ các bước xâu chuỗi prompt

- Cách bước thực hiện sơ đồ các bức xâu chuỗi prompt là 
B1: Lên dàn ý, thiết lập vai trò.
B2: Viết phần 1 - bản chất LLM dựa vào dàn ý ở bước 1 xuất ra nội dung phần 1.
B3: Viết phần 2 - Chống ảo giác, Tiếp nối mạch văn Phần 1 đưa ra Nội dung phần 2.
B4: Viết Phần 3 - Khung CREATE và Tổng hợp, Hoàn thiện phần cuối + Gộp thành cuốn sách hoàn chỉnh. 	
	
(2) Nội dung các prompt thành phần.

- Prompt 1: Đàn anh IT. Task: Dàn ý cẩm nang học code với AI (600-800 từ) cho SV năm 1: 1.LLM đoán từ, 2.3 dấu hiệu ảo giác, 3.Khung CREATE. Output: Gạch đầu dòng ngắn, không diễn giải.

- Prompt 2 viết Phần 1 (~200 từ) theo dàn ý trên. Ý chính: LLM = máy đoán từ theo xác suất (như gợi ý phím), không suy nghĩ. Tone: Gần gũi, dễ hiểu.
- Prompt 3 viết Phần 2 (~250 từ), giữ tone. Nêu 3 dấu hiệu AI ảo giác khi code: 1.Bịa hàm 2.Sai logic trường hợp biên, 3.Đoán bừa nguyên nhân bug. Chốt: 1 câu khuyên bằng Docs.
- Prompt 4 Viết Phần 3 (~250 từ): Giải thích ngắn CREATE + 1 prompt mẫu gợi ý sửa bug C . Cuối cùng: Gộp Phần 1,2,3 thành cẩm nang hoàn chỉnh + thêm tiêu đề.


(3) Cuốn cẩm nang kết quả hoàn chỉnh xuất ra từ AI.
-   **C - Context (Ngữ cảnh):** Bối cảnh của bài toán, bạn là ai, đang làm gì.
    
-   **R - Role (Vai trò):** Giao cho AI một vai trò cụ thể (VD: giảng viên, senior developer).
    
-   **A - Acton:** Chỉ dẫn chi tiết việc cần làm (hoặc ví dụ mẫu).
    
-   **E - Extra - :** Hình thức trình bày (bảng, gạch đầu dòng, code có chú thích...).
    
-   **T - Tone (Giọng điệu):** Văn phong phản hồi (thân thiện, hài hước, học thuật...).



