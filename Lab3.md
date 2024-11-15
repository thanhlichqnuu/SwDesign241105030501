## Câu 1
### Context Diagram BankSystem
![Context Diagram](https://www.planttext.com/api/plantuml/png/h5FBJiCm4BpxArOzjOXMS8sYYXOGgeHGrPuuEiwsMFKZiZT0U7mP1pw9Ny1kcZPj94vSR6TtPdQyw_nyVLzvuevAhHZp6saAxhW6eRZt4o8div9m9gnPoZU4Ymu6tXd0b8lDsjdIvDTMMPUclinyvGar5Cw-LkCntClr4zrPbQDPsFmHbR8lx9EnMcJEAsULkhQ6ueuEqbJK7u4RIu0hpGxL7qIYD8HknGN2RChDPbcNIzDzl27cM5WlgSy3NJoXs2JGdCuXe6sa9n3NcLbPfpb9QmO7SqVotPlzJv467KgW8KcDyf3hq5TA8BTbfZ162bxTSC84uXe3g0jbAyJPJGBBC3ApZfRMI9CjjpzeiMDuNWl4-4uYHc_tAZ6nqpbgGijvrwOGiTP3gJDqBHl3y2me7Bk9B2W-S8sddjj2BITrTj5MwsIdEydZ2tGVL--o1yFXUBktNq_IpD73TXWUdYLdRKHaf1-ZqVPmn9IXVQX3KpmxmTULHgEptc7AXqf_e4zxda3fqJDsXIQF_-il0000__y30000)
### Giải thích 
<ul>
  <li>PayrollController: Chịu trách nhiệm thực hiện use case "Run Payroll". Lớp này sẽ điều phối các bước xử lý, bao gồm tính toán tiền lương và gửi yêu cầu gửi tiền đến hệ thống ngân hàng.</li>
  <li>IBankSystem: Định nghĩa phương thức deposit để gửi tiền vào tài khoản ngân hàng.</li>
  <li>BankSystem: Chịu trách nhiệm nhận yêu cầu gửi tiền từ hệ thống tính lương và thực hiện các bước cần thiết để gửi tiền vào tài khoản ngân hàng.</li>
  <li>Paycheck: Chứa thông tin về số tiền, ngày trả lương và mã nhân viên.</li>
  <li>BankInformation: Lớp này chứa thông tin về tài khoản ngân hàng của nhân viên, bao gồm account number, routing number và bank name.</li>
</ul>
