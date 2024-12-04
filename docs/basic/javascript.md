# Array, Object và Reference Types trong JavaScript:

1. Array:
   - Là kiểu dữ liệu dùng để lưu danh sách các phần tử.
   - Các phần tử có thể thuộc nhiều kiểu dữ liệu khác nhau.
   - Ví dụ:
     ```javascript
     const arr = [1, 'text', true];
     ```

2. Object:
   - Là kiểu dữ liệu lưu trữ theo cặp `key: value`.
   - Dùng để biểu diễn các cấu trúc phức tạp hơn.
   - Ví dụ:
     ```javascript
     const obj = { name: 'Alice', age: 25 };
     ```

3. Reference Types:
   - Array và Object thuộc kiểu tham chiếu (reference types).
   - Khi gán hoặc truyền, chỉ địa chỉ trong bộ nhớ được sao chép, không phải giá trị thực.
   - Ví dụ:
     ```javascript
     const obj1 = { a: 1 };
     const obj2 = obj1; // obj2 tham chiếu cùng vùng nhớ với obj1
     obj2.a = 2;
     console.log(obj1.a); // Kết quả: 2
     ``` 

4. Lưu ý:

- Sử dụng `spread operator` hoặc `Object.assign` để sao chép đối tượng thay vì gán tham chiếu.
  > Lý do: Cả hai cách đều tạo ra một bản sao mới, tránh việc thay đổi dữ liệu gốc.

  a. Spread Operator:

    ```javascript
    const obj1 = { a: 1, b: 2 };
    const obj2 = { ...obj1 }; // Sao chép obj1
    obj2.a = 10;
    console.log(obj1.a); // Kết quả: 1 (Không bị thay đổi)
    ```

  b. Object.assign:

    ```javascript
    const obj1 = { a: 1, b: 2 };
    const obj2 = Object.assign({}, obj1); // Sao chép obj1
    obj2.a = 10;
    console.log(obj1.a); // Kết quả: 1 (Không bị thay đổi)
    ```

# Spread Operator (`...`)

- Dùng để mở rộng phần tử của một mảng hoặc object.  
- Ví dụ:
  ```javascript
  const arr = [1, 2, 3];
  const newArr = [...arr, 4, 5]; // [1, 2, 3, 4, 5]
  const obj = { a: 1, b: 2 };
  const newObj = { ...obj, c: 3 }; // { a: 1, b: 2, c: 3 }
  ```

# Rest Operator (`...`)

- Dùng để gom nhóm các phần tử còn lại vào một mảng hoặc object.  
- Ví dụ:
  ```javascript
  const [first, ...rest] = [1, 2, 3, 4]; // first = 1, rest = [2, 3, 4]
  const { a, ...others } = { a: 1, b: 2, c: 3 }; // others = { b: 2, c: 3 }
  ``` 

# Destructuring

- Định nghĩa: Một cách trích xuất các giá trị từ mảng hoặc thuộc tính từ object và gán chúng vào các biến riêng biệt.
- Cú pháp:
  - Mảng:  
    ```javascript
    const [a, b] = [1, 2]; // a = 1, b = 2
    ```
  - Object:  
    ```javascript
    const { name, age } = { name: 'Alice', age: 25 }; // name = 'Alice', age = 25
    ```

# Async Code & Promises

## Async Code:
- JavaScript chạy đơn luồng (single-threaded), nhưng với async code, các tác vụ (như I/O, API call) được xử lý không đồng bộ để tránh chặn luồng chính.
- Ví dụ:
  ```javascript
  setTimeout(() => console.log("Hello"), 1000); // Chạy sau 1 giây, không chặn mã khác.
  ```

## Promises:
- Là cách quản lý async code hiện đại, đại diện cho một giá trị trong tương lai (hoàn thành hoặc thất bại).
- Trạng thái: `pending`, `fulfilled`, `rejected`.
- Ví dụ:
  ```javascript
  const promise = new Promise((resolve, reject) => {
    setTimeout(() => resolve("Done!"), 1000);
  });
  promise.then((res) => console.log(res)); // "Done!"
  ``` 

> Promises giúp code dễ đọc hơn so với callback.

## Callback
- Callback là một hàm được truyền như tham số vào hàm khác, để được thực thi sau khi hàm đó hoàn thành một nhiệm vụ cụ thể. Đây là cách phổ biến để xử lý các tác vụ không đồng bộ trong JavaScript.
- Ví dụ:
```javascript
function fetchData(callback) {
  setTimeout(() => {
    console.log("Dữ liệu đã được tải!");
    callback(); // Gọi hàm callback
  }, 1000);
}

function processData() {
  console.log("Xử lý dữ liệu...");
}

fetchData(processData); // Kết quả: Dữ liệu đã được tải! -> Xử lý dữ liệu...
```

> Callback giúp quản lý luồng thực thi, nhưng dễ gây "callback hell" nếu lồng quá nhiều hàm. Promises và `async/await` giải quyết vấn đề này.

# Template literals

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals

# JavaScript — Dynamic client-side scripting

https://developer.mozilla.org/en-US/docs/Learn/JavaScript
