# Tương tác với một Smart Contract

### Giới thiệu

Trong phần cuối cùng của việc triển khai hợp đồng đầu tiên, chúng ta sẽ học cách tương tác với hợp đồng đã triển khai của bạn, sử dụng phương thức setter để cập nhật biến `name` 🔧

> Yêu cầu: Đảm bảo bạn đã cài đặt MetaMask và kết nối với mạng Open Campus Codex, và hợp đồng **SimpleContract** của bạn đã được triển khai thành công.

### Tương tác với Hợp đồng

Bây giờ hợp đồng **SimpleContract** của bạn đã được triển khai trên mạng Open Campus Codex, hãy thay đổi biến `name` thành **Vitalik** sử dụng phương thức `set` và lấy hash giao dịch để xác nhận giao dịch.

#### Gọi Phương thức set

Đầu tiên, tìm phương thức `set` trong giao diện hợp đồng của bạn. Trong trường nhập liệu, gõ **Vitalik** và nhấn "Transact". MetaMask sẽ yêu cầu bạn xác nhận giao dịch—hãy chấp nhận giao dịch và đợi cho giao dịch được xử lý.

#### Xác minh Trạng thái Hợp đồng

Sau khi giao dịch được xác nhận, gọi phương thức `name` trong hợp đồng của bạn để kiểm tra giá trị hiện tại. Nếu nó trả về **Vitalik**, chúc mừng bạn! Bạn đã thành công trong việc tương tác với hợp đồng và cập nhật trạng thái của nó. 🎉

### ❗ Nộp Giao dịch lên Proof of Learn

Để xác nhận nhiệm vụ này, hãy nộp hash giao dịch lên nền tảng Proof of Learn (POL). Điều này xác nhận rằng bạn đã thành công trong việc tương tác với smart contract.