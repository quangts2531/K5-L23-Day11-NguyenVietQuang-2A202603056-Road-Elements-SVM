# Báo cáo cá nhân — Ngày 11

| Thông tin | Giá trị | Thông tin | Giá trị |
| --- | --- | --- | --- |
| Họ tên |  | Mã học viên |  |
| Phiên bản CVAT (Help → About hoặc server/about) |  | Guideline | Road v1.0 |
| Lần nộp (`revision` trong manifest) |  | Thời điểm tạo manifest |  |
| Số lần nộp lại sau Rework |  |  |  |

Trạng thái job: front __ / front-extra __ / fisheye __ / fisheye-extra __ (completed / chưa completed).

## 1. Kiểm project

| Mục | Kết quả | Bằng chứng / ghi chú |
| --- | --- | --- |
| 6 label hình và đúng kiểu |  |  |
| Thuộc tính và giá trị |  |  |
| 4 tag ảnh, đúng giá trị camera |  |  |

- Cách vẽ polyline (hướng gần → xa):
- Cách kết thúc polyline:
- Cách đặt tag ảnh và kiểm giá trị:

## 2. Số lượng đã gán

Ghi số hình trong từng task; extra để riêng để tiện đối chiếu với manifest tổng.

| Task | Ảnh | lane | road_curb | crosswalk | drivable | traffic_light | traffic_sign |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| front | 12 |  |  |  |  |  |  |
| front-extra (đã làm __ / 4) |  |  |  |  |  |  |  |
| fisheye | 8 |  |  |  |  |  |  |
| fisheye-extra (đã làm __ / 4) |  |  |  |  |  |  |  |
| **Front tổng** |  |  |  |  |  |  |  |
| **Fisheye tổng** |  |  |  |  |  |  |  |

## 3. Bảng ca khó

| Ảnh | Nhãn | Phân vân giữa | Đã chọn | Lý do / người xác nhận |
| --- | --- | --- | --- | --- |
|  |  |  |  |  |

## 4. Phiếu QC1 nhận được và ngoại lệ

- Người kiểm được chỉ định:
- Phiếu QC1 peer-review đã nhận (tên file / revision):
- Quyết định peer-review nhận được:

| Mã lỗi | Số lỗi được xác nhận | Đồng ý? | Đã sửa / cách xử lý |
| --- | ---: | --- | --- |
|  |  |  |  |

**Ngoại lệ do coach xác nhận (ghi riêng, không tính thành lỗi peer-review):**

| Ảnh / mã | Cảnh báo lint | Xác nhận của coach | Xử lý |
| --- | --- | --- | --- |
|  |  |  |  |

Nếu chưa nhận phiếu peer-review, ghi rõ “chưa nhận được”; không thay bằng kết quả lint hoặc xác nhận ngoại lệ của coach.

## 5. Kiểm file export

- Manifest:
- Lệnh lint và thời điểm chạy:
Tóm tắt: số ảnh đọc được __; ảnh đủ bốn tag __ / __; `contains_images` __; cảnh báo lint __.

| File | Mở được? | Ảnh | Hình | Đủ tag | Có kèm ảnh? |
| --- | --- | ---: | ---: | ---: | --- |
| `<tên>-front.zip` |  |  |  |  |  |
| `<tên>-fisheye.zip` |  |  |  |  |  |
| `<tên>-manifest.json` |  | — | — | — | — |

Phân biệt cảnh báo tự động với lỗi đã xác nhận. `road_check lint` kiểm tra định dạng và một số dấu hiệu; nó không đối chiếu toàn bộ nhãn với GT.

## 6. Ảnh chụp màn hình

Đặt ảnh thật từ CVAT trong `screenshots/` cạnh report; không dùng ảnh hướng dẫn thay cho ảnh bài làm.

1. Project → Labels, thấy 6 label hình và 4 label tag: `screenshots/01-project-labels.png`.
2. Một ảnh front đã gán nhãn: `screenshots/02-front-annotated.png`.
3. Một ảnh fisheye đã gán nhãn, phóng to một polyline cong: `screenshots/03-fisheye-annotated.png`.
4. Một đoạn XML có `<polyline label="lane">`:

```xml
<!-- Dán một polyline thật từ export ở đây. -->
```

## 7. Tự đánh giá

- Lỗi đã được xác nhận bạn mắc nhiều nhất (theo mã QC1-xx) và cách tránh ở Ngày 20:
- Nhãn đó đi vào model ở đâu? Nêu một lỗi đã xác nhận và cách nó có thể làm model học sai. Nếu chỉ có cảnh báo được coach miễn, ghi đó là ngoại lệ chứ không gọi là lỗi đã xác nhận.

## 8. (Tùy chọn, buffer) Từ polyline đến đích row-anchor

| y | 720 | 680 | 640 | 600 | 560 |
| --- | ---: | ---: | ---: | ---: | ---: |
| x của chúng tôi |  |  |  |  |  |
| x của bạn kia |  |  |  |  |  |

1. Nếu dừng polyline sớm 40 px, hàng nào đổi thành “không có làn”?
2. Ở hàng 720 và 560, hai bạn lệch nhau bao nhiêu pixel? Lệch ở hàng nào ảnh hưởng LKA nhiều hơn?
3. Nếu polyline vẽ từ xa về gần, cách tính có đổi không? Script nào sẽ gặp khó?
