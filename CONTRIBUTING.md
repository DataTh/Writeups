# Hướng dẫn Đóng góp (Contributing Guide)

Chào mừng các thành viên của **Cyb3rKn1ght TDTU**! Để quản lý các bài writeup được khoa học và gọn gàng, chúng ta sẽ sử dụng quy trình **Fork & Pull Request (PR)**. 

Dưới đây là hướng dẫn chi tiết từng bước để bạn có thể đóng góp bài writeup của mình vào Repository chung của CLB.

---

## 1. Quy trình Fork và Clone

**Bước 1:** Truy cập vào Repository `Writeups` gốc của CLB trên GitHub.
**Bước 2:** Bấm vào nút **Fork** (nằm ở góc trên cùng bên phải) để tạo một bản sao của repo này về tài khoản cá nhân của bạn.
**Bước 3:** Mở Terminal (hoặc Git Bash) trên máy tính của bạn và Clone repository mà bạn vừa fork về máy:
```bash
git clone https://github.com/<tên-github-của-bạn>/Writeups.git
cd Writeups
```

---

## 2. Cách viết và lưu trữ Writeup

Vui lòng tuân thủ cấu trúc thư mục của Repository để bài viết được sắp xếp đúng chỗ. Ví dụ, nếu bạn muốn viết writeup cho một bài Web thuộc giải `Junior.Crypt.2026`:

**Bước 1:** Đi đến thư mục của giải và mảng tương ứng:
```bash
cd Junior.Crypt.2026/Web/
```

**Bước 2:** Tạo file markdown (`.md`) cho bài writeup của bạn. 
*Quy tắc đặt tên file:* Đặt tên file là tên của thử thách (viết thường, không dấu, dùng dấu gạch ngang `-` thay cho khoảng trắng).
> Ví dụ: `sql-injection-101.md`

**Bước 3 (Nếu có ảnh):** 
Nếu bài viết của bạn có sử dụng hình ảnh minh họa, hãy tạo một thư mục `images` (nếu chưa có) bên trong thư mục mảng đó, và lưu ảnh vào đây.
> Cấu trúc ví dụ:
> ```
> Junior.Crypt.2026/
> └── Web/
>     ├── sql-injection-101.md
>     └── images/
>         └── sql_inj_step1.png
> ```
*Lưu ý:* Trong file markdown, hãy chèn ảnh bằng đường dẫn tương đối. Ví dụ:
`![Mô tả ảnh](images/sql_inj_step1.png)`

**Bước 4:** Viết nội dung writeup vào file `.md` vừa tạo. (Bạn có thể dùng Markdown để format code, bôi đậm, chèn link,... cho đẹp mắt nhé).

---

## 3. Commit và Đẩy (Push) lên GitHub của bạn

Sau khi viết xong, lưu file và mở Terminal (tại thư mục Writeups), chạy các lệnh sau để lưu thay đổi:

```bash
# Thêm các file vừa tạo vào staging area
git add .

# Tạo commit với lời nhắn rõ ràng (ví dụ: Thêm writeup bài SQL Injection 101 giải Junior Crypt)
git commit -m "Add writeup for SQL Injection 101 - Junior.Crypt.2026"

# Đẩy (push) code lên repository trên tài khoản cá nhân của bạn
git push origin main
```

---

## 4. Tạo Pull Request (PR)

**Bước 1:** Truy cập lại vào trang Repository đã fork trên tài khoản GitHub cá nhân của bạn.
**Bước 2:** Bạn sẽ thấy một thông báo "This branch is 1 commit ahead of cyb3rkn1ght-tdtu:main" (hoặc tương tự). Hãy bấm vào nút **Contribute** -> **Open pull request**.
**Bước 3:** Kiểm tra lại các thay đổi (file mới, ảnh mới) xem đã chính xác chưa.
**Bước 4:** Điền tiêu đề và mô tả ngắn gọn cho Pull Request (Ví dụ: *Writeup Web - SQL Injection 101*).
**Bước 5:** Bấm **Create pull request**.

🎉 **Xong!** Bây giờ bạn chỉ cần đợi Ban Chủ Nhiệm (hoặc người quản lý Repo) review bài của bạn. Nếu mọi thứ OK, bài của bạn sẽ được **Merge** (hợp nhất) vào kho Writeup chung của Câu lạc bộ!

> **Mẹo nhỏ:** Trước khi bắt tay vào viết một bài mới, hãy luôn chạy lệnh `git pull upstream main` (nếu đã cấu hình upstream) để cập nhật repo của bạn đồng bộ với repo gốc, tránh bị conflict nhé!
