# BÁO CÁO BÀI TẬP THỰC HÀNH TỔNG HỢP: KỸ THUẬT PROMPTING NÂNG CAO (LOGIC & CHUỖI)

---

## 1. Thiết kế giải pháp tổng thể



**Kiến trúc chuỗi khép kín:**
* **Prompt 1 :** Kiểm tra tính hợp lệ của dữ liệu đầu vàoNếu lỗi -> ngắt chuỗi ngay, tránh làm crash hệ thống.
* **Prompt 2 ** Nhận JSON sạch từ Bước 1, tính số ngày nghỉ thực tế  và đối chiếu quỹ phép năm.
* **Prompt 3** Nhận kết quả từ Bước 2, xuất thông báo phản hồi chuẩn hóa.

---

## 2. Hệ thống Prompt thực thi 
### Prompt 1: Lọc dữ liệu & Xử lý đứt gãy
```text
### NHIỆM VỤ
Trích xuất và kiểm tra đơn nghỉ phép.

### BẮT LỖI DỊ BIỆT (FALLBACK)
Nếu thiếu ngày bắt đầu/kết thúc, sai định dạng ngày, hoặc ngày kết thúc < ngày bắt đầu: Dừng ngay, chỉ xuất `{"status": "ERROR", "msg": "Dữ liệu không hợp lệ"}`.

### ĐẦU RA (JSON SẠCH)
{"status": "OK", "start": "YYYY-MM-DD", "end": "YYYY-MM-DD", "leave_left": 0}

### ĐẦU VÀO
[Dữ liệu thô từ nhân viên]
