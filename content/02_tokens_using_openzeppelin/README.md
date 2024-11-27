# Cấp Độ Tiếp Theo: Triển Khai Token ERC20

Bây giờ bạn đã thành công trong việc triển khai và tương tác với smart contract đầu tiên, đã đến lúc nâng cấp! Trong phần này, chúng ta sẽ hướng dẫn bạn triển khai token ERC20 của riêng bạn, sử dụng việc triển khai ERC20 🪙 đã được kiểm chứng của OpenZeppelin. Hãy bắt đầu tạo token của bạn trên mạng Open Campus Codex!

### OpenZeppelin là gì?

OpenZeppelin là một thư viện phát triển smart contract an toàn. Nó cung cấp các triển khai của các tiêu chuẩn token phổ biến, bao gồm ERC20, mà bạn có thể sử dụng để tạo token của riêng mình mà không cần phải làm lại từ đầu. Sử dụng các triển khai của OpenZeppelin đảm bảo rằng token của bạn tuân thủ các thực tiễn và tiêu chuẩn tốt nhất trong hệ sinh thái Ethereum.

Từ việc hiểu cấu trúc cơ bản của hợp đồng, chúng ta sẽ tạo ra một token `SampleERCToken`.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SampleERCToken {
}
```

### Nhập OpenZeppelin ERC20

Trong file `TokenPoken.sol` của bạn, bắt đầu bằng việc nhập triển khai ERC20 của OpenZeppelin với câu lệnh sau:

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

Điều này cho phép bạn kế thừa hợp đồng ERC20 và xây dựng token của mình dựa trên đó. OpenZeppelin cung cấp một nền tảng an toàn và đã được kiểm chứng cho các token ERC20.

### Viết Hợp Đồng Token

Tiếp theo, hãy định nghĩa token ERC20 của bạn bằng cách viết mã hợp đồng. Sử dụng tên "TokenPoken" và ký hiệu "TP" làm đối số cho constructor ERC20. Đảm bảo rằng constructor là rỗng, chỉ gọi constructor `ERC20`:

Để biết thêm chi tiết về hợp đồng ERC20, hãy tham khảo [tài liệu của OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/erc20) để hiểu các tính năng và chức năng của nó.

Dưới đây là mã bắt đầu:

```solidity
contract SampleERCToken is ERC20 { 
	// ...
}
```

Mã này định nghĩa cấu trúc cơ bản của token của bạn, sử dụng hợp đồng của OpenZeppelin để đảm bảo an toàn và dễ dàng.

### Biên Dịch Hợp Đồng

Để biên dịch, mở IDE Solidity của bạn và chọn phiên bản biên dịch **0.8.23**. Nhấn "Compile" để đảm bảo không có lỗi, và một dấu tích màu xanh lá cây sẽ xác nhận biên dịch thành công.

### Triển Khai Hợp Đồng

Nếu bạn đang sử dụng Solide IDE, trong **Tab Build & Deploy**, chọn `SampleERCToken` và nhấn **Deploy**.

### Kiểm Tra Token

Sau khi hợp đồng `TokenPoken` của bạn được triển khai, bạn có thể tương tác với các hàm ERC20 đã kế thừa. Dưới đây là một số hành động để thử:

- 🧮 **Kiểm tra Tổng Cung:** Gọi `totalSupply` để xem tổng số token TokenPoken.
- 👛 **Kiểm tra Số Dư của Bạn:** Sử dụng `balanceOf` với địa chỉ của bạn để xem số dư token của bạn.
- 🔄 **Chuyển Token:** Thử sử dụng hàm `transfer` để gửi token đến ví khác.

### ❗ Nộp Giao Dịch lên Proof of Learn

Nếu bạn đã triển khai `SimpleContract` trước đó, bạn có thể làm điều tương tự với `SampleERCToken`. Chúc mừng! Bạn đã thành công trong việc tạo và triển khai token ERC20 của riêng mình có tên là TokenPoken với ký hiệu TP, sử dụng hợp đồng ERC20 của OpenZeppelin. Bài tập này chứng minh sức mạnh và sự dễ dàng khi sử dụng OpenZeppelin để phát triển smart contract an toàn và chuẩn hóa.

Hãy chắc chắn nhận **FREE POL POAP** từ Proof of Learn, chứng nhận bạn đã triển khai và tương tác với smart contract trên Open Campus Codex! 🎉🎉🎉