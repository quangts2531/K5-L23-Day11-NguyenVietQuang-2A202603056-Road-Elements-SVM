# Kế hoạch chốt bài nộp — Nguyễn Việt Quang

Ngày rà soát: 2026-11-23  
Phạm vi: bài Road Elements & SVM, Road v1.0  
Trạng thái: **gói nhãn/manifest, report template và 3/3 ảnh minh chứng đã chốt; CVAT 2.74.1, trạng thái completed đã xác nhận. Còn export của Nguyễn Trường Giang để hoàn tất phiếu QC1 peer-review.**

## Đã xác nhận

- Có đủ 28 ảnh đầu vào trong `data/` và bốn export: front, front-extra, fisheye, fisheye-extra.
- `road_check lint` đọc được cả bốn zip, tổng cộng 28 ảnh; không có ảnh nào bị gói kèm trong zip.
- Có 5 cảnh báo QC1-02: A05 thiếu L1/R1, A06 thiếu R1, A09 thiếu R1, A14 thiếu R1. Coach xác nhận cả bốn ảnh không có vạch nhìn thấy được và chấp nhận miễn QC1-02. Lint vẫn hiện cảnh báo vì không lưu quyết định coach.
- Hai zip bàn giao đã được tạo trong `submission/` bằng cách gộp hai export core với hai export extra; zip nguồn vẫn được giữ nguyên trong `result/`. Tên fisheye cuối đã đúng.
- Manifest mới `submission/NguyenVietQuang-manifest.json` khớp byte/hash của hai zip cuối: 16 ảnh front, 12 ảnh fisheye, tất cả đủ tag, không kèm ảnh.
- Lint cuối đọc được đủ 28 ảnh. Năm cảnh báo QC1-02 nằm ở A05, A06, A09, A14; coach xác nhận không có vạch nhìn thấy và miễn cả bốn trường hợp. Không có lỗi gán nhãn được xác nhận trong năm cảnh báo này và lint không báo mã nào khác. Đây chưa phải kết luận kiểm toàn bộ nhãn theo GT.
- CVAT server trả version 2.74.1; người nộp xác nhận cả bốn task đã completed và polyline được vẽ từ dưới lên.
- Ba ảnh CVAT thật `front.png`, `fisheye.png`, `01-project-labels.png` đã được thêm vào report.
- Metadata trong hai ZIP cuối khớp taxonomy Road v1.0: sáu label, kiểu hình, thuộc tính và giá trị; lint không báo label/kiểu/value lạ.
- `templates/report.md` và `templates/qc1_form.md` đã được chỉnh để tách cảnh báo lint, ngoại lệ coach và lỗi peer-review được xác nhận.

## Checklist 5 file nộp

| File yêu cầu | Trạng thái | Việc còn lại |
| --- | --- | --- |
| `NguyenVietQuang-front.zip` | Sẵn sàng; 16 ảnh | Không |
| `NguyenVietQuang-fisheye.zip` | Sẵn sàng; 12 ảnh | Không |
| `NguyenVietQuang-manifest.json` | Sẵn sàng; hash/byte khớp | Không |
| `NguyenVietQuang-report.md` | Đã điền dữ liệu có căn cứ; đủ 3 ảnh | Phiếu QC1 nhận từ Giang sẽ bổ sung sau theo yêu cầu |
| `NguyenVietQuang-qc1-for-NguyenTruongGiang.md` | Đã tạo bản nháp, chưa thể nộp | Cần ZIP front, ZIP fisheye và manifest của Giang để kiểm 6 ảnh, điền 12 mã và kết luận |

## Việc cần làm theo thứ tự

1. **Đã chốt hai zip bàn giao.** `submission/NguyenVietQuang-front.zip` gồm A01–A16; `submission/NguyenVietQuang-fisheye.zip` gồm B01–B12. Bốn zip nguồn còn nguyên trong `result/`.
2. **Đã tạo manifest cuối.** `submission/NguyenVietQuang-manifest.json` ghi revision 1; linter xác nhận 16/16 và 12/12 ảnh đủ tag, `contains_images=false`, đúng hash/byte.
3. **Ảnh minh chứng report đã đủ.** Đã có Project → Labels, front và fisheye trong `submission/screenshots/`; phiếu QC1 nhận từ Nguyễn Trường Giang sẽ bổ sung sau.
4. **Hoàn tất Phiếu QC1 cho Nguyễn Trường Giang.** Bản nháp `submission/NguyenVietQuang-qc1-for-NguyenTruongGiang.md` đã có. Cần ZIP front, ZIP fisheye và manifest của Giang; sau đó kiểm thủ công 6 ảnh, ghi số nhãn, 12 mã, lỗi/ảnh/nhãn/mức, tỉ lệ và quyết định. Không dùng `NguyenVietQuang-qc1-history-draft.md` thay cho phiếu này: bản đó chỉ ghi lint của lô Quang và xác nhận ngoại lệ của coach.
5. **Nộp đúng 5 file sau khi hoàn tất mục 3–4.** Hai zip, manifest, report và phiếu QC1 cho peer.

## Chặn gửi hiện tại

- Phiếu QC1 nhận từ Nguyễn Trường Giang chưa thấy trong workspace; người nộp yêu cầu bổ sung sau.
- Đã biết peer là Nguyễn Trường Giang; chưa có export để hoàn tất QC1 peer-review.

Chưa thể xác nhận “đã sẵn sàng nộp” cho đến khi hoàn tất hai chặn còn lại. Xác nhận ngoại lệ QC1-02 của coach đã được cập nhật vào [báo cáo](NguyenVietQuang-report.md) và [lịch sử QC](NguyenVietQuang-qc1-history-draft.md).
