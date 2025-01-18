# Triển khai Token ERC20

Với hiểu biết cơ bản về hợp đồng thông minh và cách sử dụng EDU Chain để tương tác và làm việc với chúng, đã đến lúc nâng cao kiến thức của bạn! Trong phần này, chúng ta sẽ hướng dẫn bạn cách triển khai **token ERC20** của riêng mình, sử dụng triển khai ERC20 đã được kiểm nghiệm của OpenZeppelin 🪙.

### OpenZeppelin là gì?

Trước khi đi sâu vào hợp đồng, chúng ta hãy hiểu về OpenZeppelin. OpenZeppelin là một thư viện phát triển hợp đồng thông minh an toàn. Nó cung cấp các triển khai cho các chuẩn token phổ biến, bao gồm ERC20, mà bạn có thể sử dụng để tạo token của riêng mình mà không phải tái phát minh lại bánh xe. Sử dụng các triển khai của OpenZeppelin đảm bảo rằng token của bạn tuân thủ các thực tiễn tốt nhất và các tiêu chuẩn trong hệ sinh thái Ethereum.

Sau khi hiểu cấu trúc cơ bản của hợp đồng, hãy tạo một `SampleERCToken`. Tải mẫu hợp đồng [tại đây](https://github.com/POLearn/pol-template/blob/master/contracts/SampleERCToken.sol) vào IDE bạn mong muốn.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_load.png)

Như chúng ta thấy, hợp đồng này là một hợp đồng trống. Tuy nhiên, đáng chú ý là có một import hợp đồng `ERC20` của OpenZeppelin. Hãy xem qua phần đó.

```solidity
import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
```

Điều này cho phép bạn kế thừa hợp đồng ERC20 và xây dựng token của bạn trên nền tảng đó. OpenZeppelin cung cấp một nền tảng an toàn, đã được kiểm nghiệm cho các token ERC20.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_setup.png)

Nếu chúng ta xem qua constructor, nó nhận vào hai tham số là `name` và `symbol`. Các mã còn lại là các triển khai cho việc minting và chuyển nhượng token ERC20, tất cả đã được hoàn thành cho bạn.

Hãy kế thừa điều này trong hợp đồng chính của chúng ta. Quay lại `SampleERCToken`. Đảm bảo rằng hợp đồng của bạn là `ERC20` như sau:

```solidity
contract SampleERCToken is ERC20
```

Trong constructor, chúng ta cũng đảm bảo gọi đến constructor của ERC20:

```solidity
constructor() ERC20("TokenName", "TOKEN") {
}
```

Chúng ta sẽ định nghĩa token ERC20 bằng cách viết mã hợp đồng. Sử dụng tên "TokenPoken" và biểu tượng "TP" làm tham số cho constructor của ERC20. Đảm bảo constructor là trống, chỉ gọi đến constructor `ERC20`:

Để biết thêm chi tiết về hợp đồng ERC20, tham khảo [tài liệu OpenZeppelin](https://docs.openzeppelin.com/contracts/4.x/erc20) để hiểu thêm về các tính năng và chức năng của nó.

### Biên dịch hợp đồng

Giống như hợp đồng trước, hãy đảm bảo bạn đang sử dụng đúng phiên bản trình biên dịch Solidity. Đối với bài tập này, chúng ta sẽ sử dụng **0.8.23**. Việc sử dụng đúng phiên bản là rất quan trọng, vì các tính năng và cú pháp có thể thay đổi giữa các phiên bản.

### Triển khai hợp đồng

Sau khi hợp đồng của bạn được biên dịch, hãy triển khai `SampleERCToken` lên EDU Chain testnet mà chúng ta đã kết nối. MetaMask sẽ yêu cầu bạn xác nhận giao dịch để triển khai hợp đồng.

### Kiểm tra Token của bạn

Khi hợp đồng `TokenPoken` của bạn đã được triển khai, bạn có thể tương tác với các hàm ERC20 được kế thừa. Dưới đây là một số hành động bạn có thể thử:

- 🧮 **Kiểm tra tổng cung:** Gọi `totalSupply` để xem tổng số token TokenPoken.
- 👛 **Kiểm tra số dư của bạn:** Sử dụng `balanceOf` với địa chỉ của bạn để xem số dư token của bạn.
- 🔄 **Chuyển token:** Thử hàm `name` để gửi token đến ví khác.

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/token_name.png)

### ❗Quest: Triển khai Token

Nếu bạn đã triển khai `SimpleContract` trước đó, bạn có thể làm điều tương tự cho `SampleERCToken`. Chúc mừng! Bạn đã thành công trong việc tạo và triển khai token ERC20 của riêng mình có tên là TokenPoken với biểu tượng TP sử dụng hợp đồng ERC20 của OpenZeppelin. Bài tập này thể hiện sức mạnh và sự dễ dàng khi sử dụng OpenZeppelin cho phát triển hợp đồng thông minh an toàn và chuẩn hóa.

Hãy chắc chắn yêu cầu **POL POAP** từ Proof of Learn, chứng minh rằng bạn đã triển khai và tương tác hợp đồng thông minh trên EDU Chain! 🎉🎉🎉