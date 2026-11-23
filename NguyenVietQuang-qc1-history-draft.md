# Phiếu QC 1 — Road v1.0 (bản tổng hợp lịch sử, bản nháp)

> **Chưa phải phiếu QC1 peer-review để nộp.** Bản này ghi lại kết quả lint của lô NguyenVietQuang và xác nhận ngoại lệ từ coach. Coach cho biết các vị trí ở A05, A06, A09, A14 không có vạch nhìn thấy được và chấp nhận ngoại lệ QC1-02. Chưa có phiếu peer-review hoàn tất, mẫu kiểm thủ công hay quyết định review cho lô của bạn được ghép.

Ghi chú phiên bản: các số liệu 20 ảnh bên dưới là snapshot của hai zip core cũ trong `result/`, trước khi gộp extra. Gói bàn giao cuối (28 ảnh) và manifest hiện hành nằm trong `submission/`; dùng báo cáo cá nhân để đối chiếu số liệu cuối.

Lô được rà bằng lint: NguyenVietQuang (tự kiểm)

Người QC được chỉ định: Nguyễn Trường Giang (`member_id: 2A202603073`); chưa có phiếu nhận được để xác nhận người này đã hoàn tất review.
Ngày tổng hợp: 2026-11-22  
Phiên bản guideline: Road v1.0  
File được kiểm: `NguyenVietQuang-front.zip` + `NguyenVietQuang-fisheye.zip`, revision 1  
Manifest: `result/NguyenVietQuang-manifest.json`, tạo lúc 2026-11-22 02:31:29 UTC  
Số ảnh trong manifest: 20 (A01–A12, B01–B08); 20/20 đủ bốn tag; 0 ảnh chưa gán nhãn; `contains_images=false` cho cả hai zip.  
Số hình theo manifest: lane 40, road_curb 24, crosswalk 11, drivable 36, traffic_light 25, traffic_sign 17 (tổng 153).  
Số ảnh đã kiểm thủ công theo mẫu 6 ảnh và số nhãn đã kiểm thủ công: chưa ghi nhận trong chat.

## Tổng hợp theo mã

| Mã | Loại lỗi | Số mục kiểm | Số lỗi / cảnh báo đã biết | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | Chưa thống kê thủ công | Lint cuối không báo thiếu tag | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 40 vị trí L1/R1 được lint trên 20 ảnh | 4 cảnh báo core và 1 cảnh báo extra; coach xác nhận A05, A06, A09, A14 không có vạch nhìn thấy và chấp nhận miễn QC1-02 | nặng |
| QC1-03 position | sai thuộc tính / thừa | Chưa kiểm đối chiếu GT | Chưa có kết luận | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | Chưa kiểm đối chiếu GT | Bản lint đầu có 1 cảnh báo đảo chiều ở A10; các lần lint sau không còn cảnh báo này | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | Chưa kiểm thủ công | Lint đầu có cảnh báo nhiều polyline cùng position; lint cuối không còn cảnh báo QC1-05 | chính |
| QC1-06 style, color, kind | sai thuộc tính | Chưa kiểm đối chiếu GT | Chưa có kết luận | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | Chưa kiểm đối chiếu GT | Chưa có kết luận | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | Chưa kiểm đối chiếu GT | Chưa có kết luận | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | Chưa kiểm đối chiếu GT | Chưa có kết luận | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | Chưa kiểm đối chiếu GT | Chưa có kết luận | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | Chưa kiểm đối chiếu GT | Chưa có kết luận | chính |
| QC1-12 file | lỗi file | 2 zip core đã được lint mở; số mục kiểm thủ công chưa ghi nhận | Manifest ghi 20 ảnh, 0 ảnh chưa gán nhãn, không kèm ảnh; lint: 4 nặng, 0 chính, 0 nhẹ | nhẹ / nặng |

## Danh sách cảnh báo lint còn lại ở revision 1

| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| ---: | --- | --- | --- | --- | --- |
| 1 | QC1-02 | A05 | lane | nặng | Lint báo thiếu L1; coach xác nhận không có vạch nhìn thấy và chấp nhận ngoại lệ. |
| 2 | QC1-02 | A05 | lane | nặng | Lint báo thiếu R1; coach xác nhận không có vạch nhìn thấy và chấp nhận ngoại lệ. |
| 3 | QC1-02 | A06 | lane | nặng | Lint báo thiếu R1; coach xác nhận không có vạch nhìn thấy và chấp nhận ngoại lệ. |
| 4 | QC1-02 | A09 | lane | nặng | Lint báo thiếu R1; coach xác nhận không có vạch nhìn thấy và chấp nhận ngoại lệ. |
| 5 | QC1-02 | A14 (front-extra) | lane | nặng | Lint extra báo thiếu R1; coach xác nhận không có vạch nhìn thấy và chấp nhận ngoại lệ. |

Ảnh A14 từng có cảnh báo thiếu R1 trong lần lint cả extra; ảnh này không nằm trong zip core cũ, nhưng đã nằm trong gói front cuối ở `submission/`.

## Xác nhận ngoại lệ của coach

| Ảnh | Nội dung cần xác nhận | Kết quả |
| --- | --- | --- |
| A05, A06, A09, A14 | Các vị trí L1/R1 bị lint báo thiếu có vạch nhìn thấy được không? | Coach xác nhận không có vạch nhìn thấy và chấp nhận miễn QC1-02. |

## Tình trạng QC

QC1-02: coach miễn cả 5 cảnh báo lint vì các vị trí được hỏi không có vạch nhìn thấy; không có lỗi gán nhãn được xác nhận trong các cảnh báo này. Đây không phải kết luận về toàn bộ lô.

Lỗi chính / số nhãn đã kiểm: chưa tính được vì chưa có mẫu kiểm thủ công.
Lỗi nhẹ: chưa có kết luận thủ công.
Ca chờ lead: 0 cho bốn ngoại lệ lane; quyết định QC peer-review của bạn được ghép vẫn chưa có.
Quyết định tổng thể cho lô: **chưa xác định**. Chưa có mẫu kiểm thủ công hoặc đối chiếu GT để kết luận Release / Hold / Rework. Đây vẫn là bản tổng hợp lịch sử, không phải phiếu QC1 để nộp.

Lưu ý: lệnh `lint` kiểm tra định dạng và một số dấu hiệu tự động; nó không thay thế việc lấy mẫu 6 ảnh, kiểm 12 mã trên bài của bạn được ghép, hoặc đối chiếu GT.
