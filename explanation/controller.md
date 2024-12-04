# async và asyncHandler

```
const asyncHandler = require("express-async-handler");

// @desc Get all contacts
// @route GET /api/contacts
// @access public
const getContacts = asyncHandler(async (req, res) => {
  const contacts = await Contact.find();
  res.status(200).json(contacts);
});
```

- Mục đích:
  - `async/await` được sử dụng để xử lý các thao tác không đồng bộ, giúp mã dễ đọc và tránh callback hell.

- Hoạt động:
  - `asyncHandler`:
    - Là một middleware để bắt và xử lý lỗi phát sinh từ các hàm async mà không cần thêm thủ công `try/catch` trong từng đoạn mã.

  - `async` trong hàm:
    - Định nghĩa `getContacts` là một hàm bất đồng bộ.
    - Cho phép sử dụng `await` để chờ kết quả từ các tác vụ không đồng bộ (ở đây là `Contact.find()`).

  - `await`:
    - Tạm dừng thực thi hàm cho đến khi lệnh `Contact.find()` hoàn tất và trả về kết quả (danh sách `contacts` từ MongoDB).
    - Đảm bảo rằng kết quả trả về sẽ được sử dụng tiếp theo mà không cần xử lý Promise thủ công.

- Lợi ích:
  - Mã sạch và dễ hiểu hơn so với việc sử dụng `.then()` hoặc callback.
  - Tự động chuyển lỗi đến middleware xử lý lỗi nếu có. 

- Ví dụ: Nếu `Contact.find()` bị lỗi, lỗi sẽ được `asyncHandler` xử lý.

- Note: 
  - `Callback` hell là tình trạng mã lồng nhiều callback trong các hàm bất đồng bộ, dẫn đến mã khó đọc, khó bảo trì, và dễ xảy ra lỗi.
