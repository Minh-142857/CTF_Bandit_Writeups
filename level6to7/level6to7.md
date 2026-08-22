# NHIỆM VỤ
Lấy password trong file có các thuộc tính sau:
- User: bandit7
- Group: bandit6
- Size: 33 bytes
Phạm vi: Toàn bộ file trong server.

# LỜI GIẢI
Giống như ở level trước, ta có thể dùng lệnh `find` để tìm file có các thuộc tính trên. Tuy nhiên, phạm vi tìm kiếm lúc này là TRÊN TOÀN BỘ SERVER. Do đó, ta cần thêm dấu `/` (thư mục gốc) làm đường dẫn tìm kiếm để terminal tìm trên mọi file trong server: 
```bash
find / -user bandit7 -group bandit6 -size 33c
```

Giải thích lệnh:
- `-user bandit7`: File thuộc về user bandit7.
- `-group bandit6`: File thuộc về group bandit6.

Terminal sẽ trả về như sau:

![Màn hình lệnh find](./images/find.PNG)

Ta thấy có rất nhiều file có cùng thuộc tính ta cần, nhưng đa số sẽ có thêm dòng `Permission denied` (Truy cập bị từ chối). Do đó, ta cần lọc đi những dòng đó bằng cách thêm `2>/dev/null` vào sau lệnh `find` như sau:
```bash
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null # Permission denied sẽ trả về error code 2 -> Đưa tất cả vào null
```

![Màn hình lệnh find](./images/find_filtered.PNG)

Cuối cùng, ta chỉ cần copy đường dẫn và ném vào lệnh `cat` để lấy password.

![Màn hình hoàn thành level](./images/objective.PNG)

# PASSWORD
```
Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
```
 