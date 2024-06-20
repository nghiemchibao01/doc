```mermaid
flowchart TB

  subgraph CouponScheduleList.aspx
    A
    H
  end

  subgraph CouponScheduleRegister.aspx
    B
    C
  end

  subgraph Error.aspx
    D
  end

  subgraph CouponScheduleConfirm.aspx
    E
    F
  end

  Start([Bắt đầu]) --> A[/Thêm mới\n thông tin/]
    A --> B[/Nhập thông tin\n thêm mới/]
    B --> |Xác nhận| C{"Kiểm tra
        thông tin đã nhập"}
    C --> |OK| E("Hiển thị thông tin lịch
        phát hành phiếu giảm giá đã nhập")
    C --> |NG| D(Hiển thị thông báo lỗi)
    D --> B
    E --> |Đăng ký| F[("Lưu thông tin vào\n Database")]
    F --> H("Hiển thị danh sách
        thiết lập lịch phát hành
        phiếu giảm giá")
    H --> End([Kết thúc])
  
```
