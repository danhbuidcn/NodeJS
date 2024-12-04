### Kiến thức cơ bản về Node.js

1. Node.js là gì?
   - Node.js là một môi trường chạy JavaScript phía máy chủ, 
   - Được xây dựng trên V8 JavaScript Engine của Chrome, cho phép phát triển các ứng dụng mạng và web hiệu quả.

2. Node.js hoạt động như thế nào?
   - Node.js sử dụng mô hình non-blocking I/O và event-driven, cho phép xử lý nhiều yêu cầu đồng thời mà không chặn luồng chính.

3. Các kiểu dữ liệu trong Node.js là gì?
   - Node.js hỗ trợ các kiểu dữ liệu nguyên thủy như Number, String, Boolean, Undefined, Null, Symbol và các kiểu dữ liệu tham chiếu như Object, Array, Function, Buffer.

4. Mô hình I/O non-blocking trong Node.js là gì?
   - Mô hình này cho phép các thao tác I/O được thực hiện không đồng bộ, giúp Node.js xử lý nhiều yêu cầu mà không bị chặn.

5. Lập trình hướng sự kiện (event-driven) là gì?
   - Lập trình hướng sự kiện là mô hình trong đó luồng chương trình được điều khiển bởi các sự kiện, giúp ứng dụng phản hồi nhanh chóng với các hành động của người dùng hoặc hệ thống.

6. Node.js hỗ trợ đa luồng không?
   - Mặc dù Node.js sử dụng mô hình đơn luồng, nhưng có thể sử dụng các module như `cluster` hoặc `worker_threads` để triển khai đa luồng.

7. NPM là gì?
   - NPM (Node Package Manager) là công cụ quản lý gói cho Node.js, cho phép cài đặt và quản lý các thư viện và công cụ phát triển.

8. REPL trong Node.js là gì?
   - REPL (Read-Eval-Print Loop) là môi trường tương tác cho phép thử nghiệm và chạy mã JavaScript trực tiếp.

9. EventEmitter trong Node.js là gì?
   - EventEmitter là lớp trong Node.js cho phép tạo và quản lý các sự kiện, giúp ứng dụng phản hồi với các sự kiện cụ thể.

10. Callback là gì trong Node.js?
    - Callback là hàm được truyền như đối số cho một hàm khác và được gọi khi tác vụ hoàn thành, thường được sử dụng trong các thao tác không đồng bộ.

### Thực hành và công cụ

1. Express.js là gì?
   - Express.js là framework web cho Node.js, giúp xây dựng các ứng dụng web và API nhanh chóng và dễ dàng.

2. Sự khác biệt giữa `require` và `import` trong Node.js là gì?
   - `require` là cú pháp của CommonJS, trong khi `import` là cú pháp của ES6 Modules.

3. Cách xử lý lỗi trong Node.js?
   - Sử dụng các callback với đối số lỗi đầu tiên hoặc sử dụng `try-catch` trong các hàm bất đồng bộ với `async/await`.

4. Cách quản lý phiên bản của các gói trong Node.js?
   - Sử dụng `package.json` để quản lý các phụ thuộc và phiên bản của chúng.

5. Cách tối ưu hóa hiệu suất ứng dụng Node.js?
   - Sử dụng caching, tối ưu hóa các thao tác I/O, và sử dụng các công cụ như PM2 để quản lý tiến trình.

6. Cách bảo mật ứng dụng Node.js?
   - Sử dụng HTTPS, xác thực và phân quyền người dùng, và tránh các lỗ hổng bảo mật như SQL Injection.

7. Sự khác biệt giữa `fs.readFileSync` và `fs.readFile` là gì?
   - `fs.readFileSync` là phương thức đồng bộ, chặn luồng chính cho đến khi hoàn thành, trong khi `fs.readFile` là phương thức bất đồng bộ, không chặn luồng chính.

8. Cách sử dụng middleware trong Express.js?
   - Middleware là các hàm được gọi trong quá trình xử lý yêu cầu, có thể dùng để xử lý xác thực, logging, hoặc xử lý lỗi.

9. Cách triển khai ứng dụng Node.js lên môi trường sản xuất?
   - Sử dụng các dịch vụ như Heroku, AWS, hoặc DigitalOcean, và đảm bảo cấu hình môi trường phù hợp.

10. Cách sử dụng các module bên ngoài trong Node.js?
    - Sử dụng NPM để cài đặt và quản lý các gói, sau đó `require` chúng trong mã nguồn.

### Kiến thức nâng cao

1. Event loop trong Node.js hoạt động như thế nào?
   - Event loop quản lý các tác vụ không đồng bộ, cho phép Node.js xử lý nhiều yêu cầu mà không bị chặn.

2. Sự khác biệt giữa `process.nextTick`, `setImmediate`, và `setTimeout` là gì?
   - `process.nextTick` được gọi trước bất kỳ sự kiện I/O nào, `setImmediate` được gọi sau khi tất cả các sự kiện I/O đã được xử lý, và `setTimeout` được gọi sau một khoảng thời gian nhất định.

3. Cách sử dụng cluster module trong Node.js?
   - Sử dụng module `cluster` để tạo các tiến trình con, giúp tận dụng đa nhân CPU và tăng hiệu suất ứng dụng.

4. Cách sử dụng worker_threads trong Node.js?
   - Sử dụng module `worker_threads` để tạo các luồng con, cho phép thực hiện các tác vụ CPU-intensive mà không chặn event loop.

5. Cách sử dụng streams trong Node.js?
   - Streams cho phép xử lý dữ liệu lớn một cách hiệu quả, bao gồm Readable, Writable, Duplex, và Transform streams.

6. Cách sử dụng child_process trong Node.js?
   - Sử dụng module `child_process` để tạo và quản lý các tiến trình con, cho phép thực thi các lệnh hệ thống hoặc các ứng dụng khác.

7. Cách sử dụng buffer trong Node.js?
   - Buffer là đối tượng dùng để xử lý dữ liệu nhị phân, đặc biệt hữu ích khi làm việc với
