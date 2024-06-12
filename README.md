---
id: EC
title: EC
sidebar_label: EC
---

import ModalViewImage from '@site/src/components/ModalViewImage';

## Tổng quan
### Trang ProductList
- Thêm 1 chọn lọc mới: 【Pt優待区分(固定[1]／%[2]／Ptのみ[3])】
=> Có thể sử dụng chọn lọc mới đúng
### Trang ProductRegister
- Thay đổi hiển thị 2 field 商品連携ID5, 商品連携ID6 lần lượt thành 【Pt優待区分(固定[1]／%[2] ]/Ptのみ[3])】 và 【Pt優待価格／割引率(%)】
- Sử dụng 2 field trên để phân loại cách sử dụng điểm khác nhau và số điểm sẽ dùng.
### Trang MasterExportSettingRegister
- Bảng OrderItem: thêm 2 field mới exchange_point_item_amount (交換ポイント数) và exchange_point_item_quantity (利用ポイント数／ポイント利用額)
- Hiển thị 2 field mới được thêm và sử dụng bình thường đối với bảng có 2 field mới
## Demo tạo Product mới
### Trường hợp 1 (Tạo product với phân loại 1 hoặc 3)
#### Bước 1
### Trường hợp 2 (Tạo product với phân loại 2)
