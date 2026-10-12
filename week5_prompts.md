# Nhật Ký Prompts Thực Tế - Tuần 5: Hiệu Ứng Chuyển Động (CSS Motion Design)

> **Dự án:** Portfolio Cá Nhân Tích Hợp Hiệu Ứng Chuyển Động Chuẩn W3C & 60fps  
> **Sinh viên thực hiện:** Phạm Hồng Hải Đăng  
> **Mã số sinh viên (MSSV):** 125000152  
> **Nhánh Git (Branch):** `feature/animations`  
> **Môn học:** Thiết kế Web (Tuần 5 - Buổi 5)  

---

## 1. Mục đích sử dụng AI & Cam kết trung thực học thuật (Academic Integrity)

Trong bài tập Tuần 5, tôi sử dụng AI với vai trò là **Trợ lý lập trình cặp (Pair Programmer)**. Tôi đóng vai trò là **Kiến trúc sư phần mềm (Software Architect)** định hướng cấu trúc, phân tích ngữ nghĩa W3C, đề xuất giải pháp bố cục Dashboard CSS Grid, và yêu cầu AI hỗ trợ sinh mã nguồn tối ưu GPU 60fps dựa trên các ràng buộc kỹ thuật do tôi chỉ định.

Dưới đây là nhật ký các prompt thực tế được trích xuất trực tiếp từ quá trình làm việc:

---

## 2. Nhật ký Prompt thực tế theo tiến trình làm bài:

### 🔹 Bước 1: Phân tích yêu cầu đề bài & Mục tiêu bài học
* **Prompt của sinh viên:**
  > *"mà bạn giải thích đề của buổi 5 đó. đề đó yêu cầu làm gì hả bạn ? và tôi thì thấy đề này đó bảo tôi học gì ?"*
* **Kết quả thu được:**
  - Xác định rõ 6 bài tập rèn luyện (Floating Action Button, Card Flip 3D, Typing Effect, Parallax Scrolling, Hamburger Menu, Skill Bar Animation).
  - Nắm vững 3 nhóm hiệu ứng bắt buộc: Hover, Keyframes, Scroll.
  - Nắm được tiêu chí đánh giá trọng tâm của giảng viên: Tối ưu hiệu năng chuyển động bằng `transform` và `opacity` (Hardware Acceleration 60fps).

---

### 🔹 Bước 2: Đề xuất kiến trúc thành phần (Component) & Ý tưởng bố cục CSS Grid
* **Prompt của sinh viên:**
  > *"bạn là chuyên gia phần mềm web , theo tôi thì nghĩ là có lẽ dùng gắn liền chuẩn cấu trúc thành phần component , riêng nút tròn liên hệ thì dùng thẻ <footer> thì mới chuẩn ngăn cách vách ngăn phù hợp thay vì <head> hay <main>. dùng kỹ thuật CSS Grid vì tôi thì nghĩ bố cục sẽ là dashboard nhiều ô đóng vai mục cuộn và vài cột"*
* **Kết quả thảo luận & Phản biện kỹ thuật:**
  - AI phân tích: Ý tưởng chia Component và dùng CSS Grid Dashboard (Bento Grid) là rất hiện đại và chuẩn mực.
  - Về vị trí nút FAB tròn: Nếu để lồng bên trong `<footer>`, khi footer áp dụng thuộc tính `transform` hay `filter` thì nút có nguy cơ bị "nhốt" trong phạm vi footer thay vì bay lơ lửng cố định trên toàn viewport (`position: fixed`).
  - Đề xuất kỹ thuật: Dùng thẻ ngữ nghĩa `<aside class="floating-fab">` đặt ngay sau `<footer>` để vừa độc lập, vừa chuẩn W3C Semantic.

---

### 🔹 Bước 3: Phản biện chuyên môn & Chốt phương án Semantic HTML
* **Prompt của sinh viên:**
  > *"ok , tôi đón nhận ý kiến của bạn. tôi vẫn giữ nguyên quan niệm dùng gắn liền chuẩn cấu trúc thành phần component , và đồng ý cho rằng dùng W3C Semantic bằng thẻ <aside class="floating-fab"> và đặt sau <footer> , tôi vẫn giữ nguyên quan điểm dùng Grid CSS"*
* **Kết quả thực thi:**
  - Xây dựng bố cục chính bằng CSS Grid 12 cột (Bento Grid) với các ô thẻ đa năng.
  - Thẻ `<aside class="floating-fab">` được đặt sau `<footer>`, không phá vỡ luồng tài liệu.

---

### 🔹 Bước 4: Yêu cầu hiện thực hóa 6 hiệu ứng chuyển động tối ưu 60fps
* **Prompt chỉ đạo kỹ thuật:**
  > *"Hãy tạo trang Portfolio hoàn chỉnh kết hợp đầy đủ 6 hiệu ứng chuyển động Tuần 5 theo kiến trúc trên:
  > 1. Floating Action Button: Hiệu ứng pulse phập phồng (Keyframes) cho nút tròn liên hệ.
  > 2. Card Flip 3D: Thẻ lật 180 độ theo trục Y khi hover (Hover), có perspective 1200px.
  > 3. Typing Effect: Chữ tự gõ bằng CSS thuần, tuyệt đối không dùng JavaScript.
  > 4. Parallax Image: Ảnh nền cố định trôi chậm hơn chữ khi cuộn bằng background-attachment: fixed (Scroll).
  > 5. Hamburger Menu: 3 gạch biến hình mượt mà thành dấu X khi mở menu di động.
  > 6. Skill Bar Animation: Thanh kỹ năng chạy dải màu tự động từ 0% đến độ dài đích.
  > Toàn bộ hiệu ứng phải tối ưu bằng transform và opacity để đạt chuẩn 60fps."*

---

## 3. Bảng đối soát tiêu chuẩn đánh giá bài nộp:

| Tiêu chuẩn đề bài | Giải pháp thực hiện trong mã nguồn | Đánh giá |
| :--- | :--- | :---: |
| **Nhóm Hover** | 3D Card Flip (`rotateY(180deg)`), hiệu ứng lướt thẻ dự án | ✅ Đạt |
| **Nhóm Keyframes** | Typing Effect CSS thuần, FAB Pulse Wave, Skill Bars | ✅ Đạt |
| **Nhóm Scroll** | Parallax Image Banner (`background-attachment: fixed`) | ✅ Đạt |
| **Tối ưu GPU** | 100% chuyển động dùng `transform`, `opacity` và `will-change` | ✅ Đạt |
| **Kiến trúc W3C** | Cấu trúc Bento Grid, `<aside class="floating-fab">` đặt sau `<footer>` | ✅ Đạt |
| **Nhánh Git** | Nhánh `feature/animations` với commit message rõ ràng | ✅ Đạt |
