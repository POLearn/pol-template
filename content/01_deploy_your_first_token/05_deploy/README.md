# Triển khai Hợp Đồng Thông Minh

Sau khi đã nắm vững các kiến thức cơ bản về Solidity, bao gồm cấu trúc hợp đồng, các biến trạng thái, định nghĩa hàm và khả năng thay đổi trạng thái, giờ là lúc triển khai hợp đồng `SimpleContract`! 🚀

### Thêm Mạng EDU Chain vào MetaMask

Để triển khai hợp đồng của bạn lên mạng thử nghiệm EDU Chain, bạn cần thêm mạng tùy chỉnh vào MetaMask.

1. Mở MetaMask và nhấp vào danh sách thả xuống mạng ở trên cùng.
2. Chọn "Thêm Mạng" và điền vào các thông tin sau:

| **Trường**           | **Chi tiết**                                  |
|----------------------|-----------------------------------------------|
| **Tên Mạng**         | EDU Chain Testnet                            |
| **URL RPC Mới**      | `https://open-campus-codex-sepolia.drpc.org`  |
| **Chain ID**         | `656476`                                      |
| **Ký hiệu Tiền Tệ**  | `EDU`                                         |
| **URL Trình Duyệt Block**| `https://edu-chain-testnet.blockscout.com/`  |

Sau khi thêm các chi tiết này, bạn sẽ kết nối với mạng EDU Chain Testnet và sẵn sàng để triển khai hợp đồng! 🎉

### Cấu hình hợp đồng

Hãy tải mẫu hợp đồng của chúng ta. Mở hợp đồng này trong IDE mà bạn mong muốn. Lý tưởng nhất là bạn có thể sử dụng IDE tương tác của PoL. Cung cấp URL - `https://github.com/POLearn/pol-template/blob/master/contracts/SimpleContract.sol`.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_load.png)

```solidity
string public name;

function set(string memory _name) public {
    name = _name;
}
```

Chúng ta cùng xem hợp đồng này đang làm gì?

Hàm `set` sẽ là hàm setter cho phép người dùng cập nhật biến trạng thái `name` một cách động. Hàm này nhận một tham số duy nhất, `_name`, kiểu `string`, được cung cấp trong quá trình gọi hàm, và gán giá trị đó cho biến `name` lưu trữ trong hợp đồng. Điều này giúp hợp đồng trở nên tương tác hơn, khi nó cho phép cập nhật theo thời gian thực, chẳng hạn như đổi tên token hoặc tùy chỉnh dữ liệu hợp đồng dựa trên đầu vào của người dùng.

### Biên dịch hợp đồng

Đảm bảo rằng bạn đang sử dụng phiên bản biên dịch Solidity chính xác. Trong bài tập này, chúng ta sẽ sử dụng **0.8.23**. Việc sử dụng phiên bản đúng rất quan trọng, vì tính năng và cú pháp có thể thay đổi giữa các phiên bản.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_version.png)

### Triển khai hợp đồng

Khi hợp đồng đã được biên dịch, hãy triển khai hợp đồng `SimpleContract` lên mạng thử nghiệm EDU Chain mà chúng ta đã kết nối. MetaMask sẽ yêu cầu bạn xác nhận giao dịch triển khai.

Khi giao dịch được xác nhận, hợp đồng của bạn đã được triển khai thành công! Bạn đã cấu hình MetaMask cho mạng EDU Chain Testnet và triển khai hợp đồng thông minh. 🎉 Bạn cũng có thể kết nối với **EDU Chain Mainnet** với các cấu hình sau:

| **Trường**           | **Chi tiết**                                  |
|----------------------|-----------------------------------------------|
| **Tên Mạng**         | EDU Chain                                     |
| **URL RPC Mới**      | `https://rpc.edu-chain.raas.gelato.cloud`     |
| **Chain ID**         | `41923`                                       |
| **Ký hiệu Tiền Tệ**  | `EDU`                                         |
| **URL Trình Duyệt Block**| `https://edu-chain.blockscout.com/`          |

### ❗Nhiệm vụ: Gửi Hợp Đồng lên PoL

Để hoàn thành nhiệm vụ này trên POL, hãy gửi giao dịch triển khai hợp đồng của bạn lên nền tảng Proof of Learn (POL). Điều này xác nhận rằng bạn đã triển khai thành công hợp đồng. Bạn có thể nhận một 🏆**POL POAP**.

Giờ hợp đồng của bạn đã được triển khai, hãy chuẩn bị bước tiếp theo! Ở phần tiếp theo, chúng ta sẽ khám phá cách tương tác với hợp đồng đã triển khai, cập nhật biến `name` và thay đổi trạng thái của hợp đồng bằng các hàm của nó ⚡