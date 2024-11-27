# Cài Đặt Hợp Đồng Thông Minh

### Giới Thiệu

Trong phần này, chúng ta sẽ đi qua cấu trúc cơ bản của một hợp đồng thông minh, giúp tự động hóa các thỏa thuận và giao dịch trên blockchain, mở ra con đường cho các ứng dụng phi tập trung (DApps) sáng tạo!

### Chỉ Dẫn Giấy Phép

```solidity
// SPDX-License-Identifier: MIT
```

Thông thường, dòng đầu tiên là **Chỉ Dẫn Giấy Phép**, điều này là tùy chọn nhưng rất tốt để sử dụng. Bằng cách sử dụng giấy phép MIT, chúng ta khuyến khích người khác tự do sử dụng và sửa đổi hợp đồng thông minh của chúng ta, đồng thời làm rõ các quyền pháp lý liên quan, thúc đẩy sự hợp tác trong cộng đồng blockchain.

### Chỉ Dẫn Pragma

**Chỉ Dẫn Pragma** xác định phiên bản biên dịch Solidity cần sử dụng:

```solidity
pragma solidity ^0.8.20;
```

Trong trường hợp này, `^0.8.20` đảm bảo hợp đồng được biên dịch bằng phiên bản 0.8.20 hoặc các phiên bản mới hơn không gây ra các thay đổi làm hỏng mã nguồn. Điều này giúp duy trì tính tương thích và đảm bảo hợp đồng hoạt động như mong đợi.

### Khai Báo Hợp Đồng

Đoạn mã này định nghĩa một hợp đồng thông minh cơ bản có tên `SimpleContract`. Từ khóa `contract` được sử dụng để khai báo một hợp đồng mới trong Solidity, đóng vai trò như một khuôn mẫu để tạo các bản sao của hợp đồng đó trên blockchain.

Bên trong dấu ngoặc nhọn `{}`, là nơi chứa tất cả logic và chức năng của hợp đồng. Điều này có thể bao gồm các biến trạng thái, hàm, và các yếu tố khác cần thiết để xác định hành vi của hợp đồng.

```solidity
contract SimpleContract { 
	// Tất cả logic sẽ được viết ở đây :) 
}
```

### Biên Dịch Hợp Đồng

Để biên dịch hợp đồng thông minh của bạn, việc chọn đúng phiên bản trình biên dịch Solidity phù hợp với chỉ dẫn pragma là rất quan trọng, ví dụ như `pragma solidity ^0.8.20;`. Việc chọn phiên bản tương thích, như **0.8.20** hoặc phiên bản mới hơn, đảm bảo biên dịch thành công và tạo ra:

-   🛠️ **Bytecode** để triển khai trên blockchain
-   📡 **Interface Nhị Phân Ứng Dụng (ABI)** để tương tác với các hàm và sự kiện của hợp đồng

Tóm lại, việc sử dụng phiên bản trình biên dịch đúng là điều cần thiết để triển khai và đảm bảo chức năng của hợp đồng thông minh.