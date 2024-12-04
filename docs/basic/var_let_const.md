### Sự khác biệt giữa `let`, `const`, và `var` trong JavaScript:

1. **`var`**:
   - **Phạm vi (Scope):** Toàn cục (global) hoặc phạm vi hàm.
   - **Hoisting:** Được nâng lên đầu phạm vi nhưng chưa được khởi tạo (giá trị ban đầu là `undefined`).
   - **Khả năng thay đổi:** Có thể gán lại giá trị.

2. **`let`**:
   - **Phạm vi (Scope):** Phạm vi khối (`{}`), không thoát ra ngoài block.
   - **Hoisting:** Chỉ được nâng lên đầu block nhưng không khởi tạo (gây lỗi nếu dùng trước khi khai báo).
   - **Khả năng thay đổi:** Có thể gán lại giá trị.

3. **`const`**:
   - **Phạm vi (Scope):** Phạm vi khối (`{}`).
   - **Hoisting:** Tương tự `let`, không thể sử dụng trước khi khai báo.
   - **Khả năng thay đổi:** Không thể gán lại giá trị, nhưng có thể thay đổi thuộc tính nếu là object hoặc array.

---

### Khi nào dùng:
- **`var`:** Hạn chế dùng do dễ gây lỗi.
- **`let`:** Dùng khi giá trị thay đổi trong suốt chương trình.
- **`const`:** Dùng cho hằng số hoặc giá trị không thay đổi. 

### Ví dụ:
```javascript
// var
var x = 10;
if (true) {
  var x = 20; // Thay đổi cả bên ngoài
}
console.log(x); // 20

// let
let y = 10;
if (true) {
  let y = 20; // Chỉ trong block
}
console.log(y); // 10

// const
const z = 10;
z = 20; // Error: Assignment to constant variable
const arr = [1, 2, 3];
arr.push(4); // Được phép
console.log(arr); // [1, 2, 3, 4]
```
