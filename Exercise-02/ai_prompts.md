# Nhật Ký Prompts - Exercise 02: Adaptive Card Layout

> **Chủ đề bài làm:** Tạp chí Thiết kế Xanh & Kiến trúc Bền vững (Adaptive News & Editorial Card)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
Bạn là chuyên gia UI/UX và lập trình web chuẩn W3C, hãy tạo thư mục "Exercise-02" để thực hiện Đề bài 2: Adaptive Card Layout (Card tin tức/sản phẩm linh hoạt).

Yêu cầu kỹ thuật cốt lõi:
1. Kiến trúc chuẩn Semantic HTML:
   - Header chứa thông tin tác giả "Phạm Hồng Hải Đăng" và nhận diện trang.
   - Thẻ Card dùng <article class="adaptive-card"> gồm 2 khối chính:
     + Khối ảnh (.card-image-wrapper) chứa thẻ <img> lấy từ thư viện mã nguồn mở Unsplash, object-fit: cover giữ tỷ lệ hoàn hảo.
     + Khối nội dung (.card-content-wrapper) chứa nhãn danh mục, ngày tháng, tiêu đề, đoạn trích tóm tắt, avatar tác giả và nút "Đọc bài viết".

2. Tư duy Responsive với Flexbox & Media Queries:
   - Trên Desktop (màn hình rộng): ảnh nằm bên TRÁI, chữ nằm bên PHẢI sử dụng flex-direction: row.
   - Trên Mobile (màn hình < 768px): ảnh chuyển lên TRÊN, chữ chuyển xuống DƯỚI sử dụng flex-direction: column.

3. Thẩm mỹ & Trải nghiệm (UI/UX):
   - Phong cách tối giản sang trọng (Minimalist Luxury) đồng bộ với Exercise-01: Tông màu be ấm tự nhiên (#f5f2eb), điểm nhấn màu xanh lá rừng sâu (#1b4332) và vàng hổ phách (#b78a48).
   - Phông chữ tiêu đề Cinzel trang trọng, phông nội dung Plus Jakarta Sans hiện đại.
   - Hiệu ứng hover mượt mà (zoom ảnh nhẹ nhàng, nâng bóng đổ card).
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng hoàn toàn yêu cầu đề bài 2:**
   - Sử dụng thuộc tính `display: flex` và chuyển đổi linh hoạt qua thuộc tính `flex-direction`.
   - **Desktop:** `flex-direction: row` (Ảnh chiếm ~42% bên trái, nội dung chữ chiếm ~58% bên phải).
   - **Mobile (`max-width: 768px`):** Tự động chuyển thành `flex-direction: column` (Ảnh chuyển lên trên với tỉ lệ cân đối, chữ nằm ngay ngắn phía dưới).
2. **Tuân thủ chuẩn mực W3C & Semantic HTML:**
   - Tránh việc đặt thẻ giao diện trong `<head>` hay dùng `<h1>` làm thẻ bọc (container). Sử dụng thẻ chuẩn `<article>`, `<header>`, `<main>`, `<section>`, `<h2>`.
   - Tích hợp thẻ `<meta name="author" content="Phạm Hồng Hải Đăng">` chính xác trong phần `<head>`.
3. **Chất lượng hình ảnh & Thư viện mã nguồn mở:**
   - Sử dụng ảnh thiên nhiên & kiến trúc có độ phân giải cao, tối ưu tải từ thư viện Unsplash miễn phí bản quyền.
   - Dùng `object-fit: cover` kết hợp với thuộc tính `loading="lazy"` giúp card hiển thị mượt mà không bị méo tỷ lệ ảnh.
4. **Trải nghiệm người dùng cao cấp:**
   - Hiệu ứng chuyển động mượt mà bằng CSS Transitions (`cubic-bezier`), bo góc mềm mại, đổ bóng đa tầng.
