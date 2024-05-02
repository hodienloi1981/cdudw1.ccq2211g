# GIT VÀ GITHUB.COM
## I. Kiểm tra và cấu hình
__Bước 1.__ Cài đặt git, đăng ký tài khoản github.com

__Bước 2.__ Kiểm tra version
-	Mở cmd.exe
-	Gõ: git --version

__Bước 3.__ Cấu hình git trên máy tinh
-	Mở cmd.exe
-	Gõ: git config --global user.name "HoTen"
-	Gõ: git config --global user.email "Email"
-	Gõ: git config --list kiểm tra
-	Xoá tên: git config --global --unset user.name
-	Xoá email: git config --global --unset user.email
## II. Cấu hình SSH Key
Link thao khảo

https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows

https://www.youtube.com/watch?v=a-zX_qc2S-M

Mở cmd.exe và chạy các lệnh sau

__Bước 1.__
    ssh-keygen -t ed25519 -C "your_email@example.com"

__Bước 2.__
Mở file tài C:\Users\<NameUserPC>\.ssh\id_ed25519.pub
Sao chép nội dung trong tập tin

__Bước 3.__
Mở website https://github.com/settings/keys
New SSH key
Giá nội dung đã sao chép ở bước 2

## III. Đẩy project từ local repository(PC) lên remote repository(Github)
### 1. Lần đầu
Mở cmd.exe
```
Bước 1. git init
Bước 2. git add .
Bước 3. git commit -m "ghi nội dung commit"
Bước 4. git branch -M master
Bước 5. git remote add origin git@github.com:hodienloi1981/cdudw1.ccq2211g.git
Bước 6. git push -u origin master
```
***Trong đó:***

__Bước 1:__ Khỏi tạo init ở local repository

Mỗi project chỉ làm 1 lần đầu

__Bước 2.__ Chuyển file từ trạng thái workspace sang staging

Thêm
```
git add file1 file2 folder1 folder2
git add .
git add -A
git add --a
```
Xoá
```
git rm --cached filename
Di chuyển file
git mv <oldfilename> <newfilename>
```
__Bước 3.__ Chuyển file từ trạng thái workspace, staging sang local repository

Chuyển từ staging sang local repository

git commit -m "ghi nội dung commit"

Chuyển từ workspace sang local repository

git commit -a "ghi nội dung commit"

__Bước 4.__ Chọn nhánh làm việc

git branch -M master

__Bước 5.__ Liên kết local repository(PC) với remote repository(Github)

Trên github.com tạo remote repository(Github)

Chạy lệnh trên cmd.exe

git remote add origin git@github.com:hodienloi1981/cdudw1.ccq2211g.git

__Bước 6.__ Đưa nội dung từ local respository lên remote respository

git push -u origin master

## 2. Repository đã tồn tại
```
Bước 1. git add filename
Bước 2. git commit -m "ghi nội dung commit"
Bước 3. git branch -M master
Bước 4. git remote add origin git@github.com:hodienloi1981/cdudw1.ccq2211g.git
Bước 5. git push -u origin master
```
Github.com Tạo dự án và add thành viên vào nhóm
Tham khảo:
https://www.youtube.com/watch?v=-Rqvfh4UoY4


