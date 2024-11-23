### 1. Create Administrative Report
**Brief Description** <br>
Trường hợp sử dụng này cho phép Payroll Administrator tạo một báo cáo "Tổng số giờ làm việc" hoặc "Trả lương đến nay". <br>
**Flow of Events** <br>
**Basic Flow** <br>
Trường hợp sử dụng bắt đầu khi Payroll Administrator yêu cầu hệ thống tạo báo cáo quản trị. <br>
1. Hệ thống yêu cầu Payroll Administrator chỉ định các tiêu chí báo cáo sau: <br>
Loại báo cáo (tổng số giờ làm việc hoặc trả lương đến nay), <br>
Ngày bắt đầu và ngày kết thúc cho báo cáo, <br>
Tên nhân viên. <br>
2. Khi Payroll Administrator cung cấp thông tin được yêu cầu, hệ thống sẽ cung cấp cho Payroll Administrator một báo cáo đáp ứng các tiêu chí báo cáo. <br>
3. Payroll Administrator sau đó có thể yêu cầu hệ thống lưu báo cáo. Tại thời điểm đó, hệ thống yêu cầu Payroll Administrator cung cấp tên và vị trí để lưu báo cáo. <br>
4. Khi Payroll Administrator cung cấp thông tin được yêu cầu và xác nhận quyết định lưu báo cáo, hệ thống sẽ lưu báo cáo vào tên và vị trí đã chỉ định. <br>
5. Nếu Payroll Administrator không chọn lưu báo cáo, báo cáo sẽ bị hủy. <br>

**Alternative Flows** <br>
&nbsp; &nbsp; **Requested Information Unavailable** <br>
&nbsp; &nbsp; Nếu trong Luồng cơ bản, thông tin được yêu cầu không có sẵn, hệ thống sẽ hiển thị thông báo lỗi. Payroll Administrator có thể chọn quay lại đầu Luồng cơ bản hoặc hủy thao tác, tại thời điểm đó trường hợp sử dụng kết thúc. <br>
&nbsp; &nbsp; **Invalid Format or Insufficient Information** <br>
&nbsp; &nbsp; Nếu trong Luồng cơ bản, Payroll Administrator chưa chỉ định đủ thông tin để tạo báo cáo đã chọn, hệ thống sẽ nhắc tác nhân về thông tin bị thiếu. Payroll Administrator có thể nhập thông tin bị thiếu hoặc chọn hủy thao tác, tại thời điểm đó trường hợp sử dụng kết thúc. <br>
**Special Requirements** <br>
Không có. <br>
**Pre-Conditions** <br>
Payroll Administrator phải đăng nhập vào hệ thống để trường hợp sử dụng này bắt đầu. <br>
**Post-Conditions** <br>
Trạng thái hệ thống không thay đổi bởi trường hợp sử dụng này. <br>
**Extension Points** <br>
Không có. <br>

### 2. Login
**Brief Description** <br>
Trường hợp sử dụng này mô tả cách một người dùng đăng nhập vào hệ thống Payroll. <br>
**Flow of Events** <br>
**Basic Flow** <br>
1. Trường hợp sử dụng bắt đầu khi actor muốn đăng nhập vào hệ thống Payroll.
2. Actor nhập tên và mật khẩu.
3. Hệ thống xác thực tên và mật khẩu đã nhập và đăng nhập actor vào hệ thống.
   
**Alternative Flows** <br>
&nbsp; &nbsp; Invalid Name/Password <br>
&nbsp; &nbsp; Nếu trong Luồng cơ bản, actor nhập tên và/hoặc mật khẩu không hợp lệ, hệ thống sẽ hiển thị thông báo lỗi. Actor có thể chọn quay lại đầu Luồng cơ bản hoặc hủy đăng nhập, lúc đó trường hợp sử dụng sẽ kết thúc. <br>
**Special Requirements** <br>
Không có. <br>
**Pre-Conditions** <br>
Hệ thống đang ở trạng thái đăng nhập và hiển thị màn hình đăng nhập. <br>
**Post-Conditions** <br>
Nếu trường hợp sử dụng thành công, actor sẽ được đăng nhập vào hệ thống. Nếu không, trạng thái hệ thống không thay đổi. <br>
**Extension Points** <br>
Không có. <br>

### 3. Run Payroll
**Brief Description** <br>
Trường hợp sử dụng này mô tả cách chạy bảng lương mỗi Thứ Sáu và ngày làm việc cuối cùng của tháng. <br>
**Flow of Events** <br>
**Basic Flow** <br>
1. Trường hợp sử dụng bắt đầu khi đến thời gian chạy bảng lương. Bảng lương được chạy tự động vào mỗi Thứ Sáu và ngày làm việc cuối cùng của tháng. <br>
2. Hệ thống truy xuất tất cả nhân viên cần được trả lương vào ngày hiện tại. <br>
3. Hệ thống tính toán tiền lương sử dụng các bảng chấm công, đơn đặt hàng, thông tin nhân viên (ví dụ: lương, phúc lợi, v.v.) và tất cả các khoản khấu trừ hợp pháp. <br>
4. Nếu phương thức nhận lương là qua thư hoặc nhận trực tiếp, hệ thống sẽ in séc lương. <br>
5. Nếu phương thức nhận lương là chuyển khoản trực tiếp, hệ thống sẽ tạo giao dịch ngân hàng và gửi nó đến hệ thống ngân hàng để xử lý. <br>
6. Trường hợp sử dụng kết thúc khi tất cả nhân viên nhận lương cho ngày mong muốn đã được xử lý. <br>
   
**Alternative Flows** <br>
&nbsp; &nbsp; **Bank System Unavailable** <br>
&nbsp; &nbsp; Nếu hệ thống ngân hàng không hoạt động, hệ thống sẽ cố gắng gửi lại giao dịch ngân hàng sau một khoảng thời gian nhất định. Hệ thống sẽ tiếp tục cố gắng gửi lại cho đến khi hệ thống ngân hàng hoạt động trở lại. <br>
&nbsp; &nbsp; **Deleted Employees** <br>
&nbsp; &nbsp; Sau khi bảng lương của một nhân viên được xử lý, nếu nhân viên đó đã được đánh dấu để xóa (xem trường hợp sử dụng "Maintain Employee"), hệ thống sẽ xóa nhân viên đó. <br>
**Special Requirements** <br>
Không có. <br>
**Pre-Conditions** <br>
Không có. <br>
**Post-Conditions** <br>
Các khoản thanh toán cho từng nhân viên đủ điều kiện được trả vào ngày hiện tại đã được xử lý. <br>
**Extension Points** <br>
Không có. <br>
