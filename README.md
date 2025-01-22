# TodoAPI
API RESTful giúp quản lý sách trong một của hàng sáng, được xây dựng bằng ASP.NET Core. API này cho phép thực hiện các thao tác CRUD (Tạo, Đọc, Cập nhật, xóa ) đôi với thông tin sách.
---
## Mục lục
- [Giới thiệu dự án](#giới-thiệu-dự-án)
- [Tính năng](#tính-năng)
- [Công nghệ sử dụng](#công-nghệ-sử-dụng)
- [Cài đặt](#cài-đặt)
- [Sử dụng](#sử-dụng)
---
## Giới thiệu dự án
**TodoAPI** là một ứng dụng Web API tối giản được xây dựng bằng .NET, giúp quản lý danh sách công việc cần làm (*To-Do List*). Ứng dụng này hỗ trợ các thao tác CRUD (Tạo, Đọc, Cập nhật, Xóa) thông qua các endpoint HTTP.

---
## Tính năng
- **Lấy danh sách công việc**: Hiển thị tất cả các công việc hiện có trong hệ thống.
- **Thêm công việc mới**: Cho phép thêm một công việc vào danh sách.
- **Lấy danh sách công việc dựa trên id**: Hiển thị tất cả các công việc trong hệ thống theo id.
- **Cập nhật công việc**: Cập nhật thông tin chi tiết của một công việc cụ thể.
- **Xóa công việc**: Xóa một công việc khỏi danh sách.
- **Lấy công việc đã hoàn thành**: Lọc các công việc đã hoàn thành.

---
## Công nghệ sử dụng
- **Framework**: ASP.NET Core Empty 
- **Ngôn ngữ**: C#
  
---
## Cài đặt

### Các bước thực hiện
1. Tạo một dự án API trong Visual Studio Code

![image](https://github.com/user-attachments/assets/71f4d036-12cf-4adf-8939-b12357c672be)

2. Thêm model và database context class.
-Class **Todo** : Định nghĩa cấu trúc dữ liệu của công việc (các thuộc tính như Id, Name, IsComplete).
- Class **TodoDb**: Tạo và quản lý kết nối với cơ sở dữ liệu, ánh xạ dữ liệu giữa ứng dụng và cơ sở dữ liệu.

3. Thêm Dependency Injection (DI)trong tệp **Program.cs**.

4. Cấu hình các Endpoint (API endpoints).
- Tạo class **BookService**:
  + app.MapGet("/todoitems"): Lấy danh sách tất cả công việc.
  + app.MapGet("/todoitems/complete"): Lấy danh sách các công việc đã hoàn thành (IsComplete = true).
  + app.MapGet("/todoitems/{id}"): Lấy chi tiết một công việc dựa trên ID.
  + app.MapPost("/todoitems"): Tạo mới một công việc.
  + app.MapPut("/todoitems/{id}"): Cập nhật một công việc dựa trên ID.
  + app.MapDelete("/todoitems/{id}"): Xóa một công việc dựa trên ID.

---
## Sử dụng
### Lấy danh sách tất cả công việc.
![image](https://github.com/user-attachments/assets/0d049ca7-4920-48b2-a1b7-1635117f216e)

### Lấy danh sách các công việc đã hoàn thành (IsComplete = true).
![image](https://github.com/user-attachments/assets/51552f32-9200-48d2-b61a-8462f429d2a7)

###  Tạo mới một công việc.
![image](https://github.com/user-attachments/assets/86cc8049-b446-46ec-93a8-589f842f356e)

### Lấy chi tiết một công việc dựa trên ID.
![image](https://github.com/user-attachments/assets/95522f0d-a594-4ed8-b38f-12023f59a973)

### Cập nhật một công việc dựa trên ID.
![image](https://github.com/user-attachments/assets/e8c42de4-897c-4c54-b297-62fb05029542)

### Xóa một công việc dựa trên ID.
![image](https://github.com/user-attachments/assets/25e17020-744b-4288-9d6a-743580be92e9)






