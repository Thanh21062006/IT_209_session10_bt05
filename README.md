# Bài 5: Tự động hóa điều phối đa dịch vụ với Docker Compose & File .env

## Giới thiệu
Bài tập này thực hiện đóng gói ứng dụng Python (Flask) và cơ sở dữ liệu PostgreSQL sử dụng Docker Compose chuẩn IaC (Infrastructure as Code) kết hợp bảo mật biến môi trường bằng file `.env`.

## Cấu trúc thư mục
- `docker-compose.yml`: Cấu hình dịch vụ đa container.
- `.env.example`: File mẫu chứa các biến môi trường.
- `Dockerfile`: Cấu hình build image cho backend Python.
- `app.py`: Mã nguồn ứng dụng Python kết nối PostgreSQL.
- `requirements.txt`: Thư viện phụ thuộc cho Python.

## Hướng dẫn chạy chương trình
1. Tạo file `.env` từ file mẫu:
   ```bash
   cp .env.example .env
   ```
2. Khởi chạy hệ thống bằng Docker Compose CLI v2:
   ```bash
   docker compose up -d
   ```
3. Kiểm tra trạng thái các container:
   ```bash
   docker compose ps
   ```
4. Xem logs:
   ```bash
   docker compose logs -f
   ```
5. Dừng hệ thống:
   ```bash
   docker compose down
   ```