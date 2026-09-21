# Nhật Ký Prompts - Exercise 03: Smart Navigation Bar

> **Chủ đề bài làm:** Thanh Điều Hướng Thông Minh & Bảng Chọn Trượt Ngầm (Smart Navbar & Off-Canvas Drawer)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
Bạn là chuyên gia UI/UX và lập trình Front-end chuẩn W3C, hãy tạo thư mục "Exercise-03" để giải quyết Bài 3: Smart Navigation Bar (Thanh điều hướng thông minh).

Yêu cầu kỹ thuật cốt lõi:
1. Đảm bảo chính xác yêu cầu đề bài:
   - Trên Desktop: Hiển thị menu ngang đầy đủ các link, ẩn nút Hamburger bằng CSS display: none.
   - Trên Mobile (< 768px): Ẩn menu ngang bằng display: none, hiển thị nút bấm Hamburger (display: flex).

2. Kiến trúc giao diện & Trải nghiệm người dùng (UX) hiện đại:
   - Khi nhấp vào nút Hamburger trên Mobile, mở một "thanh trượt ngầm" (Off-canvas Drawer) mượt mà lướt ra từ mép phải màn hình thay vì dùng pop-up hay mở trang tab con rời rạc.
   - Nút Hamburger 3 gạch có animation biến hình thành dấu [X] khi đang mở menu.
   - Có lớp màn mờ (Backdrop overlay với blur) bao phủ nền khi mở menu; bấm ra ngoài hoặc nhấn phím ESC sẽ tự động đóng menu.
   - Không hardcode kích thước cố định, sử dụng max-width và tỷ lệ viewport tự co giãn mềm mại.
   - Đảm bảo tính tiếp cận (Accessibility - a11y) với các thuộc tính aria-expanded và aria-hidden.

3. Đồng nhất phong cách thiết kế:
   - Thiết kế tối giản sang trọng (Minimalist Luxury) đồng bộ với Exercise-01 và Exercise-02 của tác giả Phạm Hồng Hải Đăng.
   - Sử dụng CSS Variables, màu be ấm kết hợp xanh lá rừng quý phái, phông chữ Cinzel & Plus Jakarta Sans.
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng hoàn hảo yêu cầu đề bài 3:**
   - Khởi tạo thanh điều hướng với class `.desktop-nav` và `.hamburger-btn`.
   - **Desktop:** `.hamburger-btn { display: none; }` đảm bảo nút 3 gạch hoàn toàn biến mất trên màn hình lớn.
   - **Mobile (`@media (max-width: 768px)`):** `.desktop-nav { display: none; }` và `.hamburger-btn { display: flex; }` giúp chuyển đổi trạng thái giao diện tức thì theo tiêu chuẩn đề thi.
2. **Kỹ thuật Off-canvas Drawer chuẩn quốc tế:**
   - Thay vì mở cửa sổ con phức tạp (popup/iframe/tab mới gây nặng trang và gián đoạn trải nghiệm người dùng), giải pháp sử dụng **thanh trượt ngầm (Off-canvas Drawer)** tích hợp sẵn bằng CSS `transform: translateX(100%)` chuyển sang `translateX(0)` khi kích hoạt.
   - Kích thước linh hoạt `width: 82%; max-width: 340px;` thích ứng với mọi đời điện thoại từ màn hình nhỏ đến tablet.
3. **Hiệu năng cao & Logic JavaScript tinh gọn:**
   - Việc xác định kích thước màn hình hoàn toàn do **CSS Media Queries** đảm nhiệm bằng phần cứng (Hardware Acceleration), không dùng `if..else` nặng nề để bắt sự kiện resize.
   - JavaScript chỉ đảm nhiệm việc chuyển đổi class (`classList.toggle`) và lắng nghe phím tắt `Escape` để đóng menu nhanh chóng.
