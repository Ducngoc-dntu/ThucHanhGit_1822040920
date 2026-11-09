# BÁO CÁO THỰC HÀNH QUẢN LÝ MÃ NGUỒN VỚI GIT & GITHUB

## 1. Thông tin sinh viên
- Họ tên: **Hà Đức Ngọc**
- Mã số sinh viên: **1822040920**
- Repository: https://github.com/Ducngoc-dntu/ThucHanhGit_1822040920

## 2. Khởi tạo và kết nối repository
```bash
mkdir ThucHanhGit_1822040920
cd ThucHanhGit_1822040920
git init -b main
git remote add origin https://github.com/Ducngoc-dntu/ThucHanhGit_1822040920.git
```
Các lệnh trên tạo thư mục bài làm, khởi tạo local repository với nhánh `main` và kết nối tới GitHub.

## 3. Commit đầu tiên
```bash
git add README.md index.html
git commit -m "Initial commit: Thêm README và cấu trúc HTML"
```
`git add` đưa file vào staging area; `git commit` lưu phiên bản đầu tiên. Commit thực tế: `2c3649a`.

## 4. Tạo nhánh và thêm giao diện
```bash
git switch -c feature/them-giao-dien
git add index.html style.css
git commit -m "feat: Thêm giao diện CSS cơ bản"
git push -u origin feature/them-giao-dien
```
Nhánh riêng giúp phát triển giao diện độc lập. Commit thực tế: `632a121`.

## 5. Merge vào nhánh chính
```bash
git switch main
git merge feature/them-giao-dien --no-edit
git push -u origin main
```
Kết quả local là merge fast-forward; nhánh `main` chứa đủ `README.md`, `index.html` và `style.css`.

## 6. Minh họa cần chụp
1. Terminal sau commit đầu tiên, hiển thị `2c3649a`.
2. Terminal sau commit nhánh tính năng, hiển thị `632a121`.
3. Terminal sau lệnh merge.
4. Trang GitHub hiển thị ba file trên nhánh `main`.
5. Trang GitHub hiển thị nhánh `feature/them-giao-dien`.

> GitHub yêu cầu xác thực bằng GitHub CLI, Personal Access Token hoặc SSH; mật khẩu tài khoản không còn được hỗ trợ khi push HTTPS.
