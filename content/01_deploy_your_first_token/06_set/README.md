# Tương Tác với Hợp Đồng Thông Minh

Đến phần cuối của việc triển khai hợp đồng đầu tiên, hãy cùng học cách tương tác với hợp đồng đã triển khai của bạn bằng cách sử dụng phương thức setter để cập nhật biến `name` 🔧

> Điều kiện tiên quyết: Đảm bảo bạn đã cài đặt MetaMask, kết nối với mạng EDU Chain Testnet, và hợp đồng `SimpleContract` của bạn đã được triển khai thành công.

### Tương Tác với Hợp Đồng

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract.png)

Giờ hợp đồng `SimpleContract` của bạn đã được triển khai trên mạng EDU Chain Testnet, hãy sử dụng phương thức `set` để cập nhật biến `name` thành `Vitalik` và lấy mã giao dịch để xác minh giao dịch.

### ❗Nhiệm vụ: Gọi phương thức `set`

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_set.png)

Bạn có thể nhấp vào phương thức `set` trong giao diện hợp đồng của mình. Vì hợp đồng có một đối số, bạn sẽ nhập tên vào đó. Nhập giá trị **Vitalik** và nhấp *Send*. Điều này sẽ yêu cầu bạn xác nhận giao dịch và cho phép bạn phê duyệt nó.

### Tương Tác với Trạng Thái Hợp Đồng

![](https://raw.githubusercontent.com/POLearn/pol-template/refs/heads/master/content/assets/images/contract_name.png)

Khi giao dịch đã được xác nhận, hãy gọi hàm `name` trong hợp đồng của bạn để kiểm tra giá trị hiện tại của nó. Nếu trả về `Vitalik`, chúc mừng bạn! Bạn đã thành công trong việc tương tác với hợp đồng và cập nhật trạng thái của nó. 🎉

Bạn có thể gửi giao dịch phương thức `set` lên nền tảng Proof of Learn (POL) cho nhiệm vụ này. Điều này xác nhận rằng bạn đã thành công trong việc tương tác với hợp đồng thông minh trên EDU Chain.