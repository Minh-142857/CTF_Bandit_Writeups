# NHIỆM VỤ
Truy cập vào thư mục "inhere", sau đó lấy password trong file duy nhất đọc được.

# LỜI GIẢI
Tương tự level trước, ta cần truy cập vào thư mục "inhere". Do đó, ta có thể dùng lệnh `cd` để truy cập vào thư mục như sau:
```bash
cd ./inhere
```

Sau đó, ta sử dụng lệnh sau để hiển thị toàn bộ file trong thư mục:
```bash
ls -al
```

![Màn hình lệnh ls -al (Trong thư mục inhere)](./images/ls_al_inhere.PNG)

Vì số lượng file khá ít (khoảng 10 file), ta hoàn toàn có thể `cat` từng file để tìm password.

```bash
cat -- -file0x #Nhớ thêm '--' để báo hiệu kết thúc options
```

Sau khi `cat` toàn bộ file, màn hình trả về như sau:

![Màn hình hoàn thành level](./images/objective.PNG)

# PASSWORD
```
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```
 