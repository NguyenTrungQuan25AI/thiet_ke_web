# Nhật Ký Prompts - Exercise 05: Responsive Image Gallery

> **Chủ đề bài làm:** Triển Lãm Thiết Kế & Kiến Trúc Tự Co Giãn Cột (Responsive Image Gallery)  
> **Sinh viên:** Phạm Hồng Hải Đăng  
> **Môn học:** Thiết kế Web (Tuần 4 - Design System & Tư Duy Responsive)

---

## Nội dung Prompt đã sử dụng:

```text
Bạn là chuyên gia UI/UX và lập trình Front-end chuẩn W3C, hãy tạo thư mục "Exercise-05" để giải quyết Bài 5: Responsive Image Gallery (Bộ sưu tập ảnh tự co giãn).

Yêu cầu kỹ thuật cốt lõi:
1. Yêu cầu đề bài 5 về CSS Grid:
   - Sử dụng thuộc tính lưới hiện đại:
     grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
   - Không cần viết nhiều câu lệnh @media queries thủ công, để CSS Grid tự động phân phối và co giãn số cột dựa theo chiều rộng màn hình (từ 4 cột, 3 cột, 2 cột đến 1 cột).

2. Kiến trúc Semantic HTML & Trải nghiệm lướt (Skimming UX):
   - Tổ chức cấu trúc .grid-container chứa các thẻ card gallery chuẩn W3C.
   - Mỗi thẻ card bao gồm:
     + Khối ảnh (.image-grid-item) chứa thẻ <img class="responsive-image"> với tỷ lệ vàng aspect-ratio: 4/3 và object-fit: cover để hình ảnh luôn sắc nét, không méo tỷ lệ.
     + Khối nội dung chữ (.content-grid-item) gồm tiêu đề, đoạn văn bản mô tả ngắn gọn, thông tin tác giả để người xem dễ dàng đọc lướt nhanh chóng.
   - Bổ sung thanh lọc danh mục ảnh (Kiến trúc, Thiên nhiên, Nội thất) và cửa sổ phóng to ảnh (Lightbox Modal) để trải nghiệm xem triển lãm chuyên nghiệp hơn.

3. Đồng nhất phong cách thiết kế:
   - Tác giả: "Phạm Hồng Hải Đăng".
   - Phong cách tối giản sang trọng (Minimalist Luxury) đồng bộ với toàn bộ các bài trước: Nền be ấm (#f5f2eb), thẻ card trắng (#ffffff), xanh lá rừng đậm (#1b4332), phông chữ Cinzel & Plus Jakarta Sans.
```

---

## Tiêu chí kỹ thuật đạt được:
1. **Đáp ứng chính xác tuyệt đối yêu cầu đề bài 5:**
   - Khung `.grid-container` áp dụng `display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.75rem;`.
   - Lưới tự động thích ứng với mọi kích thước màn hình mà không phụ thuộc vào media query cố định.
2. **Tuân thủ chuẩn mực W3C & Cấu trúc người dùng đề xuất:**
   - Tích hợp đúng cấu trúc `image-grid-item` (chứa ảnh Unsplash bản quyền mở) và `content-grid-item` (chứa tiêu đề và đoạn văn bản) đi liền nhau trong từng thẻ tác phẩm.
   - Sử dụng `aspect-ratio: 4 / 3` chuẩn hóa tỷ lệ hiển thị cho toàn bộ ảnh trong bộ sưu tập.
3. **Trải nghiệm duyệt lướt (Skimming UX) xuất sắc:**
   - Thẻ hiển thị thông thoáng, hiệu ứng hover nổi bật cùng icon kính lúp phóng to.
   - Có bộ lọc danh mục động bằng JavaScript và Lightbox Modal xem toàn màn hình tiện lợi (hỗ trợ đóng bằng phím ESC).
