# Các Hàm trong Solidity

### Giới Thiệu

Bây giờ khi chúng ta đã thiết lập một hợp đồng với một số biến trạng thái, hãy cùng tìm hiểu cách sử dụng các hàm để tương tác với chúng.

### Định Nghĩa Hàm

Trước khi chúng ta có thể sử dụng một hàm trong `SimpleContract`, chúng ta cần phải định nghĩa nó. Trong Solidity, các hàm được định nghĩa bằng từ khóa `function`, theo sau là tên hàm độc đáo, một danh sách tham số tùy chọn và một khối câu lệnh được bao trong dấu ngoặc nhọn. Cú pháp cơ bản là:

```solidity
function functionName(int arg1, string memory arg2, ...) visibility stateMutability returns() {
   // Logic đi vào đây :)
}
```

### Tên Hàm

Đoạn mã này khai báo hàm với tên độc đáo (`functionName`), đây là cách bạn sẽ gọi hàm đó.

### Tham Số

Phần này chỉ ra tham số của hàm, trong đó `arg1` là một số nguyên và `arg2` là một chuỗi được lưu trữ trong bộ nhớ; các tham số bổ sung có thể được thêm vào khi cần.

### Quyền Truy Cập

Điều này xác định mức độ truy cập của hàm, chẳng hạn như `public`, `private`, hoặc `internal`, quyết định ai có thể gọi hàm.

### Tính Chất Biến Trạng Thái

> ⚠️**Lưu ý:** Chúng ta sẽ tìm hiểu về khái niệm phạm vi (scope) trong tài nguyên tiếp theo!

Điều này chỉ ra liệu hàm có thể sửa đổi trạng thái của hợp đồng hay không (ví dụ: `pure`, `view`, hoặc `nonpayable`), ảnh hưởng đến cách nó tương tác với blockchain.

### Kiểu Trả Về

Điều này chỉ ra kiểu trả về của hàm, xác định giá trị mà hàm sẽ trả khi được gọi; dấu ngoặc đơn có thể chứa kiểu trả về nếu hàm trả về một giá trị.

Ví dụ, `returns(uint)` có nghĩa là hàm sẽ trả về một số nguyên không dấu.

```solidity
function getValue() public view returns(uint) {
	return 1;
}
```

### Nhiệm Vụ 📝

Thêm hàm sau vào `SimpleContract` để cho phép người dùng thiết lập biến trạng thái `name`:

```solidity
function set(string memory _name) public;
```

Hàm này nhận một tham số chuỗi `_name` và cập nhật biến `name` trong hợp đồng.