---
title: "Sự kiện 2"
date: 2026-06-20
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Báo cáo tóm tắt: "Hội thảo về Công cụ kỹ thuật & Container hóa" - Lựa chọn công cụ phù hợp với từng vai trò

### Mục tiêu sự kiện

- Hiểu rõ các chuỗi công cụ phù hợp với các vai trò khác nhau trong một nhóm phát triển phần mềm hiện đại (Nhà phát triển, Kỹ sư vận hành, Kỹ sư Dữ liệu/ML).
- Cung cấp kiến thức thực hành sâu về các khái niệm Container hóa, cụ thể là Docker.
- Giải thích các khái niệm cơ bản về mạng container và điều phối để chuẩn bị cho người tham dự triển khai các ứng dụng có khả năng mở rộng.

### Diễn giả

- **Kiến trúc sư Giải pháp Cấp cao** - AWS (Diễn giả là một kiến trúc sư giàu kinh nghiệm, am hiểu sâu về ứng dụng container hóa và kiến trúc microservices.)

### Những điểm nổi bật

#### Triết lý "Công cụ phù hợp"

- Diễn giả nhấn mạnh việc chọn công cụ nên dựa trên lĩnh vực vấn đề, không chỉ dựa trên xu hướng thị trường.
- Một ma trận được trình bày cho thấy các công cụ đề xuất cho từng vai trò: Developers tập trung vào `Node.js/Python`, `npm/pip`, `Git`, `VS Code`; Ops Engineers sử dụng `Terraform`, `Ansible`, `CloudWatch`, `Prometheus`; Data/ML Engineers dựa vào `Python`, `Pandas`, `SageMaker`, `Jupyter`.
- Thông điệp chính là không nên áp đặt một công cụ duy nhất cho mọi người, mà cần hiểu nhu cầu riêng của từng vai trò.

#### Hiểu Docker theo các lớp

- Docker được phân tích thành ba lớp khái niệm:
    1.  **Image:** Một mẫu chỉ đọc để tạo container, giống như một lớp trong lập trình.
    2.  **Container:** Một thể hiện có thể chạy của image, tạm thời và biệt lập.
    3.  **Registry:** Nơi lưu trữ và chia sẻ image (như Docker Hub hoặc Amazon ECR).
- Một ví dụ `Dockerfile` đơn giản được trình bày để cho thấy tất cả cấu hình được đóng gói, giúp ứng dụng có tính di động 100%.

#### Mạng Container: Giao tiếp giữa các container

- Hội thảo bao gồm các khái niệm mạng thiết yếu:
    - **Port Mapping (`-p 8080:80`)**: Ánh xạ cổng máy chủ đến cổng container để cho phép truy cập từ bên ngoài.
    - **Bridge Networks (Mặc định)**: Các container có thể giao tiếp với nhau bằng IP, nhưng IP có thể thay đổi.
    - **Custom Networks**: Cách khuyến nghị để kết nối các container theo tên, đảm bảo giao tiếp ổn định và dễ dự đoán.
- Một ví dụ cho thấy một script Python có thể giao tiếp với cơ sở dữ liệu MySQL container hóa trên cùng một mạng tùy chỉnh mà không cần mở cổng cơ sở dữ liệu ra thế giới bên ngoài.

### Những bài học rút ra

#### Hiểu biết kỹ thuật

- **Tính bất biến & Khả năng tái tạo:** Container đảm bảo rằng một ứng dụng chạy theo cách giống nhau trên mọi môi trường, điều này rất quan trọng đối với ML.
- **Hiệu quả:** Container nhẹ hơn nhiều so với Máy ảo vì chúng chia sẻ nhân HĐH của máy chủ.
- **Nguyên tắc đơn trách nhiệm:** "Một dịch vụ trên mỗi container" là một thực hành tốt cho khả năng mở rộng và bảo trì.

#### Thách thức của việc Điều phối

- Mặc dù Docker rất tốt để chạy một vài container, việc quản lý hàng trăm container thủ công là một cơn ác mộng.
- Kubernetes (K8s) được giới thiệu là một nền tảng điều phối xử lý việc khám phá dịch vụ, cân bằng tải, tự động mở rộng và tự phục hồi ở quy mô lớn.

### Áp dụng vào công việc

- **SageMaker Containers:** Hiểu rằng các SageMaker training job chạy code của bạn bên trong một môi trường container hóa; kiến thức về container giúp xây dựng custom container cho các framework cụ thể.
- **Khả năng tái tạo:** Thay vì chỉ chia sẻ file `.ipynb`, hãy cung cấp `Dockerfile` để người khác có thể thiết lập môi trường chính xác.
- **Model Serving:** Hiểu cách SageMaker Endpoints hoạt động như các web server container hóa (ví dụ: Flask/FastAPI) được phơi ra thông qua port mapping.
- **Microservices:** Thiết kế hệ thống dưới dạng microservices, cho phép các phần khác nhau được đóng gói và mở rộng độc lập.
- **Phát triển cục bộ:** Sử dụng Docker Compose để khởi chạy toàn bộ ngăn xếp dữ liệu cục bộ, tránh các vấn đề "chạy được trên máy của tôi".

### Trải nghiệm sự kiện

Hội thảo này là sự bổ sung hoàn hảo cho buổi DevOps trước đó. Nó đã cho tôi nền tảng kỹ thuật để hiểu cách các thế giới "Dev" và "Ops" được kết nối thông qua container.

- Khái niệm `Dockerfile` như một nguồn sự thật duy nhất cho môi trường runtime của ứng dụng là một bước ngoặt.
- Nó đã làm sáng tỏ SageMaker: bây giờ tôi thấy nó chỉ là việc chạy một script Python bên trong một môi trường container hóa được phơi ra qua REST API.
- Phần về mạng đã dạy tôi cách các microservices thực sự giao tiếp, vượt xa các kết nối URL đơn giản.

#### Một số hình ảnh sự kiện

![Người tham dự kiểm tra ví dụ Dockerfile trong hội thảo](/images/4-Events%20Participated/event2.1.jpg)

![Slide trình bày về kiến trúc mạng container](/images/4-Events%20Participated/event2.2.jpg)

> Sự kiện này đã cải thiện đáng kể sự hiểu biết của tôi về triển khai ứng dụng hiện đại và làm tôi nhận thức rõ hơn về hạ tầng cơ bản mà các mô hình ML của tôi dựa vào.
