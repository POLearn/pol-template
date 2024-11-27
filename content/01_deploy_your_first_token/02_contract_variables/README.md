# Các Kiểu Dữ Liệu Cơ Bản trong Solidity

### Giới Thiệu

Hãy cùng khám phá các khối xây dựng cơ bản của hợp đồng thông minh bằng cách tìm hiểu về các biến cơ bản trong hợp đồng, chúng định nghĩa trạng thái và hành vi của hợp đồng!

Trong Solidity, các biến được xác định kiểu tĩnh, có nghĩa là bạn phải chỉ định kiểu dữ liệu khi khai báo, đảm bảo tính rõ ràng và cấu trúc cho các hợp đồng thông minh. Các biến này có thể nhận giá trị mặc định dựa trên kiểu dữ liệu của chúng, và Solidity cung cấp một loạt các kiểu dữ liệu cơ bản, từ số nguyên và Boolean cho đến địa chỉ và cấu trúc tùy chỉnh, giúp bạn mô hình hóa dữ liệu phức tạp một cách hiệu quả.

**Các Ví Dụ về Các Kiểu Dữ Liệu Solidity**

-   **uint**: Số nguyên không dấu
-   **int**: Số nguyên có dấu
-   **bool**: Giá trị Boolean
-   **address**: Địa chỉ Ethereum
-   **string**: Chuỗi văn bản
-   **bytes**: Mảng byte cố định kích thước
-   **struct**: Cấu trúc dữ liệu tùy chỉnh
-   **enum**: Kiểu dữ liệu do người dùng định nghĩa cho các giá trị liệt kê

### uint

Một số nguyên không dấu, có thể biểu diễn các số nguyên không âm, cho phép giá trị lớn hơn mà không gặp phải vấn đề về số âm.

  ```solidity
  uint256 count = 10; 
  ```

### int

Một số nguyên có dấu, có thể biểu diễn cả số dương và số âm, hữu ích cho các phép tính yêu cầu một phạm vi giá trị.

  ```solidity
  int256 balance = -50; 
  ```

### bool

Giá trị Boolean có thể là `true` hoặc `false`, thường được sử dụng trong các câu lệnh điều kiện và cờ hiệu.

  ```solidity
  bool isActive = true; 
  ```

### address

Kiểu dữ liệu đại diện cho một địa chỉ Ethereum, rất quan trọng để xác định các tài khoản và hợp đồng thông minh trên blockchain.

  ```solidity
  address owner = 0x1234567890abcdef1234567890abcdef12345678; 
  ```

### string

Một chuỗi ký tự động, được sử dụng để lưu trữ văn bản, cho phép dữ liệu chuỗi có độ dài linh hoạt và thay đổi.

```solidity
  string greeting = "Hello, blockchain!"; 
  ```

### bytes

Một mảng byte có kích thước cố định được sử dụng để lưu trữ dữ liệu nhị phân thô, cung cấp cách quản lý dữ liệu ở cấp độ byte một cách hiệu quả.

```solidity
  bytes32 data = 0xabcdefabcdefabcdefabcdefabcdefabcdefabcdef; 
  ```

> 👀 Solidity cung cấp nhiều kiểu biến cơ bản, mỗi kiểu có giá trị mặc định riêng: **`uint`** (số nguyên không dấu) mặc định là `0`, **`int`** (số nguyên có dấu) cũng mặc định là `0`, **`bool`** (Boolean) mặc định là `false`, **`address`** khởi tạo là địa chỉ không có giá trị (`0x0000000000000000000000000000000000000000`), **`string`** mặc định là chuỗi rỗng (`""`), và **`bytes`** mặc định là mảng byte rỗng. Ví dụ:

```solidity
uint256 count;        // Mặc định: 0
int256 balance;       // Mặc định: 0
bool isActive;        // Mặc định: false
address owner;        // Mặc định: 0x000...
string greeting;      // Mặc định: ""
bytes32 data;         // Mặc định: ""
```

### Nhiệm Vụ 📝

Với hợp đồng `SimpleContract` đã được biên dịch, hãy thêm một biến chuỗi công khai có tên là `name` mà bất kỳ ai cũng có thể truy cập:

```solidity
string public name; // Biến này sẽ lưu trữ tên
```