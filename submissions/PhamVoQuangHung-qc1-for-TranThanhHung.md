# Phiếu QC 1 — Road v1.0

Lô được kiểm (học viên): 2A202603247       Người kiểm (học viên): 2A202603259
Ngày: 20/11/2026                          Phiên bản guideline: Road v1.0  
File được kiểm (tên + `revision` trong manifest): QC.zip (bạn chưa gửi manifest nên chưa có `revision`)  
Số ảnh kiểm: 6 (+ __ ảnh thêm, ghi riêng)   Số nhãn đã kiểm (shape + tag): 68  

## Tổng hợp theo mã
| Mã | Loại lỗi | Số mục kiểm | Số lỗi | Mức |
| --- | --- | ---: | ---: | --- |
| QC1-01 tag camera | sai thuộc tính / bỏ sót | 6 | 0 | nặng |
| QC1-02 đủ L1, R1 | bỏ sót | 12 | 0 | nặng |
| QC1-03 position | sai thuộc tính / thừa | 16 | 0 | nặng |
| QC1-04 tâm vạch, chiều, điểm dừng | sai phạm vi / bỏ sót | 16 | 1 | chính |
| QC1-05 vạch đứt, che | sai phạm vi / sai thuộc tính | 16 | 0 | chính |
| QC1-06 style, color, kind | sai thuộc tính | 16 | 0 | chính |
| QC1-07 vùng lái | sai phạm vi / bỏ sót / thừa | 19 | 0 | chính |
| QC1-08 đèn, màu | bỏ sót / sai phạm vi / sai thuộc tính | 3 | 2 | nặng / chính |
| QC1-09 facing, type, group, biển phụ | sai thuộc tính | 9 | 1 | chính |
| QC1-10 hình in, đủ biển | bỏ sót / sai phạm vi | 6 | 0 | chính |
| QC1-11 fisheye | sai phạm vi / sai thuộc tính | 0 | 0 | chính |
| QC1-12 file | lỗi file | 1 | 0 | nhẹ / nặng |

## Danh sách lỗi (mỗi lỗi một dòng)
| # | Mã | Ảnh | Nhãn (label, id) | Mức | Mô tả ngắn |
| --- | --- | --- | --- | --- | --- |
| 1 | Q1-08 đèn | A06 | Traffic_light | chính | thiếu 3 đèn giao thông chưa label |
| 2 | Q1-04 tâm vạch | A06 | Lane | chính | thiếu lane ngăn cách giữa L1 |
| 2 | Q1-09 hình in, đủ biển | A04 | Traffic_sign | chính | Đánh label còn bỏ sót nhiều biển |
| 4 | QC1-08 đèn, màu | A03 | traffic_light (không có) | chính | Thiếu đèn xanh ở xa, khoảng (707,314) |

## Ca mơ hồ
| Ảnh | Câu hỏi cho lead | Lời đáp (nếu có) |
| --- | --- | --- |
| A05 | Đường không có vạch sơn nào, bạn không vẽ L1/R1 và lint báo QC1-02. Ca này có được miễn không? (Phiếu chưa tính là lỗi) | |

## Quyết định
Lỗi nặng: 0   Lỗi chính: 4 / 68 nhãn = 5,9 %   Lỗi nhẹ: 0   Ca chờ lead: 1  
Quyết định (Release / Hold / Rework): Rework  
Lý do (theo luật của phiếu): Không có lỗi nặng, nhưng tỉ lệ lỗi chính 5,9 % vượt ngưỡng 5 %. Ca A05 chờ lead không đổi được kết luận nên không chọn Hold.  

Loại lỗi: bỏ sót = thiếu nhãn phải có; thừa = gán cái không phải đối tượng; sai phạm vi = hình lệch, sai chiều, dừng sai chỗ, tràn vùng. Ba loại này theo cách chia lỗi gán nhãn của ISO/IEC 5259-4 (mục 8.4.2); "sai thuộc tính" và "lỗi file" là khóa học thêm. Cách xếp mức: [thang mức lỗi](../docs/qc_severity_road_v1.0.md).
