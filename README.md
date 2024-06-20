```mermaid
flowchart TB

  subgraph CouponScheduleList.aspx
    A
    I
  end

  subgraph CouponScheduleConfirm.aspx
    A1
    B
    G
    H
  end

  subgraph CouponScheduleRegister.aspx
    C
    D
  end

  subgraph Error.aspx
    F
  end

  Start([Bắt đầu]) --> A[/Chọn lịch phát hành\n cần chỉnh sửa/]
  A --> A1("Hiển thị thông tin chi tiết")
  A1 --> B[/Chỉnh sửa thông tin/]
  B --> C[/"Thay đổi thông tin
      cần chỉnh sửa"/]
  C --> |Xác nhận| D{Kiểm tra thông tin\n chỉnh sửa}
  D --> |OK| G("Hiển thị thông tin
      chi tiết chỉnh sửa")
  D --> |NG| F(Hiển thị thông tin lỗi)
  F --> C
  G --> |Chỉnh sửa| H[("Cập nhật\n thông tin database")]
  H --> I(Hiển thị danh sách\n thiết lập lịch phát hành\n phiếu giảm giá)
  I --> End([Kết thúc])
  
```
