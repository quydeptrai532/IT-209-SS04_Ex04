# Bài 4: .gitignore và Amend

## Các bước thực hiện

1. Vô tình commit file `credentials.txt` lên Git.
2. Gỡ file khỏi Git nhưng vẫn giữ file trong máy bằng lệnh:

```bash
git rm --cached credentials.txt
```

3. Tạo file `.gitignore` và thêm:

```text
credentials.txt
```

4. Thêm `.gitignore` vào Git:

```bash
git add .gitignore
```

5. Sửa commit gần nhất bằng:

```bash
git commit --amend -m "add gitignore and remove credentials"
```

6. Kiểm tra trạng thái:

```bash
git status
```

7. Kiểm tra commit gần nhất:

```bash
git log -n 1
```

## Kết quả

File `credentials.txt` vẫn còn trong máy nhưng không còn được Git theo dõi. Commit gần nhất đã được sửa lại thành công bằng `--amend`.
