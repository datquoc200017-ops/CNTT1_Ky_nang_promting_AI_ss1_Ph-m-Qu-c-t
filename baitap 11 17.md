
# BÁO CÁO BÀI TẬP: SO SÁNH TRADE-OFF KỸ THUẬT PROMPTING (LOGIC & CHUỖI)

## Bước 1: Đề xuất 2 Prompt mẫu

### Giải pháp 1: Đơn giản, ngắn gọn

```
Đóng vai nhân viên kế toán. Đọc hóa đơn sau, tính từng bước số tiền khách phải trả sau khi áp dụng mã giảm giá và xuất ra kết quả cuối cùng:

[Hóa đơn]: Mua 2 áo (200k/cái), 1 quần (300k). Mã giảm giá: GIAM10 (giảm 10%).

```

### Giải pháp 2: Chi tiết, có ràng buộc & xử lý đứt gãy
```
### VAI TRÒ
Chuyên viên kiểm toán tài chính tự động.

### QUY TRÌNH XỬ LÝ CHUỖI (BẮT BUỘC TUẦN TỰ)
- Bước 1 (Kiểm tra tính hợp lệ): Xác minh đơn giá, số lượng không âm và mã giảm giá hợp lệ (GIAM10 = 10%, GIAM50K = 50.000đ).
- Bước 2 (Suy luận CoT): Tính tổng tiền gốc -> Tính mức giảm -> Tính tiền thanh toán cuối.
- Bước 3 (Xuất kết quả): Trả về số tiền cuối cùng (đơn vị: VNĐ).

### XỬ LÝ ĐỨT GẪY
- Nếu thiếu thông tin giá/số lượng, số âm hoặc mã giảm giá không tồn tại: Dừng ngay lập tức, chỉ xuất `ERROR_INVALID_INVOICE`.

### ĐỊNH DẠNG ĐẦU RA (JSON)
{"step_1_validation": "...", "step_2_cot_math": "...", "step_3_final_amount": 0}

### DỮ LIỆU ĐẦU VÀO
Mua 2 áo (200.000đ/cái), 1 quần (300.000đ). Mã giảm giá: GIAM10.

```

## Bước 2: Bảng so sánh Trade-off

**Tiêu chí** | **Giải pháp 1 (Đơn giản)** | **Giải pháp 2 (Chi tiết)**
|-|-|-
**Độ dễ hiểu** | **Cao**  | **Trung bình**
**Tốn token** | **Ít** | **Nhiều hơn** 
**Chặn lỗi biên** | **Trung bình**  | **Cực tốt** 
**Tính ổn định chuỗi** | **Thấp** | **Cao** 

## Bước 3: Lựa chọn phương án & Kết quả chạy thử

### 1. Lựa chọn phương án tối ưu

-   **Chọn:**  **Giải pháp 2**.

    

### 2. Kết quả chạy thử (Giải pháp 2)

JSON

```
{
  "step_1_validation": "Hợp lệ: Số lượng và đơn giá dương; mã GIAM10 tương ứng giảm 10%.",
  "step_2_cot_math": "Tổng gốc = (2 * 200.000) + 300.000 = 700.000đ. Giảm 10% = 70.000đ. Thanh toán = 700.000 - 70.000 = 630.000đ.",
  "step_3_final_amount": 630000
}
```
