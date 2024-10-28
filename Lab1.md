## 1. Phân tích kiến trúc <br>
  ### 1.1. Đề xuất kiến trúc mô hình MVC (Modal - View - Controller) <br>
  ### 1.2. Lý do lựa chọn: Các phần Model, View và Controller được tách ra độc lập, giúp cho việc kiểm soát và khắc phục lỗi dễ dàng hơn. <br>
  ### 1.3. Ý nghĩa từng thành phần: <br>
   * **Model**: Là bộ phận có chức năng lưu trữ toàn bộ dữ liệu của ứng dụng, là cầu nối giữa 2 thành phần là View và Controller. Các mô hình là dữ liệu được sử dụng bởi các chương trình. Đây có thể là một cơ sở dữ liệu hoặc một tệp XML thuần túy hoặc một đối tượng đơn giản. <br>
   * **View**: Đây là giao diện người dùng (theme). View là cách hiển thị trong một ứng dụng. Nó bao gồm mọi thứ mà người dùng có thể nhìn thấy. <br>
   * **Controller**: Là bộ phận chịu trách nhiệm xử lý các yêu cầu của người dùng thực hiện thông qua View. Controller bao gồm Model và View. Nó nhận đầu vào và thực hiện cập nhật tương ứng. <br>
  ### 1.4. ![Package Diagram](https://www.planttext.com/api/plantuml/png/R55RRW8n3FptANo1lG5QKK6H-e644Es_kx5GIXuhnrM5gfwi7no9ApHPO0cKlsHcCZDsZh-7QL8I_VGE8EriG8c90TIgOrnHjwCj9snmvYWbd5lQ2dc0_iJWc-Kld4mM6UIsnMz0x0Rbi-zTt3E_lepGYlOIdNioteOC_rnTPZ5eeLYorvexlR4wlxkA_eKyeDRSHz6AgEAMqR0hhQCpB0zhZy36Ukv8p7sRkw3QVavAxvGu9roEj_D8_CWpBYbajUUW5rKn6HRQD6sr4wZMKvYXFfo6AFVnEKmvcFoJVm000F__0m00) <br>
## 2. Cơ chế phân tích <br>
   * **Persistency**: Hệ thống cần lưu trữ thông tin về nhân viên và các bảng chấm công, hóa đơn mua hàng, báo cáo, phương thức thanh toán, v.v., để có thể truy cập và cập nhật dữ liệu một cách đáng tin cậy. Tính bền vững giúp duy trì dữ liệu lâu dài, bảo đảm rằng dữ liệu của nhân viên không bị mất sau khi hệ thống ngừng hoạt động và đảm bảo rằng các bản ghi lương luôn sẵn sàng khi cần. <br>
   * **Legacy Interface**: Hệ thống mới cần tích hợp và truy xuất thông tin từ cơ sở dữ liệu quản lý dự án cũ (DB2) trên mainframe IBM mà không làm thay đổi cơ sở dữ liệu hiện tại. Vì lý do chi phí, Acme muốn tận dụng lại hệ thống cũ mà không phải thay thế nó, vì vậy cần một giao diện giúp hệ thống mới tương tác mà không gây ảnh hưởng đến dữ liệu cũ. <br>
   * **Security**: Hệ thống phải đảm bảo rằng chỉ nhân viên có quyền mới có thể xem và chỉnh sửa dữ liệu cá nhân của họ. Ngoài ra, cần ngăn chặn truy cập trái phép để bảo vệ thông tin nhạy cảm về nhân viên và tiền lương. Bảo mật giúp duy trì quyền riêng tư, tuân thủ các yêu cầu bảo mật nội bộ và tránh các rủi ro về truy cập trái phép. <br>
## 3. Phân tích ca sử dụng Payment <br>
   ### 3.1. Các lớp phân tích: <br>
     Boundary: PaymentForm, ProjectManagementDatabase 
     Control: PaymentController 
     Entity: Employee 
   ### 3.2. Nhiệm vụ của từng lớp phân tích: <br>
     PaymentForm: Hiển thị UI và các trường input để người dùng nhập 
     ProjectManagementDatabase: Truy xuất thông tin theo payment method hiện tại để hiển thị lên UI 
     PaymentController: Xử lí các request payment 
     Employee: Đại diện cho employee, chứa các thông tin và phương thức liên quan đến employee 
   ### 3.3. ![Class Diagram](https://www.planttext.com/api/plantuml/png/T5FBJkH03BptLrXSs4M0bYj28y9CaABTWH4CP-GaPcZeHzJTGPf5VDaUzfFu1Poa9sHUfyYkQfVBTZx__R_q0LsejHB-LPeA7Mee57gVXE1aNWVA2clkvL-2Nq8SmfMjJObksP78Y_OBCrngCk7QEWqN5taaZKRmBW1AwIk5oyYvhOAqnl_uoSY2GinEAJpRCZDL7LR85AMIPf6KfIFlrw0hDAz9KR1C-Cv7cR4rJz9fR5I6-TGvwwPS2HV4-G-nQjtP5ofOpJ3Gj3B1W3bwsZR2ofbvih7uk7QEwT50gYjbbqITaKxW4BYPuApQFQq8Ad8iLNJ1K8cDhMlqjG7UKCaIUJkzVOzljCshguQrcMzxIqsGONEHAnlS4RLuR8XYFfl0EKWJE6LG4mUUxyGiEAw68Zq0xxDi_FjXTWpJ9Fjp39FiBXtF7oVfxFO-ct_mkvoNURDH2xlbtjGwv-aC0Brs54F4a-8rRazWyyPMzXFlRI7RJNenlD-Jaz6E3Pt3mTdPWTW6MlhU6sgUdPuUxNlOZxldYKioPVC_VW400F__0m00) <br>
   ### 3.4. ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/b5HBRjmm3Dth55osGEO2MHJ9V5hCmkYWmHo0iPYf6bboIJc0pvP5ZfGhbBBbHZDj0tHfyRt7zqZ2hyylDvAGqz1v8uyk04SXarpo1CVUOY8uuDXHID1G-XujhE2EVWuKMeAjmnDZPmosAJBikjx7aGXGu2Z4vZuEmIAFYyJdo5qkVZdkJHj3ukYNqcR-zCGPSDWOVNDfFDFSDPKYnn_KfWO3dYWBR37XFSe4tAwDoGPWzIdtWclubYrB4aWHXZbMNs9rKwmSmJtbzsmkavHxs2YLP-g7ZsyGjQSb1UmQ1PmexSE3HiFaOjWCp2fROYtsvzdL6Xf6sQgnNQk6EaBjbDZH4_eQfraKiLgQ5VaBz-3U31XBDJatMQBy7raTpYdd4LedlSUn1FlQPxYeqpAhQTxNUX8JIdxtY3FmOXztv7LxiZZ0O471n79cfbw3JhcqteT-q7LSvQS6dNVXT6ijaqXTMMDul6rRlPU5KD9CQZfabw_Wl3HDM2PhfTSxUolWFv3LLkTBUs-RCJmuxgGWBwP_liY_xABGfs5fbmgl5_gFlRGLfsRaix-XOFL7y0i00F__0m00) <br>
## 4. Phân tích ca sử dụng Maintain Timecard <br>
   ### 4.1. Các lớp phân tích: <br>
     Boundary: TimecardForm, ProjectManagementDatabase 
     Control: TimecardController 
     Entity: Employee, Timecard 
   ### 4.2. Nhiệm vụ của từng lớp phân tích: <br>
     TimecardForm: Hiển thị UI và các trường input để người dùng nhập 
     ProjectManagementDatabase: Truy xuất thông tin theo timecard method hiện tại để hiển thị lên UI 
     TimecardController: Xử lí các request timecard 
     Employee: Đại diện cho employee, chứa các thông tin và phương thức liên quan đến employee 
     Timecard: Đại diện cho timecard, chứa các thông tin và phương thức liên quan đến timecard 
   ### 4.3  ![Class Diagram](https://www.planttext.com/api/plantuml/png/Z5DBJiCm4Dtd5AEk08bIjYYgG7ma5aX8S869FMrCOpiQEw22E1aBZiGLc2PrA6cBM2InP_pclNdZV7rydeU871jRPM5XN8sC5bI58Lp4oAPe8jqgxnxCAy4aozeCF1fB2bdVUBQGvuLld4PUJgVmbW6SW3QXhd09SNtkuB0D-vhSUaak4aFf6mumymogH9uJkCOMn65zoA9nKPvXdO3Fj1bx7-gwz2wohogXo7FLRNfnSugW6cQHC2pSfZebocjAEffQOwH_gxXd_qGgtg73ELcXkSA81GRQPTKEogrs12TLJ4oephONpmlIigt5wPhOUDthskWdAGJZPdvlGptdjQqhloGQSZgq91zAQRCYAz0jshgo3buPh22GU2kmzIWbWLepXR0IMdf7FmcI-LQT_fLBO2cMqeD8-NM_HgSZE6xVs-FDTanyD1cFEqYts3kEly4RV72MBaoAzD0MS9G0oRmiEoUdvP_w1W00__y30000) <br>
   ### 4.4. ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/b9H1ReCm44NtFeMNH6eka4KLYQPg5gsggXUOu4b21JOQnf4uMnSzKgzGOq8CJPmGTZRp_yVFC_n-_onh1c9R5W8oDYHNPLMO1b5iZDKAg96VUOaPa7esL8hCQ2PJd3RJRbqW2TISSoWF1kzalZ3ZLz2mmzALFG731ceKGlHnSluu2bf8Kw5EPcAuEImAmGkvGqujaNFktoPuz5shO14aGoClxnThlJKNjN8UoIPaIrfcNRxa_lINGi_EgFAwAg0vLmieMAuqEzNUMAhbrbrDjWVQeTIst3ZSqZrnUjXgNrgfMwTU-EPrYVTxE9frUpDlDeMqhHGmdYZVz8eXlzSdYj_rupQd4ZWtEfeSvTvzXWhSKH_PVo1JZWVieMT6OJqPKzkGNfUsikGQa-XmH5oYzJSxD7QGQHqwL7jALqQtXaEussaZF9By7uVR8zpAamdJEcgNkm2q2MEvM3eExiVv1m00__y30000) <br>
## 5. Diagram hợp nhất ca sử dụng
![Sequence Diagram](https://www.planttext.com/api/plantuml/png/X5JTRjem5BxtKnnnmrOLL6uhL9K2awAD5gtiUZBn0JmIExATJgpga-rYZxHNs4dif0a1Ti6Fp-ztllFPVt__kRUE6vUd2RDxgJ9kU0fnmgsTE6VaEdSOnLezory8DupruK7dId1py45eMVaBItv8KRbFsgGm7gz3qDqTl3808MsMy4E8USgSrCf--4YUBRfWNQ3RQH6fB7ULPy5b8jLs8eH1Qrkk1wxsapYcDkxT7jfCjTf8a_AYIzC-DqQR1LNYMoJx6mlGLpB5c1jn4Jku45LMr1dwqWGS3UnqRYnij85unyqMGUNf6eqVCULIEVgqArZ-WarBZMPfz0-CQNP5C0jYPjpnDRVOXKOyH8gw-b6dkJ4K7kYSfrcY3uYUregs2b-i1LhVjG_4bpCwERtGu4neol4uzeTcU-A-tRZHy8KdKd0IKBsXOkfkN9uLKSVspdukGu7OmsZJV6Bcgjz_zz67kNBI7IkzOfP0OEaF633OendS0gsSJ8gdI0TB5qbjwPmrHwmTyBgCff-_BQzXCOc-NCCi-ZgVhhxFvikdvsZrHdbhKllZKItkrVzOAgtfI5ktfjL-frMbpQOTYvHtGuVuuqczt7zgiqVXfu8CZTGYy5WpN_59T6pq6UfBeYVMwbYMChQi-PGC1dSdb7WBlT6enxgEClpi1IhIXiEhSudrOkiurdeQUgCU3ChlhYBP2P7sReP3d-B_d0LsERdHZv05bLUMEhLCkAeIgb4OkqSbYiVz7m000F__0m00) <br>
  ### 5.1. Các tác nhân tham gia:
  * **Employee**: Ghi nhận thời gian làm việc, tạo đơn hàng bán hàng (nếu có), và chọn phương thức thanh toán.
  * **Payroll Administrato**: Quản lý thông tin nhân viên, thiết lập các thông tin như loại hình thanh toán (theo giờ, cố định, hoặc theo hoa hồng), và tạo báo cáo hành chính.
  * **Project Management Database**: Cơ sở dữ liệu hiện có chứa thông tin về các dự án và mã chi phí, được hệ thống Payroll truy xuất để phục vụ quá trình quản lý chấm công.
  ### 5.2. Các lớp phân tích tham gia:
  - **Boundary Classes**:
    - **TimecardForm**: giao diện cho nhân viên nhập và quản lý bảng chấm công.
    - **PaymentForm**: giao diện cho nhân viên chọn và thay đổi phương thức thanh toán.
    - **ProjectManagementDatabase**: truy xuất thông tin mã chi phí từ cơ sở dữ liệu dự án.
  - **Control Classes**:
    - **TimecardController**: xử lý dữ liệu từ TimecardForm và truy xuất mã chi phí từ ProjectManagementDatabase.
    - **PaymentController**: xử lý việc chọn và cập nhật phương thức thanh toán của nhân viên.
  - **Entity Classes**:
    - **Employee**: chứa thông tin nhân viên bao gồm loại hình thanh toán, phương thức thanh toán, giờ làm, và thông tin ngân hàng.
    - **Timecard**: ghi nhận thời gian làm việc và số giờ làm cho mỗi nhân viên.
