# Rà soát gói nộp — Nguyễn Việt Quang

Ngày rà soát: 2026-11-23  
Phạm vi: Road Elements & SVM, Road v1.0

## Trạng thái hiện tại

Trong `submission/` hiện có hai ZIP bàn giao, manifest, report và bảng QC Release / Hold / Rework. Có đủ 3 ảnh minh chứng trong `submission/screenshots/`. Theo yêu cầu của Quang, không tạo/đính kèm `NguyenVietQuang-qc1-for-NguyenTruongGiang.md`; bảng QC ba trạng thái là tài liệu QC đang có.

## Đã kiểm tra

- Hai ZIP mở được bằng `road_check lint`, tổng cộng 28 ảnh: front A01–A16 và fisheye B01–B12.
- Hash SHA-256 và kích thước hai ZIP khớp manifest; manifest ghi `contains_images=false`, 16/16 và 12/12 ảnh đủ tag.
- Có 3 ảnh CVAT thật và report đã liên kết đúng đường dẫn tương đối.
- Theo xác nhận của người nộp, bốn task đã `completed`, CVAT server là 2.74.1, polyline vẽ từ dưới lên.
- Lint lần rà soát này còn 5 cảnh báo QC1-02: A05 thiếu L1/R1, A06 thiếu R1, A09 thiếu R1, A14 thiếu R1. Coach đã xác nhận không thấy vạch và miễn các cảnh báo; thông tin này được ghi trong report và bảng QC. Lint không báo mã lỗi nào khác.
- Chưa có kiểm thủ công mẫu 6 ảnh, số nhãn kiểm và tỷ lệ lỗi chính. Vì vậy QC status để quyết định lô là chưa kết luận, không tự gán Release.

## Đối chiếu yêu cầu nộp

| Thành phần | Hiện có | Ghi chú |
| --- | --- | --- |
| `NguyenVietQuang-front.zip` | Có | 16 ảnh, manifest/hash khớp |
| `NguyenVietQuang-fisheye.zip` | Có | 12 ảnh, manifest/hash khớp |
| `NguyenVietQuang-manifest.json` | Có | revision 1; không kèm ảnh; đủ tag |
| `NguyenVietQuang-report.md` | Có | Có số liệu, ngoại lệ coach, bảng QC và 3 ảnh minh chứng |
| `NguyenVietQuang-qc-status.md` | Có | Thể hiện Release / Hold / Rework và các finding theo ảnh; quyết định tổng thể chưa kết luận |
| Phiếu QC1 cho Nguyễn Trường Giang | Không có theo yêu cầu của Quang | `SUBMISSION.md` gốc liệt kê phiếu này trong 5 file bắt buộc; thay bằng bảng QC status là sai khác so với checklist gốc |

## Còn thiếu / cần biết trước khi nộp

1. **Khác checklist gốc:** `SUBMISSION.md` yêu cầu phiếu QC1 kiểm bài peer. Gói hiện dùng bảng QC ba trạng thái thay cho phiếu đó theo yêu cầu của Quang. Nếu coach chấp nhận cách thay thế này, không còn thiếu file nào khác trong gói đã chọn; nếu áp dụng nguyên checklist, mục QC1 vẫn thiếu.
2. **Chưa có kết luận QC toàn lô:** Phiếu peer-review 6 ảnh và tỷ lệ lỗi chính chưa có, nên Release chưa được xác nhận. Đây là giới hạn bằng chứng, không phải lỗi lint mới.
3. **Cảnh báo lint vẫn hiện:** Có 5 dòng mức nặng QC1-02 dù coach đã miễn. Report và QC status ghi rõ từng ảnh và lý do; khi nộp cần giữ nguyên phần giải thích này.

Ảnh chụp trong `submission/screenshots/` là tài nguyên nhúng trong report; `SUBMISSION.md` dặn không gửi ảnh rời. Không gửi các file này riêng nếu kênh nộp yêu cầu đúng số file.
