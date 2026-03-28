# 🥗 FreshMeal - Healthy Food Website

<div align="center">
  <img src="https://img.placeholder.com/800x200?text=FreshMeal+-+Healthy+Food+Website" alt="FreshMeal Banner" width="800">
  <p align="center">
    <i>"Sống Khỏe Mỗi Ngày Cùng FreshMeal - Giải Pháp Thực Phẩm Lành Mạnh Toàn Diện"</i>
  </p>

  [![Java](https://img.shields.io/badge/Java-JSP%2FServlet-red.svg)](https://www.java.com/)
  [![MS SQL Server](https://img.shields.io/badge/Database-MS_SQL_Server-blue.svg)](https://www.microsoft.com/en-us/sql-server/)
  [![VNPay](https://img.shields.io/badge/Payment-VNPay-blue.svg)](https://vnpay.vn/)
  [![NetBeans](https://img.shields.io/badge/IDE-NetBeans-green.svg)](https://netbeans.apache.org/)
  [![Bootstrap](https://img.shields.io/badge/Frontend-Bootstrap-blueviolet.svg)](https://getbootstrap.com/)
</div>

---

## 📖 Tổng quan hệ thống (System Overview)

**FreshMeal** là một nền tảng thương mại điện tử chuyên biệt dành cho các sản phẩm và chế độ ăn uống lành mạnh (Healthy Food). Hệ thống không chỉ là nơi mua bán thực đơn lẻ mà còn cung cấp các gói Combo dinh dưỡng dài hạn, giúp người dùng dễ dàng duy trì lối sống khỏe mạnh.

Dự án được xây dựng với mục tiêu kết nối người cung cấp thực phẩm sạch (Seller) với khách hàng, đồng thời tích hợp đội ngũ giao hàng (Shipper) chuyên nghiệp để đảm bảo quy trình khép kín.

---

## 🛠️ Tech Stack

Dự án được phát triển dựa trên các công nghệ tiêu chuẩn, đảm bảo tính ổn định và khả năng mở rộng:

- **Frontend**: JSP, JSTL, HTML5, CSS3, JavaScript (Bootstrap 5).
- **Backend**: Java Servlet (J2EE), Jakarta Mail (Gửi email thông báo).
- **Database**: Microsoft SQL Server.
- **Payment Gateway**: VNPay API.
- **JSON Handling**: Google Gson.
- **Tools**: NetBeans IDE, Apache Tomcat, Git.

---

## 👥 Vai trò người dùng (User Roles)

Hệ thống phân quyền chi tiết với 4 vai trò chính:

| Vai trò | Chức năng chính |
| :--- | :--- |
| **👤 Customer** | Đăng ký/Đăng nhập, tìm kiếm sản phẩm/combo, đặt hàng, thanh toán qua VNPay, theo dõi đơn hàng, quản lý Profile, xem Blog sống khỏe. |
| **🏬 Seller** | Đăng ký gian hàng, quản lý Sản phẩm/Combo thực đơn, cập nhật trạng thái đơn hàng từ khách hàng, thống kê doanh thu. |
| **🚚 Shipper** | Tiếp nhận đơn hàng mới trong khu vực, cập nhật lộ trình giao hàng, xác nhận giao hàng thành công. |
| **🛡️ Admin / Manager** | Quản lý người dùng, duyệt thực đơn/combo mới từ Seller, quản lý Blog, xử lý khiếu nại và xem báo cáo hệ thống. |

---

## 🚀 Tổng quan chức năng (Functional Overview)

- **Quản lý Thực đơn (Menu Management)**: Cho phép Seller tạo các gói combo theo ngày/tuần.
- **Thanh toán trực tuyến**: Tích hợp cổng VNPay bảo mật, nhanh chóng.
- **Thông báo Email**: Tự động gửi email xác nhận đặt hàng và cập nhật trạng thái.
- **Hệ thống Blog**: Chia sẻ kiến thức về dinh dưỡng và tập luyện.
- **Đánh giá & Phản hồi**: Khách hàng có thể để lại nhận xét về món ăn.
- **Theo dõi đơn hàng**: Trạng thái đơn hàng được cập nhật thời gian thực từ Seller đến Shipper.

---

## 📂 Cấu trúc dự án (Project Structure)

```text
HealthyFoodWebsite/
├── FreshMeal/               # Mã nguồn chính của dự án Java Web
│   ├── src/java/            # Chứa các file source code Java
│   │   ├── controller/      # Các Servlets xử lý request từ người dùng
│   │   ├── dal/             # Database Access Layer (DAO, DBContext)
│   │   ├── model/           # Các lớp đối tượng (POJO)
│   │   └── vnpay/           # Cấu hình và xử lý thanh toán VNPay
│   ├── web/                 # Web Pages (Giao diện người dùng)
│   │   ├── WEB-INF/         # Cấu hình bảo mật và thư viện (lib)
│   │   ├── assets/          # CSS, Images, Fonts
│   │   ├── js/              # JavaScript files
│   │   ├── includes/        # Header, Footer, Sidebar dùng chung
│   │   └── *.jsp           # Các trang giao diện chính (Login, Index, Cart,...)
│   └── nbproject/           # Cấu hình dự án NetBeans
└── README.md                # File hướng dẫn dự án
```

---

## ⚙️ Cài đặt & Chạy (Installation & Running)

### 1. Yêu cầu hệ thống
- **Java**: JDK 8 hoặc mới hơn (Ưu tiên JDK 17+).
- **IDE**: NetBeans hoặc IntelliJ IDEA.
- **Server**: Apache Tomcat 9.0+.
- **Database**: SQL Server 2014 trở lên.

### 2. Thiết lập Database
1. Mở SQL Server Management Studio (SSMS).
2. Tạo database mới với tên `SWPproject`.
3. Chạy các file script SQL (nếu có) để tạo bảng và dữ liệu mẫu.
4. Cập nhật thông tin kết nối (User, Password) trong file [DBContext.java](file:///d:/Project_SWP_TryHard/healthy-food-G5/FreshMeal/src/java/dal/DBContext.java).

### 3. Cấu hình VNPay (Nếu cần)
- Cập nhật các key `vnp_TmnCode`, `vnp_HashSecret` trong cấu hình nếu bạn muốn sử dụng môi trường sandbox riêng.

### 4. Triển khai
1. Mở thư mục `FreshMeal` bằng NetBeans.
2. Chuột phải vào Project -> **Clean and Build**.
3. Chuột phải vào Project -> **Run**. Hệ thống sẽ tự động mở trình duyệt tại `http://localhost:8080/FreshMeal`.

---

## 🖥️ Tính năng & Màn hình (Features & Screens)

- **Trang chủ**: Banner khuyến mãi, danh mục món ăn nổi bật và blog mới nhất.
- **Cửa hàng (Menu)**: Bộ lọc sản phẩm theo calo, giá cả và loại thực phẩm.
- **Chi tiết sản phẩm**: Thông tin dinh dưỡng chi tiết (Protein, Carbs, Fats).
- **Giỏ hàng & Thanh toán**: Quy trình checkout 3 bước đơn giản.
- **Dashboard Quản lý**: Giao diện trực quan dành cho Seller và Admin.

---

<div align="center">
  <p>Được phát triển bởi <b>Team G5 - SWP391</b></p>
  <p>© 2026 FreshMeal. All Rights Reserved.</p>
</div>
