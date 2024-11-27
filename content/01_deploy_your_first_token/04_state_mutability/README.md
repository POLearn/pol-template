# Tính Tương Thích Trạng Thái (State Mutability)

### Giới Thiệu

Tính tương thích trạng thái trong Solidity chỉ ra cách mà một hàm tương tác với trạng thái của hợp đồng và blockchain. Hiểu rõ về tính tương thích trạng thái là rất quan trọng để tối ưu hóa việc sử dụng gas và đảm bảo các hàm hoạt động như mong muốn.

Có ba loại tính tương thích trạng thái chính trong Solidity: `pure`, `view`, và `nonpayable`.

### Pure

Hàm `pure` chỉ ra rằng hàm đó không đọc hoặc sửa đổi trạng thái của hợp đồng. Nó chỉ dựa vào các tham số đầu vào của mình và thường được sử dụng cho các phép toán tính toán.

```solidity
function add(uint a, uint b) public pure returns (uint) {
    return a + b;
}
```

### View

Hàm `view` cho phép đọc trạng thái của hợp đồng nhưng không cho phép sửa đổi bất kỳ thứ gì. Nó có thể được sử dụng để truy xuất dữ liệu được lưu trữ trong hợp đồng mà không thay đổi chúng.

```solidity
function getBalance() public view returns (uint) {
    return balance;
}
```

### Nonpayable

Hàm `nonpayable` có thể sửa đổi trạng thái của hợp đồng và cho phép nhận Ether, nhưng không chấp nhận Ether trong suốt cuộc gọi hàm. Đây là tính tương thích trạng thái mặc định nếu không có tính tương thích nào được chỉ định.

```solidity
function setBalance(uint _balance) public {
    balance = _balance;
}
```

### Tóm Tắt

Bằng cách sử dụng tính tương thích trạng thái phù hợp cho các hàm của bạn, bạn có thể đảm bảo rõ ràng về cách thức hoạt động của chúng và tối ưu hóa chi phí gas cho các tương tác của hợp đồng.