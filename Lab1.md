1. Phân tích kiến trúc <br>
  1.1. Đề xuất kiến trúc mô hình MVC (Modal - View - Controller) <br>
  1.2. Lý do lựa chọn: Các phần Model, View và Controller được tách ra độc lập, giúp cho việc kiểm soát và khắc phục lỗi dễ dàng hơn. <br>
  1.3. Ý nghĩa từng thành phần: <br>
   * Model: Là bộ phận có chức năng lưu trữ toàn bộ dữ liệu của ứng dụng, là cầu nối giữa 2 thành phần là View và Controller. Các mô hình là dữ liệu được sử dụng bởi các chương trình. Đây có thể là một cơ sở dữ liệu hoặc một tệp XML thuần túy hoặc một đối tượng đơn giản. <br>
   * View: Đây là giao diện người dùng (theme). View là cách hiển thị trong một ứng dụng. Nó bao gồm mọi thứ mà người dùng có thể nhìn thấy. <br>
   * Controller: Là bộ phận chịu trách nhiệm xử lý các yêu cầu của người dùng thực hiện thông qua View. Controller bao gồm Model và View. Nó nhận đầu vào và thực hiện cập nhật tương ứng. <br>
  1.4. ![Package Diagram](https://www.planttext.com/api/plantuml/png/R55RRW8n3FptANo1lG5QKK6H-e644Es_kx5GIXuhnrM5gfwi7no9ApHPO0cKlsHcCZDsZh-7QL8I_VGE8EriG8c90TIgOrnHjwCj9snmvYWbd5lQ2dc0_iJWc-Kld4mM6UIsnMz0x0Rbi-zTt3E_lepGYlOIdNioteOC_rnTPZ5eeLYorvexlR4wlxkA_eKyeDRSHz6AgEAMqR0hhQCpB0zhZy36Ukv8p7sRkw3QVavAxvGu9roEj_D8_CWpBYbajUUW5rKn6HRQD6sr4wZMKvYXFfo6AFVnEKmvcFoJVm000F__0m00) <br>
2. Cơ chế phân tích <br>
   * Persistency: Hệ thống cần lưu trữ thông tin về nhân viên và các bảng chấm công, hóa đơn mua hàng, báo cáo, phương thức thanh toán, v.v., để có thể truy cập và cập nhật dữ liệu một cách đáng tin cậy. Tính bền vững giúp duy trì dữ liệu lâu dài, bảo đảm rằng dữ liệu của nhân viên không bị mất sau khi hệ thống ngừng hoạt động và đảm bảo rằng các bản ghi lương luôn sẵn sàng khi cần. <br>
   * Legacy Interface: Hệ thống mới cần tích hợp và truy xuất thông tin từ cơ sở dữ liệu quản lý dự án cũ (DB2) trên mainframe IBM mà không làm thay đổi cơ sở dữ liệu hiện tại. Vì lý do chi phí, Acme muốn tận dụng lại hệ thống cũ mà không phải thay thế nó, vì vậy cần một giao diện giúp hệ thống mới tương tác mà không gây ảnh hưởng đến dữ liệu cũ. <br>
   * Security: Hệ thống phải đảm bảo rằng chỉ nhân viên có quyền mới có thể xem và chỉnh sửa dữ liệu cá nhân của họ. Ngoài ra, cần ngăn chặn truy cập trái phép để bảo vệ thông tin nhạy cảm về nhân viên và tiền lương. Bảo mật giúp duy trì quyền riêng tư, tuân thủ các yêu cầu bảo mật nội bộ và tránh các rủi ro về truy cập trái phép. <br>
3. Phân tích ca sử dụng Payment <br>
   3.1. Các lớp phân tích: <br>
     * Boundary: PaymentForm, ProjectManagementDatabase <br>
     * Control: PaymentController <br>
     * Entity: Employee <br>
   3.2. Nhiệm vụ của từng lớp phân tích: <br>
     * PaymentForm: Hiển thị UI và các trường input để người dùng nhập <br>
     * ProjectManagementDatabase: Truy xuất thông tin theo payment method hiện tại để hiển thị lên UI <br>
     * PaymentController: Xử lí các request payment <br>
     * Employee: Đại diện cho employee, chứa các thông tin và phương thức liên quan đến employee <br>
   3.3. ![Class Diagram](https://www.planttext.com/api/plantuml/png/T5FBJkDG3DtdAxm4YKgiArHHaeuKCOMAnnevYSdSwNraxdMG2kBBMCmdpI_WF9f9Iidk-jZd-DZElu-_bu7HSsrq58MjiXLwD91h3679x5LMCwMvi_VgbU0yYbYn9eWR71A5PPFzx3niS6V8CZm6GJ5G5BKS-_WFvmrSN6IkjWNwtM81Rn78LwXGQTprMRSLAsV3oMcBbSHzV4tyonMfhMh-ZwrHQMNBPL5u2k40l4AxNUQvoF4OwULYPv-LDzYeJP6LzywlXGzB4kHziE7TRyf5qmhGj9GWOoO-ZvaI_TJAK3g1kFPU2dehArDfjoFgB4qakWJfZRtJchnGvzrZoYnsffm3LvFoWbeLA4iRsGxuGiTowwh9F4I6ZlQzIYE2Azuxd07rI9h079JbDcZHa3o3N8qjsqWrPXuWUDkayVNZvWpMo_Jd6IJftIf-U4fMczlxzE6zhSnaVpTV-B3Rw4rjCXdF13AJQnXZOf-qxExO00vFh7C_ljdPxCXYvk3fJqsXcUzNL4g6oStx6N-N-FrTpK7gK8J41ybIXI6w95l8d_e9003__mC0) <br>
   3.4. ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/b5HBRjmm3Dth55osGEO2MHJ9V5hCmkYWmHo0iPYf6bboIJc0pvP5ZfGhbBBbHZDj0tHfyRt7zqZ2hyylDvAGqz1v8uyk04SXarpo1CVUOY8uuDXHID1G-XujhE2EVWuKMeAjmnDZPmosAJBikjx7aGXGu2Z4vZuEmIAFYyJdo5qkVZdkJHj3ukYNqcR-zCGPSDWOVNDfFDFSDPKYnn_KfWO3dYWBR37XFSe4tAwDoGPWzIdtWclubYrB4aWHXZbMNs9rKwmSmJtbzsmkavHxs2YLP-g7ZsyGjQSb1UmQ1PmexSE3HiFaOjWCp2fROYtsvzdL6Xf6sQgnNQk6EaBjbDZH4_eQfraKiLgQ5VaBz-3U31XBDJatMQBy7raTpYdd4LedlSUn1FlQPxYeqpAhQTxNUX8JIdxtY3FmOXztv7LxiZZ0O471n79cfbw3JhcqteT-q7LSvQS6dNVXT6ijaqXTMMDul6rRlPU5KD9CQZfabw_Wl3HDM2PhfTSxUolWFv3LLkTBUs-RCJmuxgGWBwP_liY_xABGfs5fbmgl5_gFlRGLfsRaix-XOFL7y0i00F__0m00)
