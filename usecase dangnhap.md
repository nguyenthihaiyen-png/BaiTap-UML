
# Sơ đồ Use Case - Hệ thống đăng nhập

## 1. Prompt nhờ AI hướng dẫn vẽ

Bạn là chuyên gia phân tích và thiết kế hệ thống UML.
Hãy hướng dẫn tôi vẽ sơ đồ Use Case cho chức năng đăng nhập
hệ thống bằng Mermaid.

Yêu cầu:
- Có tác nhân Người dùng.
- Có biên hệ thống Đăng nhập.
- Có use case Nhập thông tin tài khoản.
- Có use case Xác thực thông tin.
- Có use case Thông báo lỗi đăng nhập.
- Có quan hệ giữa tác nhân và các chức năng.
- Sơ đồ sử dụng màu đen trắng, đường nối màu đen.
- Viết mã Mermaid hoàn chỉnh, có thể render trong VS Code
  hoặc Antigravity IDE.
- Hướng dẫn cách lưu file Markdown và cài extension để xem sơ đồ.

## 2. Mã Mermaid vẽ Use Case


# Sơ đồ Activity đăng nhập

```mermaid
flowchart TD
    A(( )) --> B( Nhập thông tin<br/>tài khoản )
    B --> C( Bấm nút Login )
    C --> D( Hệ thống kiểm tra<br/>thông tin )
    D --> E{Thông tin<br/>có đúng?}

    E -- Sai --> H( Hiển thị thông báo<br/>sai thông tin )
    E -- Đúng --> F( Trang chủ )

    H --> I(( ))
    F --> G(( ))

    style A fill:#000,stroke:#000,color:#000
    style B fill:#fff,stroke:#000,color:#000
    style C fill:#fff,stroke:#000,color:#000
    style D fill:#fff,stroke:#000,color:#000
    style E fill:#fff,stroke:#000,color:#000
    style F fill:#fff,stroke:#000,color:#000
    style H fill:#fff,stroke:#000,color:#000

    style G fill:#000,stroke:#000,stroke-width:2px,color:#000
    style I fill:#000,stroke:#000,stroke-width:2px,color:#000

    linkStyle default stroke:#000,stroke-width:2px
```


## 3. Cách mở và render sơ đồ

1. Lưu nội dung này thành file `usecase.md`.
2. Mở file bằng VS Code hoặc Antigravity IDE.
3. Cài extension `Markdown Preview Mermaid Support`.
4. Nhấn `Ctrl + Shift + V` để xem sơ đồ Use Case.

## 4. Kết quả

Sơ đồ mô tả tác nhân Người dùng tương tác với chức năng
đăng nhập, xác thực thông tin, thông báo lỗi và truy cập
trang chủ.

Màu sắc của sơ đồ là đen trắng, đường nối màu đen.
