<div align="center">
  <h1>LabOdc System</h1>
  <p>Hệ thống Quản lý Dự án và Kết nối Nhân sự Thực tập sinh (OJT)</p>
</div>

---

## 📖 Giới thiệu

**LabOdc** là một nền tảng quản lý dự án nội bộ và kết nối nhân sự toàn diện. Hệ thống được xây dựng nhằm mục đích là cầu nối hiệu quả giữa **Doanh Nghiệp (Company)** có nhu cầu giao việc, **Nhân tài/Sinh viên (Talent)** có mong muốn tích lũy kinh nghiệm thông qua dự án thực tế, và các **Cố vấn (Mentor)** định hướng, quản lý chất lượng dự án.

## ✨ Chức năng chính (Key Features)

LabOdc phân quyền chặt chẽ với 5 vai trò (Roles) cụ thể:

- 👑 **System Admin & Lab Admin**: Quản lý toàn bộ hệ thống, duyệt dự án từ Doanh nghiệp, quản lý người dùng, thống kê và quản lý quỹ (Fund).
- 🏢 **Company (Doanh Nghiệp)**: Đăng tải dự án mới, cập nhật thông tin dự án, xem danh sách dự án của mình và theo dõi tiến độ.
- 🧑‍🏫 **Mentor (Cố vấn)**:
  - Tiếp nhận dự án được phân công.
  - Thêm, sửa, xóa Task. Hỗ trợ import/export Task hàng loạt qua **Mẫu Excel**.
  - Đánh giá chất lượng và review tiến độ hoàn thành Task của Talent.
- 👨‍💻 **Talent (Nhân tài / Thực tập sinh)**:
  - Duyệt và ứng tuyển vào các dự án khả dụng.
  - Xem danh sách công việc (Task) được Mentor giao.
  - Nộp kết quả công việc và xem đánh giá.

## 🛠 Công nghệ sử dụng (Tech Stack)

### Backend

- **Core**: Java 17, Spring Boot 3.5.x
- **Database**: PostgreSQL 17, Hibernate / Spring Data JPA
- **Security**: Spring Security, JWT (JSON Web Token), OAuth2 Resource Server
- **Khác**: Lombok, Maven

### Frontend

- **Core**: React 18, TypeScript, Vite
- **Styling**: Tailwind CSS
- **State Management**: React Hooks
- **Network**: Axios

---

## 🚀 Hướng dẫn cài đặt (Local Setup)

### Yêu cầu hệ thống (Prerequisites)

- [Node.js](https://nodejs.org/) (Phiên bản 18+ khuyến nghị)
- [Java Development Kit (JDK) 17+](https://adoptium.net/)
- [PostgreSQL](https://www.postgresql.org/) (Cài đặt Database `labodc_db`)
- [Maven](https://maven.apache.org/) (Đã tích hợp sẵn `mvnw`)

### 1. Cài đặt Backend

1. Clone dự án về máy:

```bash
git clone <repository_url>
cd Project---JAVA
```

2. Cấu hình Database: Mở file `labOdc/src/main/resources/application.yml` và thay đổi `username`/`password` cho khớp với PostgreSQL của bạn.
3. Chạy Backend bằng Maven Wrapper:

```bash
cd labOdc
./mvnw spring-boot:run
```

> Server Backend sẽ chạy tại: `http://localhost:8082`

### 2. Cài đặt Frontend

1. Mở một Terminal mới và trỏ vào thư mục Frontend:

```bash
cd FE
```

2. Cài đặt các thư viện (Dependencies):

```bash
npm install
```

3. Chạy môi trường phát triển (Dev Server):

```bash
npm run dev
```

> Server Frontend sẽ chạy tại: `http://localhost:5173`

---

## 📁 Cấu trúc dự án (Project Structure)

```text
Project---JAVA/
├── labOdc/                 # Thư mục chứa Source Code Backend (Spring Boot)
│   ├── src/main/java/      # Logic chính (Controller, Service, Repository, Model, DTO, Security)
│   ├── src/main/resources/ # Cấu hình ứng dụng và file tĩnh (templates excel)
│   └── pom.xml             # Cấu hình dependency của Maven
└── FE/                     # Thư mục chứa Source Code Frontend (React/Vite)
    ├── src/                # Logic chính, Pages, Components, Hooks
    ├── package.json        # Cấu hình thư viện Node.js
    └── tailwind.config.js  # Cấu hình giao diện Tailwind
```

## 📜 Giấy phép (License)

Dự án được phát triển nội bộ cho mục đích học tập và quản lý OJT.
