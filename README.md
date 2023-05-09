# **PostgreSQL**

PostgreSQL là một hệ quản trị cơ sở dữ liệu quan hệ mã nguồn mở, được phát triển bởi cộng đồng và được cung cấp miễn phí. Nó là một trong những hệ quản trị cơ sở dữ liệu phổ biến nhất hiện nay và được sử dụng rộng rãi trong các ứng dụng web và doanh nghiệp.

## **Tính năng**

PostgreSQL có các tính năng sau:

- Hỗ trợ ACID (Atomicity, Consistency, Isolation, Durability), đảm bảo tính toàn vẹn của dữ liệu.
- Hỗ trợ các kiểu dữ liệu phong phú, bao gồm cả các kiểu dữ liệu đặc biệt như hình học, âm thanh và văn bản.
- Có khả năng lưu trữ lên đến hàng nghìn tỷ hàng.
- Có khả năng xử lý truy vấn phức tạp và đa luồng, hỗ trợ các chức năng mở rộng để tăng hiệu suất.
- Có khả năng đồng bộ dữ liệu với các máy chủ khác và hỗ trợ các tính năng như giám sát và quản lý dữ liệu.

## Các câu lệnh cơ bản trong PostgreSQL:

1. Tạo một cơ sở dữ liệu:

```
CREATE DATABASE ten_cua_database;

```

1. Tạo một bảng:

```
CREATE TABLE ten_cua_bang (
  cot_1 kieu_du_lieu,
  cot_2 kieu_du_lieu,
  ...
);

```

1. Chèn một bản ghi vào bảng:

```
INSERT INTO ten_cua_bang (cot_1, cot_2, ...) VALUES (gia_tri_1, gia_tri_2, ...);

```

1. Lấy dữ liệu từ bảng:

```
SELECT cot_1, cot_2, ... FROM ten_cua_bang;

```

1. Cập nhật một bản ghi trong bảng:

```
UPDATE ten_cua_bang SET cot_1 = gia_tri_moi WHERE dieu_kien;

```

1. Xóa một bản ghi khỏi bảng:

```
DELETE FROM ten_cua_bang WHERE dieu_kien;

```

Chú ý rằng đây chỉ là một số ví dụ về các câu lệnh trong PostgreSQL và có rất nhiều tính năng và câu lệnh khác trong hệ thống quản trị cơ sở dữ liệu này.

### Sao lưu (backup) và phục hồi (restore) CSDL PostgreSQL:

1. Sao lưu toàn bộ CSDL:

```

pg_dump <database_name> > <backup_file_name>.sql

```

1. Phục hồi toàn bộ CSDL từ tệp sao lưu:

```

psql -d <database_name> -f <backup_file_name>.sql
```

Lưu ý: Khi sao lưu và phục hồi CSDL, bạn cần đăng nhập vào PostgreSQL server với quyền admin để thực hiện các câu lệnh trên.

### Kết nối với PostgreSQL trên localhost, bạn có thể sử dụng câu lệnh sau:

```

psql -h localhost -U <username> -d <database_name>

```

Trong đó:

- **`localhost`**: địa chỉ IP của máy chủ PostgreSQL trên localhost.
- **`<username>`**: tên người dùng được phép truy cập vào CSDL.
- **`<database_name>`**: tên CSDL bạn muốn kết nối đến.

Sau khi chạy câu lệnh này, bạn sẽ được yêu cầu nhập mật khẩu của người dùng. Nếu mật khẩu hợp lệ, bạn sẽ được đưa đến command-line shell của PostgreSQL và có thể thực hiện các câu lệnh để tương tác với CSDL.
