# Phiếu QC 1 — Road v1.0 (bản tổng hợp lịch sử, bản nháp)

> **Chưa phải phiếu QC1 peer-review để nộp.** Bản này chỉ tổng hợp những gì có trong chat về bài của NguyenVietQuang. Người QC được chỉ định ghi dưới đây; chat không có dữ liệu kiểm một bạn khác, số nhãn được lấy mẫu thủ công, hoặc xác nhận của coach cho các ảnh thiếu vạch.

Lô được kiểm (học viên): NguyenVietQuang (tự kiểm qua lint)  
Người kiểm (học viên): Nguyễn Trường Giang (`member_id: 2A202603073`)  
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
| QC1-02 đủ L1, R1 | bỏ sót | 40 vị trí L1/R1 được lint trên 20 ảnh | 4 cảnh báo lint; người nộp nói các vạch không có thật, chờ coach xác nhận | nặng |
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
| 1 | QC1-02 | A05 | lane | nặng | Thiếu L1 theo lint; người nộp nói ảnh không có vạch; chờ coach xác nhận. |
| 2 | QC1-02 | A05 | lane | nặng | Thiếu R1 theo lint; người nộp nói ảnh không có vạch; chờ coach xác nhận. |
| 3 | QC1-02 | A06 | lane | nặng | Thiếu R1 theo lint; người nộp nói ảnh không có vạch; chờ coach xác nhận. |
| 4 | QC1-02 | A09 | lane | nặng | Thiếu R1 theo lint; người nộp nói ảnh không có vạch; chờ coach xác nhận. |

Ảnh A14 từng có cảnh báo thiếu R1 trong lần lint gồm cả extra; A14 không nằm trong hai zip và manifest revision 1 ở trên.

## Ca chờ coach

| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05, A06, A09 | Xác nhận các vị trí L1/R1 bị thiếu có thật sự không có vạch nhìn thấy được không? | Chưa có trong chat. |

## Quyết định tạm thời

Lỗi nặng đã xác nhận: chưa kết luận (4 cảnh báo QC1-02 đang chờ coach xác nhận).  
Lỗi chính / số nhãn đã kiểm: chưa tính được từ lịch sử chat.  
Lỗi nhẹ: chưa có kết luận thủ công.  
Ca chờ lead: 3 ảnh (A05, A06, A09).  
Quyết định tạm thời: **Hold**, chỉ cho bản tự kiểm này, chờ coach xác nhận QC1-02. Đây không phải quyết định QC peer-review để nộp.

Lưu ý: lệnh `lint` kiểm tra định dạng và một số dấu hiệu tự động; nó không thay thế việc lấy mẫu 6 ảnh, kiểm 12 mã trên bài của bạn được ghép, hoặc đối chiếu GT.
