# Báo cáo cá nhân — Ngày 11

Họ tên: Nguyễn Việt Quang  
Mã học viên: 2A202603056  
Phiên bản CVAT (Help → About): **Cần bổ sung**  
Guideline: Road v1.0  
Lần nộp (`revision` trong manifest): 1  
Thời điểm export theo manifest: 2026-11-22 09:31:29 (giờ Việt Nam)  
Số lần nộp lại sau Rework: 0

Manifest dùng để tổng hợp: `result/NguyenVietQuang-manifest.json`. Manifest revision 1 hiện bao gồm hai zip core; các zip extra được lint riêng và chưa nằm trong manifest này.

## 1. Kiểm project

| Mục | Đúng như guideline Road v1.0? | Ghi chú |
| --- | --- | --- |
| 6 label, đúng kiểu | Theo export/lint: có các label lane, road_curb, crosswalk, drivable, traffic_light, traffic_sign. | Cần ảnh chụp tab Labels để xác nhận kiểu label trong project. |
| Thuộc tính và giá trị | Chưa xác nhận đầy đủ bằng ảnh chụp project. | Lint cuối không báo nhãn hoặc giá trị lạ; vẫn cần đối chiếu CVAT trước khi nộp. |
| 4 tag ảnh | Có theo manifest/lint. | 20/20 ảnh core đủ bốn tag; cần lưu ảnh chụp project làm minh chứng. |

Cách kết thúc polyline trên bản CVAT này: **Cần bổ sung theo thao tác bạn đã dùng trong CVAT.**  
Cách đặt tag ảnh trên bản CVAT này: **Cần bổ sung theo thao tác bạn đã dùng trong CVAT.**

## 2. Số lượng đã gán

Số liệu core lấy từ manifest revision 1. Số liệu extra lấy từ lần lint bốn zip riêng; extra chưa được đưa vào manifest.

| Task | Ảnh | lane | road_curb | crosswalk | drivable | traffic_light | traffic_sign |
| --- | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| front | 12 | 32 | 13 | 3 | 28 | 23 | 16 |
| front-extra (đã làm 4 / 4) | 4 | 9 | 0 | 4 | 10 | 9 | 10 |
| fisheye | 8 | 8 | 11 | 8 | 8 | 2 | 1 |
| fisheye-extra (đã làm 4 / 4) | 4 | 0 | 2 | 5 | 4 | 0 | 0 |

## 3. Bảng ca khó

| Ảnh | Nhãn | Phân vân giữa | Đã chọn | Lý do |
| --- | --- | --- | --- | --- |
| A05 | lane | Thiếu L1 và R1 hay ảnh không có vạch | Không gán thêm theo lời xác nhận của người làm; chờ coach xác nhận | Không nên vẽ vạch không nhìn thấy; lint vẫn báo QC1-02. |
| A06 | lane | Thiếu R1 hay ảnh không có vạch | Không gán thêm theo lời xác nhận của người làm; chờ coach xác nhận | Cần coach xác nhận ngoại lệ QC1-02. |
| A09 | lane | Thiếu R1 hay ảnh không có vạch | Không gán thêm theo lời xác nhận của người làm; chờ coach xác nhận | Cần coach xác nhận ngoại lệ QC1-02. |
| A04, A06, A08, A09, A10, A11, A12 | lane | Một vạch đứt / marking đôi bị ghi thành nhiều polyline cùng position | Đã sửa; lint cuối không còn cảnh báo QC1-05 | Giữ một polyline cho một marking; với marking đôi dùng `kind=double`. Cần kiểm trực quan lần cuối. |

Lint cuối trên hai zip core còn bốn cảnh báo QC1-02: A05 thiếu L1/R1, A06 thiếu R1, A09 thiếu R1. Coach chưa xác nhận các trường hợp này trong lịch sử chat.

## 4. Phiếu QC 1 nhận được

Người QC được chỉ định: Nguyễn Trường Giang (`member_id: 2A202603073`).  
Quyết định nhận được: **Chưa có trong lịch sử chat; cần bổ sung sau khi nhận phiếu QC1 peer-review.**

| Mã lỗi | Số lỗi | Đồng ý? | Đã sửa? |
| --- | ---: | --- | --- |
| Chưa có phiếu QC1 đã hoàn tất trong lịch sử chat | — | Chưa xác định | Chưa xác định |

## 5. Kiểm file export

Lint đã mở được hai zip core và đọc 20 ảnh. Manifest ghi `contains_images=false`, `images_unlabelled=0`, `images_all_tags` là 12/12 cho front và 8/8 cho fisheye.

| File | Mở lại được? | Số shape ảnh 1 (job / file) | Số shape ảnh 2 (job / file) | Tag camera có trong XML? |
| --- | --- | ---: | ---: | --- |
| `NguyenVietQuang-front.zip` | Có, lint đọc được | A01: 10 | A02: 8 | Có theo lint/manifest |
| `NguyenVietQuang-fisheye.zip` | Có, lint đọc được | B01: 2 | B02: 6 | Có theo lint/manifest |

## 6. Ảnh chụp màn hình

1. Tab Labels của project: **Cần chèn ảnh chụp từ CVAT.**
2. Một ảnh camera trước đã gán đủ: **Cần chèn ảnh chụp từ CVAT.**
3. Một ảnh fisheye đã gán: **Cần chèn ảnh chụp từ CVAT.**
4. Một đoạn XML có `<polyline label="lane">`: **Cần chèn ảnh chụp hoặc trích đoạn XML.**

## 7. Tự đánh giá

Lỗi/cảnh báo cần chú ý nhất là QC1-02: lint báo thiếu L1/R1 ở một số ảnh, dù người làm cho biết vạch không nhìn thấy. Để tránh lặp lại, kiểm tra từng bên làn trước khi kết thúc ảnh; nếu vạch thật sự không thấy thì ghi mã ảnh và xin coach xác nhận, không tự vẽ thêm.

Nhãn lane đi vào dữ liệu huấn luyện để model học vị trí vạch. Nếu thiếu một vạch nhìn thấy được, model có thể học nhầm rằng ranh giới làn không tồn tại và bỏ sót nó khi suy luận. Nếu vạch thật sự không thấy, việc không gán nhãn là đúng; coach cần xác nhận để phân biệt với lỗi bỏ sót.

## 8. (Tùy chọn, buffer) Từ polyline đến đích row-anchor

Chưa thực hiện hoạt động row-anchor tùy chọn.
