# Bài 2: Khởi chạy Web Server Nginx với Port Mapping

## 1. Khởi chạy container

Lệnh sử dụng:

`docker run -d -p 8080:80 --name my-web nginx:alpine`

Container sử dụng image `nginx:alpine`, có tên `my-web` và ánh xạ cổng 8080 của máy tính tới cổng 80 trong container.

## 2. Kiểm tra trang web

Lệnh kiểm tra:

`curl http://localhost:8080`

Kết quả mong đợi: Trang web trả về mã HTML có nội dung `Welcome to nginx!`.

## 3. Kiểm tra container

Lệnh sử dụng:

`docker ps`

Kiểm tra container `my-web` đang chạy và cổng 8080 được ánh xạ chính xác.

## 4. Dừng và xóa container

Lệnh sử dụng:

`docker stop my-web && docker rm my-web`

Container được dừng và xóa sau khi hoàn tất thử nghiệm.
