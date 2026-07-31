---
title: "Sự kiện 3"
date: 2026-06-27
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# Báo cáo tóm tắt: "Giao lưu đấu kiến thức AWS" - Cuộc thi giữa các nhóm

### Mục tiêu sự kiện

- Tạo ra một môi trường hấp dẫn và cạnh tranh, nơi các thực tập sinh có thể kiểm tra kiến thức của mình về các dịch vụ cốt lõi của AWS.
- Khuyến khích làm việc nhóm nhịp độ nhanh, tư duy nhanh và giải quyết vấn đề hợp tác dưới áp lực.
- Củng cố kiến thức về các khái niệm AWS như EC2, S3, VPC, Bảo mật, Serverless và Quản lý chi phí.

### Người tham gia và Hình thức

- **Người tham gia:** 4 nhóm thực tập sinh từ chương trình FCAJ (bao gồm nhóm của tôi, Nhóm AQI).
- **Hình thức:** Một cuộc thi dạng đố vui với các câu hỏi nhịp độ nhanh.
    - **Vòng 1 (Cá nhân):** Mọi người tự trả lời. Người có thành tích tốt nhất sẽ tiến vào vòng tiếp theo.
    - **Vòng 2 (Theo nhóm):** Các nhóm thảo luận để trả lời các câu hỏi tình huống phức tạp hơn.
    - **Vòng 3 (Chung kết):** Một cuộc "đấu súng" nơi các nhóm chọn chủ đề và trả lời câu hỏi độ khó cao để giành điểm.

### Những điểm nổi bật

#### Áp lực của "Chế độ chiến đấu"

- Tính chất nhịp độ nhanh thúc đẩy chúng tôi giao tiếp hiệu quả và ra quyết định nhanh chóng.
- Chúng tôi có chưa đầy 30 giây để thảo luận mỗi câu hỏi và gửi một câu trả lời duy nhất với tư cách một nhóm.
- Giữ bình tĩnh và lắng nghe nhau có giá trị hơn việc hét to nhất.

#### Các câu hỏi tình huống thực tế

- Các câu hỏi yêu cầu nhiều hơn là ghi nhớ định nghĩa; chúng kiểm tra sự hiểu biết về các sự đánh đổi.
- Ví dụ: Chọn kiến trúc phù hợp cho một ứng dụng có tính khả dụng cao và độ trễ thấp cho người dùng ở Đông Nam Á.
- Giải pháp của nhóm tôi (container ECS/Fargate + ALB) được mentor đánh giá cao, người đã trân trọng lý luận của chúng tôi về việc loại bỏ chi phí quản lý EC2.

#### Phát hiện các câu hỏi lắt léo

- Một số câu hỏi được thiết kế để gài bẫy những người không đọc kỹ.
- Ví dụ: Lớp lưu trữ hiệu quả nhất về chi phí cho các file JSON được truy cập không thường xuyên nhưng cần truy xuất ngay lập tức là **S3 Standard-IA**, không phải S3 Intelligent-Tiering. Từ khóa là "truy cập không thường xuyên".

### Những bài học rút ra

#### Kiến thức kỹ thuật

- **Kiến thức cơ bản về Mạng là nền tảng:** Nhiều câu hỏi bao gồm VPC, Subnets, Security Groups và NACLs. Hiểu về mạng là rất quan trọng ngay cả đối với Kỹ sư ML.
- **Serverless so với Managed vs. Unmanaged:** Biết sự khác biệt giữa các dịch vụ được quản lý hoàn toàn (Lambda), một phần (ECS/Fargate) và không được quản lý (EC2) là chìa khóa để chọn công cụ phù hợp.
- **Hạ tầng toàn cầu của AWS:** Hiểu dịch vụ nào là toàn cầu (IAM, S3) và dịch vụ nào là theo khu vực (EC2, VPC) là cần thiết để thiết kế các kiến trúc có khả năng phục hồi.

#### Làm việc nhóm và Giao tiếp

- **Tin tưởng vào điểm mạnh của nhóm:** Chúng tôi đã thắng một số vòng bằng cách nhanh chóng phân công vai trò và tin tưởng vào chuyên môn của nhau.
- **Sự im lặng có thể là vàng:** Nhóm tốt nhất không phải là nhóm ồn ào nhất, mà là nhóm lắng nghe cẩn thận và gửi một câu trả lời thống nhất.

### Áp dụng vào công việc

- **Đặt tên và Gắn thẻ tài nguyên:** Gắn thẻ đúng cách rất quan trọng để theo dõi chi phí; tôi sẽ đảm bảo tất cả tài nguyên dự án của tôi được gắn thẻ chính xác.
- **VPC và Subnets:** Bây giờ tôi hiểu rõ hơn tại sao SageMaker Notebook của tôi cần nằm trong một subnet cụ thể; tôi sẽ chú ý hơn đến cấu hình mạng.
- **Tối ưu hóa chi phí:** Tôi sẽ ưu tiên sử dụng Spot Instances cho các tác vụ training không quan trọng và theo dõi chi tiêu với AWS Budgets.
- **Tính khả dụng cao & Khả năng chịu lỗi:** Thiết kế triển khai multi-AZ là một yêu cầu đối với hệ thống doanh nghiệp.
- **Hiểu "Tại sao" của các dịch vụ:** Hiểu các sự đánh đổi của dịch vụ AWS, không chỉ tính năng, để đưa ra các quyết định kiến trúc tốt hơn.

### Trải nghiệm sự kiện

AWS Knowledge Battle không chỉ là một cuộc đố vui thú vị. Nó là một bản tóm tắt hoàn hảo của một vài tuần đầu tiên của kỳ thực tập.

- Nó buộc chúng tôi phải nhớ lại và tổng hợp tất cả những gì chúng tôi đã học về EC2, S3, Security Groups, IAM và kiến trúc Serverless dưới áp lực.
- Môi trường cạnh tranh rất hiệu quả để củng cố kiến thức.
- Nó đã giúp tôi bước ra khỏi "vùng ML" của mình và nhận ra tầm quan trọng của hạ tầng nền tảng như VPC, Load Balancer và Security Groups.



> Sự kiện này đã nhắc nhở tôi rằng một Kỹ sư ML giỏi không chỉ biết mô hình—họ còn hiểu hạ tầng mà mô hình dựa vào.
