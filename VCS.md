# HỆ THÔNG QUẢN LÝ PHIÊN BẢN

## 1. VCS là gì? Đặc điểm & tính năng?

- **VCS (Version Control System)** là hệ thống lưu giữ các phiên bản
  của mã nguồn của sản phẩm phần mềm
- **Đặc điểm và tính năng của VCS**
  - VCS cho phép người quản trị phân chia các tập tin cho từng
    thành viên, quản lý lịch sử thay đổi file/mã nguồn
  - Cho phép khôi phục lại phiên bản cũ của các file
  - Cho phép các thành viên có thể phát hiện lỗi và sửa lỗi một
    cách thuận tiện
  - Tự động so sánh và cập nhật mã nguồn khi các thành viên sửa
    đổi cùng một tập tin tại cùng một thời điểm

## 2. Trình bày hoạt động của Mô hình CVCS và DVCS? So sánh?

#### Hệ thống quản lý phiên bản tập trung (Centralized version control systems - CVCS)

CVCS là hệ thống quản lý phiên bản truyền thống. Trong đó, mã nguồn được lưu trữ trong một kho lưu trữ (repository) trong máy chủ trung tâm do duy nhất một người có thẩm quyền (Project Manager, Leader) duy trì. Các thành viên trong team sẽ trích xuất hoặc cập nhật "update" của họ vơi dữ liệu có trong kho lưu trữ hoặc có thể thay đổi dữ liệu hoặc ủy thác thông tin "commit" trong kho lưu trữ. Mọi hoạt động này đều được thực hiện trực tiếp trên kho lưu trữ.

#### Hệ thống quản lý phiên bản phân tán (Dístribute version control system - DVCS)

DVCS là hệ thống quản lý phiên bản được nâng cấp nhằm giải quyết những nhược điểm của mô hình CVCS. Trong đó, tất cả mọi nguời đều có một kho lưu trữ cục bộ là bản sao của kho lưu trữ chính. Mỗi người sẽ tự duy trì kho lưu trữ của riêng mình. Họ có thể cam kết (commit) và cập nhật (update) kho lưu trữ của mình mà không có sự can thiệp nào.
Họ có thể cập nhật kho lưu trữ cục bộ của họ với dữ liệu mới từ máy chủ trung tâm bằng một hoạt động được gọi là "pull" kéo về và đẩy ngược lại các thay đổi đối với kho lưu trữ chính bằng một hoạt động được gọi là "push" đẩy từ kho lưu trữ cục bộ của họ lên kho chính.

#### So sánh giữa CVCS và DVCS

|                             |                        CVCS                         |                                                                   DVCS                                                                    |
| --------------------------- | :-------------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------: |
| Máy chủ                     |         Yêu cầu phải có 1 máy chủ trung tâm         |                                                  Không yêu cầu phải có máy chủ trung tâm                                                  |
| Làm việc ngoại tuyến        |                      Không thể                      |                                                        Có thể với đầy đủ chức năng                                                        |
| Khả năng phối hợp           |   Chỉ có thể hợp tác thông qua máy chủ trung tâm    |                       Hỗ trợ hợp tác trực tiếp thông qua các kho lưu trữ cục bộ mà không cần qua máy chủ trung tâm                        |
| Tốc độ                      |               Thời gian phản hồi chậm               |                                                         Thời gian phản hồi nhanh                                                          |
| Chia và trộn nhánh          |    Khả năng chia nhánh và trộn nhánh bị hạn chế     |                            Khả năng trộn và chia nhánh được đánh giá cao, đảm bảo làm việc song song hiệu quả                             |
| Bảo mật và kiểm soát        |   Kiểm soát tập trung các quyền và lượng truy cập   |                                      Mỗi người đều có đầy đủ quyền kiểm soát trên kho lưu trữ cục bộ                                      |
| Khả năng mở rộng            |                     Bị hạn chế                      |                                                           Khả năng mở rộng cao                                                            |
| Sao lưu và phục hồi dữ liệu | Phụ thuộc vào các bản sao lưu trên server trung tâm | Mỗi người đều có một bản copy cục bộ hoàn chỉnh từ server trung tâm, trong đó co các bản sao lưu có sẵn và các chức năng phục hồi dữ liệu |
