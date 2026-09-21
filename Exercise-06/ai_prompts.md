# Nhật Ký Prompts - Exercise 06: Mobile-First Contact Form

> **Chủ đề bài làm:** Biểu Mẫu Liên Hệ Theo Tư Duy Mobile-First (Mobile-First Contact Form)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
Bạn là chuyên gia UI/UX và Front-end chuẩn W3C, hãy tạo thư mục "Exercise-06" để thực hiện Bài 6: Mobile-First Contact Form (Form liên hệ theo tư duy Mobile-First).

Yêu cầu kỹ thuật cốt lõi:
1. Bản chất tư duy Mobile-First:
   - Viết toàn bộ CSS nền tảng (Base styles) ưu tiên cho thiết bị di động trước:
     + Các ô nhập liệu (<input>, <textarea>, <select>) và nút gửi (<button>) đều chiếm width: 100% để người dùng thao tác bấm chạm bằng ngón tay dễ dàng.
     + Khóa cứng cấu trúc co giãn bằng box-sizing: border-box và overflow: hidden để hình ảnh và ô nhập co giãn mượt mà mà không bao giờ bị vỡ khung hay xuất hiện thanh cuộn ngang khó chịu.
   - Nâng cấp dần lên màn hình lớn bằng truy vấn @media (min-width: 768px):
     + Giới hạn chiều rộng của form (max-width: 640px) tránh việc form bị bè quá rộng làm xấu bố cục.
     + Căn giữa màn hình hoàn hảo bằng margin: 0 auto.
     + Nhóm trường Họ và Tên chuyển thành bố cục 2 cột nằm ngang linh hoạt.

2. Trải nghiệm người dùng (UX) và Thẩm mỹ:
   - Tác giả: "Phạm Hồng Hải Đăng".
   - Phong cách tối giản sang trọng (Minimalist Luxury) đồng bộ với toàn bộ bộ bài tập Tuần 4.
   - Có ảnh bìa banner studio không gian xanh với hiệu ứng zoom nhẹ, thông điệp truyền cảm hứng.
   - Xử lý tương tác gửi form bằng JavaScript và hiển thị thông báo Toast đẹp mắt, không bị tải lại trang.
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng chuẩn xác tuyệt đối yêu cầu đề bài 6:**
   - Sử dụng đúng tư duy **Mobile-First**: Mọi thuộc tính kích thước mặc định được tối ưu cho màn hình nhỏ (`width: 100%`), sau đó chỉ dùng `@media (min-width: 768px)` để mở rộng giao diện cho Desktop.
   - Form trên Desktop tự động áp dụng `max-width: 640px; margin: 0 auto;`, đảm bảo tính công thái học (Ergonomics) và sự cân đối hoàn hảo trong thị giác.
2. **Cơ chế khóa cứng cấu trúc hình ảnh & bố cục không bị méo:**
   - Dùng `box-sizing: border-box` trên toàn bộ trang để padding và border không làm nở chiều rộng thực tế.
   - Ảnh biểu trưng (`card-banner img`) sử dụng `object-fit: cover` và `max-width: 100%`, co giãn tự nhiên theo chiều ngang của form mà không bao giờ làm lệch khung.
3. **Trải nghiệm nhập liệu cao cấp (Form UX):**
   - Các ô nhập liệu có hiệu ứng Focus Ring phát sáng nhẹ nhàng (`box-shadow`), nhãn rõ ràng, hỗ trợ đầy đủ thuộc tính `required` và `placeholder` lịch thiệp.
   - Tích hợp thông báo Toast khi gửi thông điệp thành công.
