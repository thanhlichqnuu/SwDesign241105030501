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
   ### 4.3. <br> ![Class Diagram](https://www.planttext.com/api/plantuml/png/Z99DJiGm38NtEONL5I3DWXiCwi0EX10NC9sdAf2VoZ4ZZH0dOy6Hk09fKggYOKPa4_d5p_PdvUlZSvsKHL-zCoQzs40I4unHgmxK2bX1LrjlWqqgh7O7Ui0GHMb5hUEKQ6Ev5_R6T2NydLnpRw9uUZEKFLA4n_q0Ad7flXcxb11XkmZyuE8Uk6EFB13rq5gm5QiGosVdHERzLEis1fNe7AGCGDGLflfOxAEOU3TBDOj31pTBSuk9lRBe8SKIuf1XBdClyHcTtdBW7XvXzF8J9qn3Pj3hXR5ES7IppML3grMvJg_WpnAB3VqKkcWcqFyQydKKoUIppYl9N-mR003__mC0)
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
   ### 5.3. ![Class Diagram](https://www.planttext.com/api/plantuml/png/p9HBJiCm48RtFeNL5I1rmPOLY52f4eMAmW46UqWCVaJs114XJiQ28t45t3pQf4sWIo95IVpFv_6CV-Vxy-iy47WgZ6Oil2ZBlGl862dIo1UWBCMRNvbSknAHp-sJymP8ESkd_59323nHa7emZ8dgSuKQ1SqAAzPHinZEtncFbrGXrr3UvjLuenyTiu-Ml92oJRJ1fjo2mUe56-s-pEi10qehcqRCOmZLK712WLwXABoYygOmZ-XhWS1AyF8UtXAKHPMxHXnbw7V6yinPxD2PAxmkxu3gn04q-FAiUXVE61L2H3VoElfQ6KNRqXvo6TM1wjgYvd8TFDZ2IsV9EwtHDuqCFNcaWtiKRBM8rFFG4agHeNX9KAjNzEK2ANEoEsL_vNkp5Zsv2yOfyHTGzkHcHGAiG9qCIIbQz37LJ5dGxRAx-JOUtMliltRHdoQgRPOFRXJVbh_qxZcwOW4MKZHeAG62HmZOz3j5wk_Im3cTd4xuT5eznYp8TWzfXnbq7nkmVeSPizVk-Zh-wT2ZHRFXat0GEkhuW-XHsnz4i_5jRFcJoTRgZ9sZbV7d_GC00F__0m00)
   ### 5.4. ![Sequence Diagram](https://www.planttext.com/api/plantuml/png/d5PBZgCm5Dnp2YkhH4fV88jH8mXI5cWYjJY00w_Jde3DsAPRETiivaXpXNbs-DWq92WBBu1wzJvLjldtv--hqbJgfYg3G5qO9r8e20BDT0aafOnhN6HVrQMu0f03VnUoefe9Jbx86_nkWET0OaRFabP1G7Cj95aTwLMAiYHXKJ7Eb9OKNwy8LUGO1ZNcOpchATV8K4AkauRdXZ91RWDwIv8xg4XmRTX1th2HXmsBegksemltoHp4vmhtFbTM5rJ3c2uRqVaedp4RCSROoHms7c6FKlp2jbFAwHagu3gccfwe0Zl7DFR0lKBuRPy6mJ4aBp_C87UaOAekwVLdRKVS3d6zCLgnJwpSZXkN2JY6Ew8-n1SH5gt86eUrRLlSjkLlWWAyO3URibgH5SRrHQqcSw5o7RoloW_xbiXvY90cCZIeRj_ZUXGH3H761BYw9Xcl6qsWcneRVEqocA2sEPj6DQUApOHDPK93xGWTxBRk8esKct4cvo521jiTwZpDuEXdl83BmFVfZkGIp5iENuCh6CTjZZlLJMd2sYosJWKQzst-0Va5TMQV8Ayfw0zHh5SroozDZNguLJMUx-SAcqve96WriuNs4pt4_bIYINFT_FYClyQHYooMBREOEHYoMOlvdMM3ix8fPo5wYZSpGiqC_b1inXcSXmWf1ktEe2VZfpnbSqhGZNGk0d4oPzDOtJQ5Ew-7UomRDBPnj-uUxB758zcIsIrtTq1FcNkwAy-vjnFq6UUE8nSvzw4F3RQlCxhlGuStDaCllCjipeVU5Z5tNFoa3-FbFeo7KoON_9tXnMsB7Lal7aIovD-mKtLRv1auu4yD98pJiZir7PUuFSwCQR6LR9Mlm0lyIViF003__mC0)
## 6. Phân tích ca sử dụng Run Payroll <br>
   ### 6.1. Các lớp phân tích: <br>
     Boundary: PayrollUI, ProjectManagementDatabase
     Control: PayrollController
     Entity: Printer, BankSystem, Timecard, Employee
   ### 6.2. Nhiệm vụ của từng lớp phân tích: <br>
     PayrollUI: Hiển thị UI payroll
     PayrollController: Controller xử lí cho các phương thức liên quan đến payroll
     Printer: Đại diện cho printer, dùng để in bảng lương
     ProjectManagementDatabase: Truy xuất thông tin các employee
     BankSystem: Đại diện cho bank system, chứa các thuộc tính và các phương thức liên quan đến bank system
     Timecard: Đại diện cho timecard, chứa các thuộc tính và các phương thức liên quan đến timecard
     Employee: Đại diện cho employee, chứa các thuộc tính và các phương thức liên quan đến employee
   ### 6.3. <br> ![Class Diagram](https://www.planttext.com/api/plantuml/png/X5DBJiCm4Dtx55PN1QaBRj10MR0eL7p4UkfC6rD_el5u4I5Ene8ZSGKSuxQXfP2DP-Qzf_dcy_rZ6XY8epL2X8rsadn08LYpGNaVdLn0HzuOEP5N1aAGCmrh0Yk4ocw1dsxagv3fgtLe3NGbV8-j9nwVIIdU3XHNtd7_8XKbHLUWAhAtm5gDppAoHeS4Z0bM3QfD2Il25Bm4jtaaS04KQ-yA5j3LloCAZ8ec2H_007Kfkgki5pnqWT6MahXNhv3ctk4FveAqurtbRUyDYXlG_0igdeE3DLfqF0E69GGimZLoPSorROtl48VARImJ9nABUpFBhWEBsGYvXsmkqv1MchFTGjTdcoCtllv6KskLKZuwlersYRHFzQWjAg3wCDMtiF6HmhEd3TQ3lYAf9hLnHtKPmf7Ezr1b-uIzRdyceukHd4poStG9ulWs1lJzUlxcbUNyHpgn6d5wQLlv-MYt7x5Rr03SJlHNyCViX13JTAdfx_i2003__mC0)
   ### 6.4. ![Seuence Diagram](https://www.planttext.com/api/plantuml/png/T5JBZjim3BphAtZS7l83EHIxTb9W3m6Cs8kUkJBNKIrBhaItyBVrq4_gBvIA7tNTRO0SDEPmPYZQltxyV8oCWOVEAXLRuo3uI4gnOKjm7HmKE0PlBHoWfAy3EKrmCjW4x9H2pJv0EKQcBhTUju0Hj7hrWwinZ0ltvJdXByzAUyS2B7W-7Is5zBp8DyJWlv3c2pfig2F79sHynKYfy9GfGGoFSEvwwqUwe-VBWbQc8usXJcYLBsWHZEDPwRg06Rfsif_mh5HAm-6ZM3r25KpJI7sG6VJp31u-1LFZ21BQOcJuxeECh071FgHXc6_8b89AOcbJvCT4dzC-3UmxPACVDhKIkiXJxIaxGaFyPEqIQbicaK_Psf9u20wi4GV-RHr2L3Lj2TRx7jx4gg2tjKg1_2R9y-KkcMuZZHWkn3TVtmlMFZBLT3vVTkBlS3RgCskIgV99vkQ743_Bn6Yd8NUKpbM-qzWJDW8pfLWf6gqUh3mgqSe2oUpk4dQV3ao43erDLzWRtHw6_bwvwNOzGfzsHOZwHhgTU_rbMJPePLqN3_rCcEYpwPtncKXMLlbVPxK9ilLIt_jeU6yinGmaNTBMLW5TJ6szsnYSAhFo295S_V-wrO-i_89bvQB2VpYInMkAyVqqCrkaLFfFwkdbgKtiBOxpvbybJs2HtmuYtvxabL6Fqa8-Gxy1003__mC0)
