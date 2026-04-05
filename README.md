# Filament Admin Panel - Bài tập quản lý Danh mục & Sản phẩm

## Thông tin sinh viên
- **MSSV**: 23810310091
- **Họ và tên**: [Tên sinh viên]

## Yêu cầu đã thực hiện
- [x] **Cấu trúc dữ liệu**:
    - Bảng `sv23810310091_categories` và `sv23810310091_products` (Sử dụng tiền tố MSSV).
    - Các trường dữ liệu đầy đủ theo yêu cầu (id, name, slug, price, stock_quantity, image_path, status, etc.).
- [x] **Quản lý Danh mục (Category Resource)**:
    - Tự động tạo slug khi nhập name.
    - Bộ lọc `is_visible` trong danh sách.
- [x] **Quản lý Sản phẩm (Product Resource)**:
    - Form sử dụng Grid layout.
    - Sử dụng Rich Editor cho mô tả sản phẩm.
    - Cho phép upload 01 ảnh đại diện (lưu trong thư mục `products`).
    - Hiển thị giá tiền theo định dạng VNĐ (Sử dụng `.money('VND')`).
    - Tìm kiếm theo tên và lọc theo danh mục.
    - Validation: Giá không được âm, số lượng tồn kho phải là số nguyên.
- [x] **Tùy chỉnh giao diện**:
    - Màu Primary được đổi sang mã màu **Indigo** (trong `AdminPanelProvider.php`).
- [x] **Trường thông tin sáng tạo**:
    - Thêm trường `brand_origin` (Xuất xứ thương hiệu) cho Product.
- [x] **Lịch sử Git**:
    - Đã có ít nhất 05 commits với nội dung rõ ràng.

## Hướng dẫn cài đặt
1. Clone repository.
2. Chạy `composer install`.
3. Sao chép `.env.example` thành `.env` và cấu hình cơ sở dữ liệu.
4. Chạy migration: `php artisan migrate`.
5. Tạo tài khoản admin: `php artisan make:filament-user`.
6. Truy cập `/admin`.

**Lưu ý**: Nếu gặp lỗi thiếu driver SQLite, hãy bật `extension=pdo_sqlite` trong file `php.ini`.
