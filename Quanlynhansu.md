# TÀI LIỆU PHÂN TÍCH USE CASE - HỆ THỐNG QUẢN LÝ NHÂN SỰ

---

## 1. Xác Định Actors & Phân Rã Chức Năng

### 1.1. Tác nhân (Actors)
* **Nhân viên (Employee):** Người dùng nội bộ thao tác trên dữ liệu cá nhân của chính mình.
* **Quản lý Chi nhánh (Branch Manager):** Cán bộ phụ trách quản lý nhân sự thuộc đơn vị, điều chuyển nhân sự và kết xuất các biểu mẫu báo cáo.

### 1.2. Danh sách Use Cases

| Mã UC | Tên Use Case | Tác nhân chính | Mô tả chức năng |
| :--- | :--- | :--- | :--- |
| **UC01** | Xem hồ sơ cá nhân | Nhân viên | Cho phép nhân viên xem thông tin hồ sơ của chính mình |
| **UC02** | Cập nhật thông tin cá nhân | Nhân viên | Cho phép sửa số điện thoại, địa chỉ và ảnh đại diện của bản thân |
| **UC03** | Bổ sung khả năng ngoại ngữ | Nhân viên | Thêm thông tin trình độ/chứng chỉ ngoại ngữ mới |
| **UC04** | Tra cứu nhân viên | Quản lý Chi nhánh | Tìm kiếm, lọc và xem thông tin nhân sự trong chi nhánh |
| **UC05** | Cập nhật thông tin nhân viên | Quản lý Chi nhánh | Cập nhật số điện thoại, địa chỉ, ảnh đại diện của nhân viên |
| **UC06** | Chuyển đơn vị cho nhân viên | Quản lý Chi nhánh | Điều chuyển nhân viên sang bộ phận hoặc đơn vị công tác mới |
| **UC07** | Lập báo cáo thống kê BM2 | Quản lý Chi nhánh | Tạo và xuất biểu mẫu thống kê BM2 |
| **UC08** | Lập báo cáo thống kê BM3 | Quản lý Chi nhánh | Tạo và xuất biểu mẫu thống kê BM3 |

---

## 2. Sơ Đồ Use Case (Mermaid)

```mermaid
flowchart LR
    %% Khai bao Actors
    NV["Nhân viên"]
    QL["Quản lý Chi nhánh"]

    %% He thong va Use Cases
    subgraph HeThong ["Hệ Thống Quản Lý Nhân Sự"]
        direction TB

        subgraph Nhom_NV ["Chức năng Cá nhân"]
            UC01(["UC01: Xem hồ sơ cá nhân"])
            UC02(["UC02: Cập nhật thông tin cá nhân (ĐT, Địa chỉ, Hình)"])
            UC03(["UC03: Bổ sung khả năng ngoại ngữ"])
        end

        subgraph Nhom_QL ["Chức năng Quản trị Chi nhánh"]
            UC04(["UC04: Tra cứu nhân viên"])
            UC05(["UC05: Cập nhật thông tin nhân viên (ĐT, Địa chỉ, Hình)"])
            UC06(["UC06: Chuyển đơn vị cho nhân viên"])
            UC07(["UC07: Lập báo cáo thống kê BM2"])
            UC08(["UC08: Lập báo cáo thống kê BM3"])
        end
    end

    %% Ket noi giua Actor va Use Cases
    NV --> UC01
    NV --> UC02
    NV --> UC03

    QL --> UC04
    QL --> UC05
    QL --> UC06
    QL --> UC07
    QL --> UC08

```

---

## 3. Sơ Đồ Use Case Chuẩn PlantUML (Tùy chọn)

```plantuml
@startuml
left to right direction
skinparam packageStyle rectangle

actor "Nhân viên" as NV
actor "Quản lý Chi nhánh" as QL

rectangle "Hệ Thống Quản Lý Nhân Sự" {
    package "Hồ sơ cá nhân" {
        usecase "Xem hồ sơ cá nhân" as UC01
        usecase "Cập nhật thông tin cá nhân\n(Điện thoại, Địa chỉ, Hình)" as UC02
        usecase "Bổ sung khả năng ngoại ngữ" as UC03
    }

    package "Nghiệp vụ Quản lý" {
        usecase "Tra cứu nhân viên" as UC04
        usecase "Cập nhật thông tin nhân viên\n(Điện thoại, Địa chỉ, Hình)" as UC05
        usecase "Chuyển đơn vị cho nhân viên" as UC06
        usecase "Lập báo cáo thống kê (BM2)" as UC07
        usecase "Lập báo cáo thống kê (BM3)" as UC08
    }
}

NV --> UC01
NV --> UC02
NV --> UC03

QL --> UC04
QL --> UC05
QL --> UC06
QL --> UC07
QL --> UC08

@enduml
```