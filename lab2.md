## 4. Phân tích ca sử dụng Create Administrative Report <br>
   ### 4.1. Các lớp phân tích: <br>
     Boundary: AdministrativeReportForm, ProjectManagementDatabase 
     Control: AdministrativeReportController 
     Entity: Report 
   ### 4.2. Nhiệm vụ của từng lớp phân tích: <br>
     AdministrativeReportForm: Hiển thị UI và các trường input để người dùng nhập 
     ProjectManagementDatabase: Truy xuất thông tin các employee và report
     AdministrativeReportController: Xử lí các Administrative Report 
     Report: Đại diện cho report, chứa các thông tin và phương thức liên quan đến report
   ### 4.3. <br> ![Class Diagram](https://www.planttext.com/api/plantuml/png/Z5BBJiCm4BpxArOv0L8ElVPKbC8DL1L-O4bNaS6FQBsjL26-Z4C_gR-0OmUhLKb5BgkCTsTsnZv-7nP1a6LhZLBXGpjW7qWfqM886YOKWlkDrKu7OHIz8rXJxrcWXiPW2B3Ks35QfThqUzwSUnyzM_XK46Su0Q_xdc0EByBQTGbFMom7jJaC9O7aDXUGxOtV4psZFMC0w4YoMiDQY3NUt0AehsjxDTu9UsE8qtO0RJAS3zFu00RS5IXteMl95AX8ZC5aep9jyTBXXC4oNYHMxD-fbITqs94bD_3X6mOQ3SGG7au8ydQJLrBDAgZhLAx7yoV5INg_H7VL6C9_1sAPjAJYjuW1nRVv0m00__y30000)
   ### 4.4. ![Squence Diagram](https://www.planttext.com/api/plantuml/png/f5DBJiCm4Dtx5BCi4Rr05wYq0NK15G9nW6aoQWs97Pn9KTOiEGKh9AHAhCc2HINkaHDm1PnFLJS2jH8Rnv7VctdpdlrTV0vJHiDP70cHtai5HgSa14kE2CQ6a0bEmrWgcR91bak2QqgqOUZ33Jraf082N-BSO2m41gmDtAPan4ndAaIJTzWD-LoR6325wYi2hTZew5VWk3cBo5JmxPyWPINchHOH8kCCKu8he-yeu4jKEAVOWlpDYQNx8o4gRT0_gJl30AQBycEL0ClrMmR1Ohs2sVf5Gs0NKKCirD4mWA2sf6dRCur68vcCnADgVBci77E4EcnRon_P6dFYipY9T4uqnPXw3j5Aj91-joivS16I2z-jtsOp0CzJzEXvFSuJEeOwOsk5tP8AsurJqr7GEhe9kQl4xTv2NGLRPoUoB9uKyA8idXrJ7RfZKZUMYw_tR5yIAIvtSpZ4VyUVYcyD-jVeXqqpAOlNVE_5GlkIedQW_QDig_ybGWnjrFPT_m000F__0m00)
## 5. Phân tích ca sử dụng Maintain Employee Information <br>
   ### 5.1. Các lớp phân tích: <br>
     Boundary: SelectFunctionForm, AddEmployeeForm, UpdateEmployeeForm, ProjectManagementDatabase 
     Control: SelectFunctionController, AddEmployeeController, UpdateEmployeeController, DeleteEmployeeController
     Entity: Employee
   ### 5.2. Nhiệm vụ của từng lớp phân tích: <br>
     SelectFunctionForm: Hiển thị UI cho người dùng chọn chức năng thêm sửa hoặc xoá employee
     ProjectManagementDatabase: Truy xuất thông tin các employee
     AddEmployeeForm: Form để thêm employee mới
     UpdateEmployeeForm: Form để cập nhật employee được chỉ định
     SelectFunctionController: Điều hướng user đến hành động tương ứng
     AddEmployeeController: Controller xử lí việc thêm employee
     UpdateEmployeeController: Controller xử lí việc cập nhật employee
     DeleteEmployeeController: Controller xử lí việc xoá employee
     Employee: Đại diện cho employee, chứa các thuộc tính và phương thức liên quan đến employee
   ### 5.3. ![Class Diagram](https://www.planttext.com/api/plantuml/png/x5LBZjGm4Dtx55Ql0AaNR6SrQ49B8z4meeS3LDj5OiQVg5n1H8YJiU18N05FIARZQHlr0OWK9V6hzygfUfNy_ldhEZ8G3yuA4H-CbnGY2i66BSez6C_fb6zTRyE8A6_zvq0Es0Glj_B6GeooCT0IE27Kz7X0YuftWrUFKRiKBhyBcGvjOczX_D1FwpF-ugNuiJ3VQBqaUg9jfGU7L_B0P7mxBU0SSp_sEU30s7IVP0XZpA0Ob05xG3MGuV7zu8v8UG23rq3w7hurg8TfRqcY2SFHuXGHk4EgO7qNF1PKkp2G7Jy2OnOUmGADsP8ApfaOa_9PzAF8E-CCNwNoCxP8fv9zwdKABrHjATAjpbZ57jq4pnIiHPex5JEuqg8p5fomHFchmtSmgWxLGuFMV4KQzyXTq6l9_1NEL8SCNXEJ9Fw3g3Dutf42hz0s9QX5ZvHIxOm7ksnxdUzf2EeL_k_Nib-dd4KdBEdbgSvt5Bua--t1GuiEFJV0S8I8SsDRvDmEXI_EvlL6RhVJfUPryVnpi-8KRIuAmxRYr7pyV7yhewxOrPSMvP6xY5eThOlOrVcwY2tgRLpuhpQdcHBY6hrElw4_0000__y30000)
   ### 5.4. ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/d5PBZgCm5Dnp2YkhH4fV88jH8mXI5cWYjJY00w_Jde3DsAPRETiivaXpXNbs-DWq92WBBu1wzJvLjldtv--hqbJgfYg3G5qO9r8e20BDT0aafOnhN6HVrQMu0f03VnUoefe9Jbx86_nkWET0OaRFabP1G7Cj95aTwLMAiYHXKJ7Eb9OKNwy8LUGO1ZNcOpchATV8K4AkauRdXZ91RWDwIv8xg4XmRTX1th2HXmsBegksemltoHp4vmhtFbTM5rJ3c2uRqVaedp4RCSROoHms7c6FKlp2jbFAwHagu3gccfwe0Zl7DFR0lKBuRPy6mJ4aBp_C87UaOAekwVLdRKVS3d6zCLgnJwpSZXkN2JY6Ew8-n1SH5gt86eUrRLlSjkLlWWAyO3URibgH5SRrHQqcSw5o7RoloW_xbiXvY90cCZIeRj_ZUXGH3H761BYw9Xcl6qsWcneRVEqocA2sEPj6DQUApOHDPK93xGWTxBRk8esKct4cvo521jiTwZpDuEXdl83BmFVfZkGIp5iENuCh6CTjZZlLJMd2sYosJWKQzst-0Va5TMQV8Ayfw0zHh5SroozDZNguLJMUx-SAcqve96WriuNs4pt4_bIYINFT_FYClyQHYooMBREOEHYoMOlvdMM3ix8fPo5wYZSpGiqC_b1inXcSXmWf1ktEe2VZfpnbSqhGZNGk0d4oPzDOtJQ5Ew-7UomRDBPnj-uUxB758zcIsIrtTq1FcNkwAy-vjnFq6UUE8nSvzw4F3RQlCxhlGuStDaCllCjipeVU5Z5tNFoa3-FbFeo7KoON_9tXnMsB7Lal7aIovD-mKtLRv1auu4yD98pJiZir7PUuFSwCQR6LR9Mlm0lyIViF003__mC0)
## 6. Phân tích ca sử dụng Run Payroll <br>
   ### 6.1. Các lớp phân tích: <br>
     Boundary: SelectFunctionForm, AddEmployeeForm, UpdateEmployeeForm, ProjectManagementDatabase 
     Control: SelectFunctionController, AddEmployeeController, UpdateEmployeeController, DeleteEmployeeController
     Entity: Printer, Bank System
   ### 6.2. Nhiệm vụ của từng lớp phân tích: <br>
     SelectFunctionForm: Hiển thị UI cho người dùng chọn chức năng thêm sửa hoặc xoá employee
     ProjectManagementDatabase: Truy xuất thông tin các employee
     AddEmployeeForm: Form để thêm employee mới
     UpdateEmployeeForm: Form để cập nhật employee được chỉ định
     SelectFunctionController: Điều hướng user đến hành động tương ứng
     AddEmployeeController: Controller xử lí việc thêm employee
     UpdateEmployeeController: Controller xử lí việc cập nhật employee
     DeleteEmployeeController: Controller xử lí việc xoá employee
     Employee: Đại diện cho employee, chứa các thuộc tính và phương thức liên quan đến employee
