# Phiếu QC 1 — Road v1.0

> **BẢN NHÁP — CHƯA ĐƯỢC DÙNG ĐỂ NỘP.** Chưa có export/manifest của Nguyễn Trường Giang trong workspace, nên chưa thể chọn mẫu, kiểm nhãn, ghi số lỗi hoặc kết luận Release / Hold / Rework.
>
> Phiếu này ghi kết quả **kiểm thủ công lô của một bạn khác**. Không lấy số dòng `road_check lint` làm số lỗi QC1: lint chỉ gợi ý, không đối chiếu toàn bộ nhãn với GT. Nếu coach xác nhận QC1-02 là vị trí không có vạch nhìn thấy, ghi ngoại lệ riêng và không tính là lỗi đã xác nhận.

Lô được kiểm (học viên): Nguyễn Trường Giang (`member_id: 2A202603073`)  
Người kiểm (học viên): Nguyễn Việt Quang (`member_id: 2A202603056`)  
Ngày tạo bản nháp: 2026-11-23  
Ngày kiểm: Chờ bắt đầu review  
Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): Chưa nhận được  
Số ảnh kiểm: Chưa chọn (yêu cầu 6 ảnh)  
Số nhãn đã kiểm (shape + tag): Chưa kiểm

## Tổng hợp theo mã

| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | Chưa kiểm | Chưa kiểm | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | Chưa kiểm | Chưa kiểm | nặng |
| QC1-03 position | sai thuộc tính / thừa | Chưa kiểm | Chưa kiểm | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | Chưa kiểm | Chưa kiểm | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | Chưa kiểm | Chưa kiểm | chính |
| QC1-06 style, color, kind | sai thuộc tính | Chưa kiểm | Chưa kiểm | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | Chưa kiểm | Chưa kiểm | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | Chưa kiểm | Chưa kiểm | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | Chưa kiểm | Chưa kiểm | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | Chưa kiểm | Chưa kiểm | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | Chưa kiểm | Chưa kiểm | chính |
| QC1-12 file | lỗi file | Chưa kiểm | Chưa kiểm | nhẹ / nặng |

## Danh sách lỗi

Chưa kiểm; bổ sung sau khi nhận ZIP và hoàn thành mẫu review.

| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| ---: | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |

## Ca mơ hồ

Chưa kiểm.

| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
|  |  |  |

## Quyết định

Lỗi nặng: Chưa kiểm  
Lỗi chính / số nhãn đã kiểm: Chưa kiểm  
Lỗi nhẹ: Chưa kiểm  
Ca chờ lead: Chưa kiểm  
Quyết định: **Chưa kết luận — chưa có export peer để kiểm.**

Để hoàn tất phiếu, cần ZIP front, ZIP fisheye và manifest của Nguyễn Trường Giang. Ảnh gốc A01–B12 đã có trong `data/`.

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); “sai thuộc tính” và “lỗi file” là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
