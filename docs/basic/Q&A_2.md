### 1. Node.js là gì?
  - Node.js hoạt động như thế nào?
    + Node.js là môi trường runtime JavaScript, sử dụng engine V8 để thực thi code. 
    + Hoạt động trên mô hình event-driven, không đồng bộ, sử dụng một luồng đơn với Event Loop để xử lý nhiều yêu cầu đồng thời.
  - Tại sao chọn Node.js?
    + Tốc độ cao, không chặn (non-blocking), dễ mở rộng, và hỗ trợ cộng đồng mạnh mẽ.

### 2. Event Loop và Node.js
  - Giải thích Node.js Event Loop và các giai đoạn của nó:
    + Event Loop là cơ chế xử lý các tác vụ không đồng bộ qua các giai đoạn:
    + Timers: Xử lý `setTimeout` và `setInterval`.
    + Pending I/O: Xử lý I/O chưa hoàn tất.
    + Poll: Lấy sự kiện mới.
    + Check: Xử lý `setImmediate`.
  - Hoạt động đơn luồng nhưng vẫn đồng thời:
    + Dựa vào non-blocking I/O và hệ thống thread pool cho các tác vụ nặng (như mã hóa, đọc file).

### 3. Module trong Node.js
  - Module là gì?
    + Là các đơn vị code độc lập.
  - Các loại module:
    + Core modules (vd: fs, http).
    + Built-in modules (đi kèm Node.js).
    + User-defined modules (do người dùng tạo).
  - Export/Import module:
    + `module.exports = ...` (Export).
    + `require('./module')` hoặc `import` (Import).

### 4. NPM (Node Package Manager)
  - NPM là gì?
    + Trình quản lý package cho Node.js.
  - Sự khác biệt giữa `dependencies` và `devDependencies`:
    + `dependencies`: Các gói cần khi ứng dụng chạy.
    + `devDependencies`: Chỉ dùng trong phát triển.
  - Cách gỡ hoặc nâng cấp package:
    + `npm uninstall <package>` hoặc `npm update`.

### 5. Package và Package Management
  - Package là gì?
    + Một tập hợp code chia sẻ chức năng.
  - Tạo package riêng:
    + Viết code, tạo `package.json` (qua `npm init`).
  - Publish package lên NPM:
    + `npm publish` (cần tài khoản NPM).
### 6. Streams và Buffer
  - Streams:
    + Là cách xử lý dữ liệu chunk-by-chunk.
    + Loại: Readable, Writable, Duplex, Transform.
  - Buffer:
    + Là vùng nhớ tạm cho dữ liệu binary. Giúp xử lý stream hiệu quả.

### 7. File System
  - Đọc/ghi file:
    + `Async`: `fs.readFile()` hoặc `fs.writeFile()`.
    + `Sync`: `fs.readFileSync()`.
  - Sync vs Async:
    + `Sync` chặn tiến trình. `Async` không chặn.

### 8. Error Handling
  - Phương pháp xử lý lỗi:
    + ``Callback` (dùng tham số err).
    + ``Promises` (.then() và .catch()).
    + ``Async/Await` (dùng try...catch).
  - Khi nào dùng cái gì:
    + `Callback`: Legacy code.
    + `Promises/Async-Await`: Code dễ đọc hơn.


### 9. HTTP Module
  - Tạo HTTP server:
    + Sử dụng http.createServer().
  - HTTP vs HTTPS:
    + HTTPS mã hóa kết nối, an toàn hơn.
 

### 10. Middleware trong Express.js
  - Middleware là gì?
    + Các hàm xử lý yêu cầu giữa client và server.
  - Loại Middleware:
    + Ứng dụng: Dùng toàn cục (app.use()).
    + Định tuyến: Chỉ dùng cho một route cụ thể.

### 11. Security
  - Lỗ hổng phổ biến:
    + SQL Injection, XSS, CSRF.
  - Cách bảo vệ:
    + Validate input, escape dữ liệu, và sử dụng các thư viện bảo mật.

### 12. Authentication và Authorization
  - JWT là gì?
    + Một token chuẩn dùng để xác minh danh tính người dùng.
  - Authentication vs Authorization:
    + `Authentication`: bạn là ai (login).
    + `Authorization`: bạn có quyền gì.

### 13. Database Integration
  - Kết nối MongoDB/PostgreSQL:
    + Dùng `mongoose` (MongoDB) hoặc `pg` (PostgreSQL).
  - ORM vs Query Builders:
    + ORM: Mô hình hóa dữ liệu (dễ dùng hơn).
    + Query Builders: Gần với SQL thực hơn.

### 14. Performance Optimization
  - Cải thiện hiệu suất:
    + Sử dụng caching, clustering, và tối ưu hóa code.
  - Clustering:
    + Dùng cluster để tận dụng CPU đa luồng.

### 15. Real-time Applications
  - WebSocket:
    + Giao thức giao tiếp hai chiều thời gian thực.
  - WebSocket vs HTTP:
    + WebSocket duy trì kết nối liên tục.

### 16. Testing
  - Công cụ test:
    + Jest, Mocha, Chai.
  - Unit Test vs Integration Test:
    + Unit test kiểm tra từng module.
    + Integration test kiểm tra tích hợp giữa các module.

### 17. Các mô hình lập trình phổ biến bao gồm:

- `Imperative Programming`: Chỉ định các bước thực hiện chi tiết, ứng dụng thực thi các lệnh theo thứ tự cụ thể.
- `Declarative Programming`: Định nghĩa mục tiêu, hệ thống tự động tìm cách thực hiện.
- `Event-driven Programming`: Xử lý dựa trên các sự kiện, ứng dụng phản ứng với các sự kiện đầu vào mà không cần chờ đợi.
- `Object-oriented Programming` (OOP): Tổ chức mã nguồn thành các đối tượng với trạng thái và hành vi.
- `Functional Programming` (FP): Sử dụng các hàm thuần túy và bất biến, tránh thay đổi trạng thái. 
- `Concurrent Programming`: Xử lý các tác vụ đồng thời để tăng hiệu quả.
