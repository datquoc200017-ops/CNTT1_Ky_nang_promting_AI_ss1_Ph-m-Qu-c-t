# ĐỀ BÀI:
## BTTH
### Bài làm

#### C - Context
Bạn là Chuyên viên xử lý dữ liệu nhân sự cấp cao.

#### R - Request
Trích xuất thông tin ứng viên từ email thô gồm: Họ tên, SĐT, Email, Vị trí, Số năm kinh nghiệm, Kỹ năng chính.

#### E - Explanation
Dữ liệu dùng để import trực tiếp vào database HR nên yêu cầu chính xác 100%, chuẩn định dạng.

#### A - Action & Quy tắc chuẩn hóa
1. Quét email thô và trích xuất đúng 6 trường dữ liệu.
2. Chuẩn hóa:
   - `name`: Viết hoa chữ cái đầu mỗi từ (VD: Nguyễn Văn A).
   - `phone`: Định dạng +84 hoặc viết liền không dấu cách (VD: +84912345678).
   - `experience_years`: Số nguyên/thập phân (nếu mới tốt nghiệp/chưa có kinh nghiệm ghi 0).
   - `skills`: Mảng các kỹ năng không trùng lặp.
3. Xử lý thiếu dữ liệu: Điền `null` trong JSON và "N/A" trong bảng nếu email không đề cập. Cấm tự suy diễn.

#### T - Tone & Ràng buộc đầu ra
- Khách quan, chính xác.
- Chỉ xuất ra **1 bảng Markdown** và **1 mảng JSON thô**. Tuyệt đối KHÔNG viết lời dẫn đầu hay kết thúc.

#### E - Extras (Few-shot Examples)

#### Ví dụ 1
Input: "Chào HR, em là trần văn bình. Em apply vị trí Backend Dev. SĐT: 090 123 4567, mail: binh.tv@gmail.com. Em có 2 năm làm Python, SQL, FastAPI và SQL."
Output:
| Họ tên | SĐT | Email | Vị trí | Kinh nghiệm (năm) | Kỹ năng |
|---|---|---|---|---|---|
| Trần Văn Bình | +84901234567 | binh.tv@gmail.com | Backend Dev | 2 | Python, SQL, FastAPI |

[
  {
    "name": "Trần Văn Bình",
    "phone": "+84901234567",
    "email": "binh.tv@gmail.com",
    "position": "Backend Dev",
    "experience_years": 2,
    "skills": ["Python", "SQL", "FastAPI"]
  }
]

## Ví dụ 2
Input: "Xin chào anh chị, em tên LÊ THỊ CÚC (cuc.le@outlook.com), sinh viên mới ra trường muốn ứng tuyển Thực tập sinh Tester. Em biết dùng Jira và Postman."
Output:
| Họ tên | SĐT | Email | Vị trí | Kinh nghiệm (năm) | Kỹ năng |
|---|---|---|---|---|---|
| Lê Thị Cúc | N/A | cuc.le@outlook.com | Thực tập sinh Tester | 0 | Jira, Postman |

[
  {
    "name": "Phạm Quốc Đạt",
    "phone": null,
    "email": "cuc.le@outlook.com",
    "position": "Thực tập sinh Tester",
    "experience_years": 0,
  }
]

#### Dữ liệu cần xử lý
Input: "{{CHÈN_NỘI_DUNG_EMAIL_THÔ_VÀO_ĐÂY}}"
Output:

2. Chạy thử nghiệm (Test) và Kiểm tra JSON
3. **Họ tên**

**SĐT**

**Email**

**Vị trí**

**Kinh nghiệm (năm)**

**Kỹ năng**

N/A

N/A

N/A

N/A

N/A

N/A

[ { "name": null, "phone": null, "email": null, "position": null, "experience_years": null, "skills": null } ]






