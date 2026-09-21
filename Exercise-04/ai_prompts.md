# Nhật Ký Prompts - Exercise 04: Dark/Light Mode Theme

> **Chủ đề bài làm:** Hệ Thống Giao Diện Sáng / Tối với CSS Variables & Transitions (Dark/Light Mode Theme)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
Bạn là chuyên gia UI/UX và lập trình web chuẩn W3C, hãy tạo thư mục "Exercise-04" để giải quyết Bài 4: Dark/Light Mode Theme (Chế độ Sáng / Tối).

Yêu cầu kỹ thuật cốt lõi:
1. Đảm bảo đúng chuẩn đề bài 4:
   - Khai báo 2 bộ biến màu (CSS Variables): Bộ biến mặc định tại :root là Chế độ Sáng (Light Mode), và bộ biến Chế độ Tối (Dark Mode) được kích hoạt thông qua class .dark-theme.
   - Class .dark-theme sẽ ghi đè toàn bộ các biến màu nền (--bg-page, --bg-card), màu chữ (--color-text-main), viền và độ bóng (--shadow-card).
   - Thiết lập hiệu ứng chuyển tiếp CSS transition mượt mà (0.4s ease) cho mọi thành phần giao diện, tránh tình trạng giật cục hoặc chớp tắt khi đổi theme.

2. Trải nghiệm người dùng (UX) và Tương tác nút bấm:
   - Thiết kế nút cần gạt (Theme Toggle Switch) tinh tế gồm icon Mặt trời ☀️ và Mặt trăng 🌙 với con lăn gạt chuyển vị trí mượt mà (transform: translateX).
   - Xử lý logic nhấp chuột bằng JavaScript sử dụng cấu trúc if...else rõ ràng: Kiểm tra nếu document.body có chứa class .dark-theme thì gỡ bỏ (remove) và ngược lại thêm vào (add).
   - Tích hợp thêm localStorage để lưu lại trạng thái lựa chọn của người dùng, giúp giao diện không bị mất chế độ tối khi tải lại trang (F5).

3. Tính nhất quán trong phong cách thiết kế:
   - Đồng bộ nhận diện tác giả "Phạm Hồng Hải Đăng" và phong cách tối giản sang trọng (Minimalist Luxury) của chuỗi bài tập Tuần 4.
   - Chế độ Sáng: Tông be ấm (#f6f3ed) kết hợp xanh lá rừng sâu (#1b4332).
   - Chế độ Tối: Tông đen ngọc lục bảo huyền bí (#0f1412, #18201b) kết hợp xanh ngọc phát sáng (#52b788) và điểm nhấn vàng ánh kim (#e9c46a).
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng hoàn toàn yêu cầu đề bài 4:**
   - Định nghĩa đầy đủ 2 bộ biến màu rõ ràng: `:root` (Chế độ Sáng mặc định) và `body.dark-theme` (Chế độ Tối ghi đè).
   - Sử dụng thuộc tính `transition: background-color 0.4s ease, color 0.4s ease, border-color 0.4s ease, box-shadow 0.4s ease` cho toàn bộ trang web giúp chuyển đổi êm ái, bảo vệ mắt người dùng.
2. **Hiện thực logic JavaScript chuẩn mực bằng `if...else`:**
   - Hàm `toggleTheme()` kiểm tra trạng thái bằng câu lệnh điều kiện `if (body.classList.contains('dark-theme'))` đúng như ý tưởng thiết kế ban đầu.
   - Bổ sung `localStorage` ghi nhớ trạng thái theo tiêu chuẩn sản phẩm web thực tế.
3. **Thẩm mỹ UI/UX cao cấp:**
   - Nút gạt chuyển chế độ trực quan với chuyển động gạt tròn (`.toggle-knob`) sinh động, có biểu tượng ☀️ và 🌙.
   - Có cả nút bấm phụ trải nghiệm thử nghiệm giữa trang và khu vực trình diễn mã nguồn CSS Variables trực tiếp.
