# Bài 2 : Chuỗi tấn công từ mật khẩu bị rò rỉ
## 2. Vấn đề
Giải thích cơ chế Hacker sử dụng mật khẩu rò rỉ từ web nhỏ để chiếm đoạt các tài khoản lớn (domino effect).

## 3. Yêu cầu đầu ra 

**Phân tích tại sao mật khẩu cảm tính lại dễ bị bẻ khóa hơn mật khẩu do máy tính sinh ra.**
-Vì mật khẩu cảm tính làm ta dễ nhớ nhưng cũng tạo cơ hội cho các bot của hacker dễ xâm nhập sau nhiều lần thử khác nhau dẫn dễ dàng bẻ khóa.
-Mật khẩu do máy tính sinh ra là gồm 12 kí tự từ gồm từ in hoa đén in thường lẫn số và các kí tự như @,#,!,... qua đó việc thử chạy bot và đoán ra được là chuyện khó khắn và tốn rất nhiều thời gian.
**Sử dụng tiêu chuẩn **AES-256** để giải thích tại sao việc lưu mật khẩu trong Password Manager lại an toàn hơn ghi chép thủ công.**
  | |PASS MANAGER|Ghi chép thủ công|
  |---|---|---|
  |Dữ liệu mã hóa| kho mật khẩu được mã hóa bằng AES-256| Sổ tay hay file Notes là văn bản thuần, ai thấy là đọc được.  |
  |Master Password|các tài khoản khác dùng chuỗi ngẫu nhiên, độc nhất|mật khẩu ngắn, dễ đoán và dùng lại|
  |Mất thiết bị vẫn an toàn|không có Master Password thì không giải mã được|mất là lộ hết|
  |Zero-knowledge|dữ liệu được mã hóa ngay trên máy bạn, nhà cung cấp cũng không đọc được|Không hỗ trợ|
  |Thêm tiện ích|tự điền đúng tên miền (chống trang giả), cảnh báo mật khẩu yếu/trùng, sao lưu đa thiết bị, hỗ trợ 2FA.|Không có|
