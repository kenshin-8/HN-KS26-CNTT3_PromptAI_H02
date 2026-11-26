# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:**  Hoa Việt Hoàng
- **Lớp:** CNTT3
- **Link repository Pha2:** https://github.com/kenshin-8/HN-KS26-CNTT3_PromptAI_H02.git
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):** ChatGPT

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[\
&#x20; {\
&#x20;   "ma_goi": "DT",\
&#x20;   "ngay_hoi_thao": "2026-12-20",\
&#x20;   "nguoi_lon": 2,\
&#x20;   "tre_em": 1,\
&#x20;   "hang_ve": "thuong",\
&#x20;   "ghi_chu": null\
&#x20; },\
&#x20; {\
&#x20;   "ma_goi": "CB",\
&#x20;   "ngay_hoi_thao": "2027-01-10",\
&#x20;   "nguoi_lon": 3,\
&#x20;   "tre_em": 0,\
&#x20;   "hang_ve": "thuong",\
&#x20;   "ghi_chu": "có một người dùng xe lăn cần lối đi riêng"\
&#x20; },\
&#x20; {\
&#x20;   "ma_goi": "VIP",\
&#x20;   "ngay_hoi_thao": null,\
&#x20;   "nguoi_lon": 4,\
&#x20;   "tre_em": 0,\
&#x20;   "hang_ve": "vip",\
&#x20;   "ghi_chu": "cần ngồi bàn đầu gần màn hình chiếu"\
&#x20; }\
]
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e2bf-7f58-83ec-b870-8f3fbd122401

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
### **1. Kiểm tra bảng giá và quy tắc**

- Gói DT (Gói Đầu Tư): **1.500.000 đồng/người lớn**.
- Trẻ em từ 6–12 tuổi: 50% giá vé người lớn.
- Trẻ dưới 6 tuổi: miễn phí.
- Nhóm từ 4 người lớn trở lên: giảm 10% tiền vé.
- Sổ tay: 200.000 đồng/bộ, không được giảm giá.

### **2. Tính toán từng bước**

**Bước 1: Tiền người lớn**

Có 4 người lớn, mỗi người 1.500.000 đồng.

\\(4 \times 1.500.000 = 6.000.000\\) đồng.

**Bước 2: Tiền trẻ em**

- Trẻ 8 tuổi: \\(1.500.000 \times 50\\% = 750.000\\) đồng.
- Trẻ 11 tuổi: \\(1.500.000 \times 50\\% = 750.000\\) đồng.
- Trẻ 4 tuổi: Miễn phí = 0 đồng.

Tổng tiền trẻ em:

\\(750.000 + 750.000 + 0 = 1.500.000\\) đồng.

**Bước 3: Tiền vé**

Tiền vé = Tiền người lớn + Tiền trẻ em.

\\(6.000.000 + 1.500.000 = 7.500.000\\) đồng.

**Bước 4: Giảm giá nhóm**

Nhóm có 4 người lớn, đủ điều kiện giảm 10%.

\\(7.500.000 \times 10\\% = 750.000\\) đồng.

Tiền vé sau giảm:

\\(7.500.000 - 750.000 = 6.750.000\\) đồng.

**Bước 5: Phụ thu sổ tay**

Nhóm đặt mua 2 bộ sổ tay, mỗi bộ 200.000 đồng.

\\(2 \times 200.000 = 400.000\\) đồng.

**Bước 6: Tổng tiền**

Tổng tiền = Tiền vé sau giảm + Phụ thu sổ tay.

\\(6.750.000 + 400.000 = 7.150.000\\) đồng.

Kết quả cuối cùng

[RESULT: 7.150.000 đồng]
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e2e6-10bc-83ec-ba3e-eb9cf00becf3

### b) Kiểm tra kết quả AI

Đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{\
&#x20; "loai_su_co": "sai_khu_vuc",\
&#x20; "so_khach": 2,\
&#x20; "so_phien_bi_anh_huong": 2,\
&#x20; "tom_tat": "Hai khách mua vé gói DT cho 2 người lớn bị xếp vào dãy ghế phụ phía sau không có bàn viết trong 2 phiên học đầu, không đảm bảo tiện ích khu vực ghế ngồi đã cam kết. Mức đền bù: 400.000 đồng/khách/phiên. Tổng tiền hoàn: 2 × 2 × 400.000 = 1.600.000 đồng. Do tổng mức đền bù vượt 1.200.000 đồng, cần Trưởng phòng Chăm sóc khách hàng phê duyệt trước khi gửi email cho khách."\
}
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e32d-3f8c-83ec-acf5-f955f9353398

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| -------- | ---- | ---------- | ----------- |

\| **1. Đúng thông tin (50%)** | **0/5** | Có 2 lỗi nghiêm trọng:&#x20;
```

**Link trò chuyện:** https://chatgpt.com/share/6b07e37e-776c-83ec-a81a-3594b7366bb2
