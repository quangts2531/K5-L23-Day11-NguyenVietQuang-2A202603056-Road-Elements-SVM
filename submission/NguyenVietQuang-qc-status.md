# Trạng thái QC theo bằng chứng hiện có

> Đây là kết quả lint cộng với ngoại lệ coach, không phải peer-review hoàn chỉnh. Release / Hold / Rework là quyết định ở cấp lô, không gán riêng cho từng ảnh.

| Quyết định QC cấp lô | Kết quả hiện tại | Căn cứ |
| --- | --- | --- |
| Release | Chưa quyết định | Chưa có peer-review thủ công 6 ảnh và tỷ lệ lỗi chính. |
| Hold | Không có ca chờ coach đã biết | Coach đã xác nhận và miễn các cảnh báo QC1-02 nêu dưới đây. |
| Rework | Không yêu cầu cho các finding hiện có | Năm cảnh báo QC1-02 được miễn; lint không báo mã nào khác. Đây không phải kết luận về toàn bộ nhãn. |

## Finding theo ảnh

| Ảnh | Finding lint hiện tại | Xử lý / tình trạng |
| --- | --- | --- |
| A05 | QC1-02 thiếu L1 và R1 (2 cảnh báo) | Coach xác nhận không có vạch nhìn thấy; miễn, không rework cho finding này. |
| A06 | QC1-02 thiếu R1 | Coach xác nhận không có vạch nhìn thấy; miễn, không rework cho finding này. |
| A09 | QC1-02 thiếu R1 | Coach xác nhận không có vạch nhìn thấy; miễn, không rework cho finding này. |
| A14 (front-extra) | QC1-02 thiếu R1 | Coach xác nhận không có vạch nhìn thấy; miễn, không rework cho finding này. |
| A01–A04, A07–A08, A10–A13, A15–A16, B01–B12 | Không có finding trong lint gần nhất | Chưa kiểm thủ công/GT; không gán Release riêng cho các ảnh. |

**Quyết định tổng thể: chưa kết luận.** Chưa có mẫu kiểm thủ công 6 ảnh, số nhãn đã kiểm và tỷ lệ lỗi chính. Coach đã xử lý ngoại lệ QC1-02; xác nhận này không thay thế peer-review toàn lô.
