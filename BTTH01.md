# [Bài thực hành 1] Lập kế hoạch tài chính cá nhân bằng Chain-of-Thought
## Phần 1: Nhật ký suy luận logic (Reasoning Steps) chỉ ra công thức tính toán và số liệu trung gian.

**Tính toán từng bước (Chain-of-Thought):**

**1. Thu nhập thực nhận sau thuế & bảo hiểm:**

   - Tổng thu nhập gộp = $18.000.000 + 3.500.000 + 1.500.000 = 23.000.000\text{ VNĐ}$

   - Thu nhập thực nhận (Net) = $23.000.000 - 2.000.000 = 21.000.000\text{ VNĐ}$

**2. Chi phí cố định & Trả nợ tối thiểu:**

   - Tổng chi phí cố định = $3.500.000 + 700.000 + 2.500.000 + 600.000 + 200.000 + 800.000 = 8.300.000\text{ VNĐ}$ (Chiếm: $8.300.000 / 21.000.000 \approx 39,52\%$)

   - Tổng trả nợ tối thiểu = $1.200.000 + 1.500.000 + 900.000 = 3.600.000\text{ VNĐ}$ (Chiếm: $3.600.000 / 21.000.000 \approx 17,14\%$)

**3. Lập quỹ tiết kiệm & mục tiêu 12 tháng:**

   - Mức tiết kiệm tối thiểu (20%) = $21.000.000 \times 20\% = 4.200.000\text{ VNĐ/tháng}$

   - Yêu cầu mục tiêu 12 tháng: Quỹ dự phòng ($30.000.000 / 12 = 2.500.000\text{ VNĐ}$) + Quỹ học tập ($10.000.000 / 12 \approx 833.333\text{ VNĐ}$) = $3.333.333\text{ VNĐ/tháng}$.

   - Đề xuất phân bổ 25% thu nhập thực nhận ($5.250.000\text{ VNĐ/tháng}$) để vượt chuẩn mục tiêu:

      > Quỹ dự phòng: $2.500.000\text{ VNĐ}$ ($11,90\%$)

      >Quỹ học tập: $850.000\text{ VNĐ}$ ($4,05\%$)

      >Đầu tư tích lũy: $1.900.000\text{ VNĐ}$ ($9,05\%$)

**4. Phân bổ phần còn lại (Chi tiêu cá nhân & Trả nợ tăng tốc):**

   - Dòng tiền còn lại = $21.000.000 - (8.300.000 + 3.600.000 + 5.250.000) = 3.850.000\text{ VNĐ}$ ($18,34\%$)

   - Phân bổ: Trả nợ gốc tăng tốc (ưu tiên thẻ tín dụng lãi cao): $2.000.000\text{ VNĐ}$ ($9,52\%$) và Chi tiêu cá nhân linh hoạt: $1.850.000\text{ VNĐ}$ ($8,81\%$).


**Mẫu chạy thử Prompt:**

```
"Bạn là một có kinh nghiệm và như một người chuyên gia trong việc lập kế hoạch tài chính cho cá nhân. Đưa ra kế hoạch tài chính cá nhân giúp tối ưu hóa dòng tiền và đưa ra đề xuất phân bổ ngân sách chi tiêu hợp lý. Ràng buộc tài chính (tiết kiệm tối thiểu 20%, trả nợ đúng hạn, quỹ dự phòng).

THU NHẬP:

- Lương: 18.000.000 VNĐ
- Freelance: 3.500.000 VNĐ
- Kinh doanh online: 1.500.000 VNĐ
Thuế và bảo hiểm: 2.000.000 VNĐ


CHI PHÍ CỐ ĐỊNH:

- Thuê nhà: 3.500.000 VNĐ
- Điện nước Internet: 700.000 VNĐ
- Ăn uống: 2.500.000 VNĐ
- Xăng xe: 600.000 VNĐ
- Điện thoại: 200.000 VNĐ
- Học tập: 800.000 VNĐ


CÁC KHOẢN NỢ:

- Thẻ tín dụng: 12.000.000 VNĐ, trả tối thiểu 1.200.000 VNĐ
- Vay tiêu dùng: 20.000.000 VNĐ, trả tối thiểu 1.500.000 VNĐ
- Vay laptop: 9.000.000 VNĐ, trả tối thiểu 900.000 VNĐ


MỤC TIÊU:

- Tiết kiệm tối thiểu 20% thu nhập thực nhận.
- Quỹ dự phòng mục tiêu 30 triệu.
- Quỹ học tập mục tiêu 10 triệu.
- Thời hạn 12 tháng.
- Trả nợ đúng hạn." 
```

**Prompt thiết lập kỹ năng:** Lập kế hoạch tài chính cho cá nhân.

```
Tên:

lập-kế-hoạch-tài-chính

Mô tả:

Lập kế hoạch tài chính chi tiết cho cá nhân

Chỉ dẫn: 

Thiết kế prompt kế hoạch tài chính cho cá nhân hàng tháng từ dữ liệu đầu vào gồm: Thu nhập, Chi phí cố định , Các khoảng nợ, Mục tiêu tiết kiệm.
Lập ra kế hoạch tài chính chi tiết, tối ưu hóa dòng tiền và đưa ra đề xuất phân bổ ngân sách chi tiêu cho thật hợp lý.
Thực hiện suy luận từng bước (Chain-of-Thought) để tính toán ngân sách trước khi xuất ra kết quả cuối cùng.
Thực hiện theo chuẩn khung CREATE (Context - Request - Explanation - Action - Tone - Extras).
Kích hoạt Chain-of-Thought: 'Hãy suy nghĩ từng bước một và tính toán chi tiết trước khi đưa ra kết quả'
Quy trình lập luận gầm các bước:
- Bước 1: Tính toán tổng thu nhập sau khi trừ thuế và chi phí bắt buộc.
- Bước 2: Phân bổ các khoản tiền trả nợ tối thiểu.
- Bước 3: Lập quỹ tiết kiệm và quỹ dự phòng theo tỷ lệ.
- Bước 4: Chia phần còn lại cho chi tiêu cá nhân 
Ràng buộc kỹ thuật:
- Bắt buộc phải hiện thị đầy đủ phép tính cộng trừ nhân chia, không nhảy cóc kết quả.
- Đảm bảo tổng tỷ lệ phần trăm phân bổ ngân sách phải bằng chính xác 100%.
- Ràng buộc tài chính (tiết kiệm tối thiểu 20%, trả nợ đúng hạn, quỹ dự phòng).
- Khi tính toán chi tiết và phân tích từng bước xong, hãy xuất ra dạng Markdown và đảm bảo chỉ từ 200 - 300 chữ cho phần báo cáo trả lời.

```

## Phần 2: Bảng phân bổ ngân sách cuối cùng bằng Markdown Table với các cột: Hạng mục, Số tiền, Tỷ lệ %, Ghi chú.

**Bảng phân bổ ngân sách tối ưu (100% Thu nhập thực nhận: 21.000.000 VNĐ)**

| Hạng mục phân bổ | Số tiền (VNĐ) | Tỷ lệ (%) | Ghi chú tối ưu dòng tiền |
| :--- | :--- | :--- | :--- |
| 1. Chi phí cố định | 8.300.000 | 39,52% | Duy trì kỷ luật, tránh phát sinh ngoài kế hoạch |
| 2. Trả nợ (Tối thiểu + Tăng tốc) | 5.600.000 | 26,67% | 3,6tr trả tối thiểu + 2tr tất toán nhanh thẻ tín dụng | 
| 3. Tiết kiệm & Mục tiêu (25%) | 5.250.000 | 25,00% | 2,5tr Dự phòng + 850k Học tập + 1,9tr Tích lũy |
| 4. Chi tiêu cá nhân linh hoạt | 1.850.000 | 8.81% | Giải trí, mua sắm cá nhân |
| **Tổng cộng** | **21.000.000** | **100%** | **Đảm bảo đủ 30tr dự phòng và 10tr học tập sau 12 tháng** |

