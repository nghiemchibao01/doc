---
id: Overview
title: Tổng quan
sidebar_label: Tổng quan
---

## Tống quan task
- Thêm chức năng mới: Bán những sản phẩm quy đổi bằng điểm
- Những luồng ảnh hưởng:
	+ Luồng tạo, cập nhật Product (EC)
	+ Luồng import (EC)
	+ Luồng export (EC)
	+ Luồng order (Front)
## Sơ lượt chức năng
### EC
- Sử dụng id liên kết sản phẩm 5 (cooperation_id5) và id liên kết sản phẩm 6 (cooperation_id6) của bảng w2_Product
=> phân biệt sản phẩm thường và sản phẩm quy đổi bằng điểm.
- Hiển thị thêm thông tin dùng điểm của những order có sản phẩm quy đổi bằng điểm.
### Front
Khi là sản phẩm quy đổi bằng tiền: 
- Sử dụng button add to cart khác và hiển thị nội dung chuyên biệt (ProductDetail).
- Thay đổi lần lượt ở các trang CartList, OrderPayment, OrderConfirm, OrderComplete để hiện thị thông tin của chức năng mới.

## Phạm vi ảnh hưởng
### Front
- Màn hình chi tiết sản phẩm (ProductDetail)
- Màn hình Cart (CartList)
- Màn hình CartListLp (CartListLP)
- Màn hình Landing Page
- Màn hình thanh toán order (OrderPayment)
- Màn hình xác nhận order (OrderConfirm)
- Màn hình hoàn thành đơn hàng (OrderComplete)
- Màn hình chi tiết lịch sử đơn hàng (OrderHistoryDetail)

### EC
- Màn hình xác nhận order (OrderConfirm)
- Màn hình danh sách Product (ProductList)
- Màn hình đăng ký/cập nhật Product (ProductRegister)
- Man hình cập nhật đơn hàng (OrderModifyInput, OrderModifyConfirm)

### Batch MasterFileImport
- Kiểm tra dữ liệu của cooperation_id5, cooperation_id6 khi thêm, cập nhật product, product variation.
