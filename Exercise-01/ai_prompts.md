# Nhật Ký Prompts - Exercise 01: Responsive Typography Scale

> **Chủ đề bài làm:** Môi trường xanh (Green Environment & Sustainable Living)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
bạn là chuyên gia UI/UX, tạo và tách ra một thư mục con có tên "Exercise-01", làm chủ đề là môi trường xanh, áp dụng nguyên tắc thiết kế web tối giản nhưng sang trọng là phải chuẩn hóa thiết kế : kiêng kị tiêu đề khác nhau sẽ làm rối mắt và làm giảm tính thẩm mỹ, tiêu đề thì phải đồng nhất màu và đồng nhất cỡ chữ : màu xanh lá và kích cỡ thì theo tỷ lệ 1:8 so với trang web (để có thể tự động nhỏ hay phóng to tùy theo trang web bị phóng to hoặc thu nhỏ), phải có màu tương phản để nổi bật màu xanh lá của cỡ chữ là màu nâu be, và để phù hợp yêu cầu đề bài 1, thì nên tổ chức cấu trúc:
<head>
<nav>
<main>
bố cục chính
</main>
</nav>
</head>

dùng rem thay vì px, ưu tiên CSS Grid auto-fit, không dùng float hay position tuyệt đối cho bố cục chính. sử dụng thư viện ảnh mã nguồn mở nếu cần lấy ảnh làm minh họa.
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng yêu cầu đề bài 1:** Hệ thống Typography Scale (`h1`–`p`) được quản lý bằng **CSS Variables** tại `:root` và tự động thu nhỏ kích thước khi màn hình `< 600px`.
2. **Phong cách thiết kế:** Tối giản & sang trọng (Minimalist Luxury) với nền màu **nâu be** (`#f5f1ea`) làm nổi bật các tiêu đề đồng nhất màu **xanh lá rừng** (`#1b4332`).
3. **Bố cục chuẩn mực:** Sử dụng **CSS Grid auto-fit** kết hợp đơn vị **rem**, không lạm dụng `float` hay `position: absolute`.
4. **Hình ảnh minh họa:** Sử dụng ảnh chất lượng cao bản quyền mở từ Unsplash về thiên nhiên và môi trường xanh.
