> Tổng hợp từ "Ronin Engineer Roadmap (v2024.1)" và các syllabus: Fundamentals of Programming, Advanced Backend, System Design, Working Methodology, Kafka, Kubernetes.

> Mục tiêu: Học cùng với AI và đi từ người **chưa có nền tảng lập trình** đến trình độ **Senior / có khả năng thiết kế hệ thống lớn**, đủ tự tin phỏng vấn vị trí Junior → Senior/Solution Architect.
---
## 🗺️ Tổng quan lộ trình
 
| #   | Module                                    | Số buổi | Đối tượng phù hợp                                                    | Mục tiêu đạt được                                                      |
| --- | ----------------------------------------- | ------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| 0   | Fundamentals of Programming               | 30      | Chưa biết lập trình, sinh viên năm 1-3, chuyển ngành, fresher        | Nắm nền tảng Java, DB, Spring, Git → làm được web backend cơ bản       |
| 1   | Advanced Backend                          | 24      | Sinh viên năm cuối, dev 1-3 năm kinh nghiệm, không giới hạn ngôn ngữ | Thiết kế API/kiến trúc chuẩn, tối ưu DB, caching, security, K8s, CI/CD |
| 2   | System Design                             | 16      | Dev ≥3 năm kinh nghiệm, đã hoàn thành module 1                       | Thiết kế hệ thống phân tán quy mô lớn (Uber, Airbnb, Ví điện tử...)    |
| 3   | Working Methodology                       | 8       | Mọi cấp độ, đặc biệt người chuẩn bị phỏng vấn/xin việc               | Phương pháp làm việc hiệu quả, kỹ năng mềm, phỏng vấn                  |
| 4   | Kafka (CCDAK)                             | 18      | Dev ≥1 năm, làm việc/muốn tìm hiểu Kafka                             | Thành thạo Kafka, sẵn sàng thi chứng chỉ CCDAK                         |
| 5   | Kubernetes (CKAD)                         | 12      | Dev đã/muốn làm việc với K8s                                         | Thành thạo vận hành K8s, sẵn sàng thi chứng chỉ CKAD                   |
| 6   | DevOps & Observability *(mới bổ sung)*    | 14      | Dev ≥1-2 năm, đã hoàn thành Module 1                                 | Vận hành hệ thống trên cloud, giám sát/observability, bảo mật hạ tầng  |
| 7   | Advanced Topics *(optional, mới bổ sung)* | tự chọn | Dev muốn mở rộng theo hướng chuyên sâu                               | GraphQL, Data pipeline, DR, AI/LLM integration                         |

**Tổng thời lượng lõi (0→3): 78 buổi** — đây là trục chính bắt buộc theo thứ tự.

**Module 4 (Kafka), 5 (Kubernetes), 6 (DevOps & Observability)** là các nhánh chuyên sâu, học sau khi hoàn thành Module 1 (Advanced Backend), có thể học song song hoặc chọn theo định hướng cá nhân.

**Module 7 (Advanced Topics)** là các chủ đề mở rộng, học khi đã vững Module 0-2 và có nhu cầu cụ thể.

Con đường sự nghiệp sau khi hoàn thành: **Software Architect / Solution Architect / Enterprise Architect**.

---
## 0️⃣ Module 0 — Fundamentals of Programming (30 buổi)

**Nội dung:** kiến thức nền tảng lập trình, Java Core, cấu trúc dữ liệu, giải thuật, database, framework Spring, công cụ làm việc.

| Nhóm        | Chủ đề             | Buổi | Nội dung chính                                                                                 |
| ----------- | ------------------ | ---- | ---------------------------------------------------------------------------------------------- |
| Programming | Programming Basics | 6    | Biến, kiểu dữ liệu, cấu trúc dữ liệu, vòng lặp, mảng, chức năng, phân biệt tham trị/tham chiếu |
|             | Java Core ⚡        | 4    | Class, Static, Final, OOP, JVM hoạt động thế nào, GC hoạt động thế nào, ưu nhược điểm Java     |
|             | Data Structures    | 3    | Stack, Queue, Linked List, Map, Tree                                                           |
|             | Algorithms ⚡       | 3    | Sorting, DFS, BFS, Two Pointers, Sliding Window                                                |
|             | File Processing    | 1.5  | Mở/đóng file, xử lý file, xử lý luồng                                                          |
|             | UML Diagramming    | 0.5  | Sequence Diagram, Activity Diagram, Data Flow Diagram                                          |
| Database    | MySQL              | 1    | Kiểu dữ liệu, thiết kế bảng                                                                    |
|             | SQL Functions      | 0.5  | Sum, Average, Concat...                                                                        |
|             | Join               | 0.5  | Các kiểu join, ưu nhược điểm, khi nào dùng join/nested query                                   |
| Framework   | Spring             | 3    | IoC, Dependency Injection, Spring Boot, Spring MVC, Spring Retry                               |
|             | ORM ⚡              | 2    | JPA, JDBC, One-To-One, One-To-Many                                                             |
|             | CRUD               | 1    | RESTful API, xử lý ngoại lệ tập trung                                                          |
| Tools       | Git ⚡              | 1    | Basic commands, Git Workflow, resolve conflicts                                                |
|             | Editor/IDE         | 0.5  | Keymap để code nhanh hơn                                                                       |
|             | Postman            | 0.5  | Collection structure, env var, script                                                          |
| Assignments | Weekly + Final     | 2    | Extract customer từ log file, xây dựng hệ thống đặt phòng khách sạn, câu hỏi phỏng vấn         |

🎯 **Đầu ra:** trở thành Junior Developer, có thể tự xây dựng ứng dụng web theo yêu cầu.

---
## 1️⃣ Module 1 — Advanced Backend (24 buổi)

*Khai giảng dự kiến: 27/09/2024 — dạy kỹ thuật nâng cao, bài toán thực tế. Đối tượng: sinh viên năm cuối / dev 1-3 năm kinh nghiệm, không giới hạn ngôn ngữ.*

| Nhóm                  | Chủ đề                                                             | Buổi | Nội dung chính                                                                                                                               |
| --------------------- | ------------------------------------------------------------------ | ---- | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Web App               | API Design                                                         | 1    | Mindset thiết kế, convention, Async API, Sorting, Relations, Clean API Docs                                                                  |
|                       | Project Structure & Architecture                                   | 1    | Hexagonal Architecture, Clean Architecture, Functional Architecture, DDD                                                                     |
|                       | Caching                                                            | 2    | Caching Strategies, Challenges, Redis Architecture, Data Structures, best practices scale                                                    |
|                       | Security                                                           | 1    | Attack types & prevention, Authentication (Basic, Cookie, JWT, OAuth2.0), Authorization (RBAC, PBAC)                                         |
|                       | **Security nâng cao** 🆕                                           | 1    | OWASP Top 10 (SQL Injection, XSS, CSRF, SSRF...), Secrets Management (Vault/AWS Secrets Manager), Encryption at rest/in transit, mTLS        |
|                       | **Service Communication** 🆕                                       | 1.5  | gRPC & Protocol Buffers, Service Discovery, API Gateway pattern, BFF (Backend For Frontend)                                                  |
| Dev Practices         | Development & Deployment Principles                                | 1    | SOLID, KISS, DRY, Twelve-factor app, why abstraction                                                                                         |
|                       | Design Patterns                                                    | 1    | Factory, Template, Strategy, Observer                                                                                                        |
|                       | Clean Code                                                         | 1    | Objectives, cách viết clean code                                                                                                             |
|                       | Code Review                                                        | 0.25 | Types of review, process, resolve conflicts                                                                                                  |
|                       | Datetime                                                           | 0.5  | Khi nào dùng timestamp, datetime, best practices                                                                                             |
|                       | Regex ⚡                                                            | 1    | Group, Flags, Look Around, Case Studies                                                                                                      |
| Advanced Database     | Design, Index, Join, Transaction ⚡, Partition, View, Anti-patterns | ~3   | Thiết kế bảng scalable, cách index/execution plan, cách transaction hoạt động, isolation level, locking, partition, anti-pattern SQL         |
| Network               | Fundamentals ⚡ / Protocol                                          | 1.5  | OSI Model, Network Topology, Socket, TCP/UDP, SSL/TLS, HTTPS, Long Polling, Websocket, SSE                                                   |
| Integration           | Case study VNPay Payment Gateway                                   | –    | Tích hợp thanh toán thực tế                                                                                                                  |
| Operation             | OS / Containerization / Kubernetes ⚡ / CI/CD                       | 5    | Kernel, Memory Management, File System, Docker vs VM, Docker Compose, K8s Architecture, Pod/Service/Ingress/HPA, CI/CD pipeline chuẩn        |
| Testing               | Unit Testing / Load Testing                                        | 2    | Good Unit Test, Coverage Metrics, Mock vs Stub, K6, chiến lược load test                                                                     |
|                       | **Testing nâng cao** 🆕                                            | 1    | Integration Testing, Contract Testing (Pact), Testcontainers                                                                                 |
| Database Ops          | **Migration & Deployment Strategy** 🆕                             | 1    | Database Migration tools (Flyway, Liquibase), Blue-Green Deployment, Canary Release, Feature Flags                                           |
| Soft Skills (offline) | Viết CV, xử lý stress, đàm phán lương, problem solving             | 3    |                                                                                                                                              |
| Assignments           | Weekly + Final                                                     | 2    | Export file lớn, tag/tái sắp xếp bảng, multi-language, cache local, JWT auth flow, SSO cho 2 web app, task scheduling, Flight Booking System |

🎯 **Đầu ra:** đủ kiến thức apply vị trí Middle/Senior.

---
## 2️⃣ Module 2 — System Design (16 buổi)

*Đối tượng: dev ≥3 năm kinh nghiệm hoặc đã hoàn thành Module 1. Kỹ năng cần thiết cho vị trí Senior/Solution Architect.*

| Nhóm                        | Chủ đề                                             | Buổi | Nội dung chính                                                                          |
| --------------------------- | -------------------------------------------------- | ---- | --------------------------------------------------------------------------------------- |
| Requirement Analysis        | Functional/Non-functional Requirements, Estimation | 1    | Cần thu thập thông tin gì, cách đặt câu hỏi, throughput, storage, caching               |
| Design Principles           | Laws, CAP, Handling trade-offs                     | 1    | Why not How, Consistency ACID vs CAP, priority/separation                               |
| Architectural Foundations   | Monolithic vs Distributed, Architecture Styles ⚡   | 1.5  | Layered, Microkernel, Event-Driven, Microservices                                       |
| Database                    | Scaling relational DB, chọn đúng loại DB           | 0.5  | High read/write load, SQL vs NoSQL, Wide-columnar vs Column-Oriented                    |
| Async Communication         | Async, Kafka ⚡                                     | 2.5  | Message Queue, Pub/Sub, Architecture, Message Flow, Partition, Consumer Group           |
| Architectural Patterns      | Data Management, Reliability                       | 2    | CQRS, Event Sourcing, TC/C vs Saga, Retry, DLQ, Circuit Breaker, Graceful Shutdown      |
|                             | **Idempotency & Concurrency Control** 🆕           | 1    | Idempotency Key trong thiết kế API, Distributed Locking (Redis Redlock, Zookeeper/etcd) |
|                             | **Message Serialization** 🆕                       | 0.5  | Avro, Protobuf, Schema Registry (đi kèm Kafka)                                          |
| Algorithm & Data Structures | –                                                  | 1    | Consistent Hashing, Bloom Filter, Trie, LSM                                             |
| Infrastructure Patterns     | **CDN & Load Balancing** 🆕                        | 1    | CDN, thuật toán LB (Round Robin, Least Connections, Consistent Hashing) áp dụng thực tế |
|                             | **Search Engine** 🆕                               | 1    | Elasticsearch/full-text search, inverted index, khi nào cần search engine riêng         |
| Visualization               | Diagramming, Presenting                            | 1    | Diagramming Tools, C4 Model, best practices                                             |
| Labs ⚡                      | Thiết kế thực tế                                   | 2.5  | URL Shortener, Airbnb, Digital Wallet, Fraud Detector, Real-time Leaderboard            |
| Technical Problems          | Scalability ⚡, Reliability, Concurrency            | 2.5  | Bottleneck, lag message, exactly-once, deadlock, cache eviction                         |
| Assignments                 | Weekly                                             | –    | Uber/Grab system, Rate Limiter, S3 Object Storage, Ad Click Reporter                    |
🎯 **Đầu ra:** thiết kế được hệ thống lớn, tư duy như một Solution Architect.

---
## 3️⃣ Module 3 — Working Methodology (8 buổi)

*Dành cho mọi cấp độ, đặc biệt hữu ích khi chuẩn bị phỏng vấn/xin việc.*

| Nhóm                  | Chủ đề                                              | Buổi | Nội dung chính                                      |
| --------------------- | --------------------------------------------------- | ---- | --------------------------------------------------- |
| Problem Solving ⚡     | Định nghĩa vấn đề, cách tiếp cận, trade-off         | 1    |                                                     |
| Procedure             | 20-Minute Rule, Planning, Personal Radar            | 0.5  |                                                     |
| Resources             | Cách tìm & đọc tài liệu, sách                       | 0.5  |                                                     |
| Soft Skills           | Presentation, Leadership, Communication, Behavior ⚡ | 2.5  | Rule of Three, top-down, focus on target            |
| Interview Preparation | CV Review ⚡, Self Introduction, Mocking Interview   | 3.5  | Cấu trúc CV, cách gây ấn tượng, luyện phỏng vấn thử |
🎯 **Đầu ra:** phương pháp làm việc hiệu quả, sẵn sàng phỏng vấn ở mọi cấp bậc.

---
## 4️⃣ Module 4 (nhánh chuyên sâu) — Kafka / CCDAK (18 buổi)
 
 *Khai giảng dự kiến: 22/03/2024. Đối tượng: dev ≥1 năm kinh nghiệm, đã/muốn làm việc với Kafka.*
- **Message Broker & Core Concepts** (3 buổi): Kafka Introduction, Setup, Producer, Consumer
- **Pet Project**: Fraud Detection
- **Best Practices** (1 buổi): Recommended Configurations, Message Format
- **Why Kafka?** (1.5 buổi): cách chọn message broker, hiệu năng, độ tin cậy
- **Group Membership** (1 buổi): Partition Assignment, Liveness
- **Problems & Patterns** (3 buổi): Error Handling, Delay Queue, Large Message, Message Lag, Request-response, Exactly-once, Message Ordering
- **Security** (1 buổi)
- **CCDAK Exam Prep** (1 buổi): Tips, Dumps

🎯 **Đầu ra:** sẵn sàng thi chứng chỉ Confluent CCDAK.
 
---
## 5️⃣ Module 5 (nhánh chuyên sâu) — Kubernetes / CKAD (12 buổi)
*Đối tượng: dev đã/muốn làm việc chuyên sâu với Kubernetes.*
- **Kubernetes Architecture** (0.5 buổi)
- **Workloads** (1.5 buổi): Pod, Job, ReplicaSet, Deployment
- **Configuration** (0.25 buổi): ConfigMap, Secret
- **Networking ⚡** (2 buổi): Service, Ingress, KubeDNS, Network Policy
- **Storage** (0.75 buổi): PV, PVC
- **Autoscaler** (0.5 buổi): HPA, Keda
- **Security** (0.5 buổi): Pod Security, Service Account
- **Troubleshooting ⚡** (1.5 buổi): Scheduling, Resource Management, Pod Lifecycle
- **Best Practices, CKAD Tips, Dumps** (2 buổi), **Labs** (2.5 buổi)

🎯 **Đầu ra:** sẵn sàng thi chứng chỉ CKAD (Certified Kubernetes Application Developer).
 
---
## 6️⃣ Module 6 (nhánh chuyên sâu, mới bổ sung) — DevOps & Observability (14 buổi)

*Đối tượng: dev đã hoàn thành Module 1, muốn vững vận hành hệ thống thực tế trên production. Đây là mảng gần như thiếu hoàn toàn trong roadmap gốc nhưng rất hay bị hỏi ở vòng phỏng vấn Senior.*

| Nhóm               | Chủ đề                       | Buổi | Nội dung chính                                                                           |
| ------------------ | ---------------------------- | ---- | ---------------------------------------------------------------------------------------- |
| Cloud Fundamentals | Cloud cơ bản (AWS/GCP/Azure) | 3    | IAM, VPC/Networking, S3/Object Storage, Load Balancer, Auto Scaling Group                |
|                    | Infrastructure as Code       | 2    | Terraform hoặc CloudFormation, quản lý hạ tầng dạng code                                 |
| Observability      | Logging tập trung            | 1.5  | ELK/EFK stack, structured logging, correlation ID                                        |
|                    | Metrics & Monitoring         | 1.5  | Prometheus, Grafana, các loại metrics cần theo dõi                                       |
|                    | Distributed Tracing          | 1.5  | OpenTelemetry, Jaeger/Zipkin, trace 1 request qua nhiều service                          |
|                    | Alerting & SLO               | 1    | SLO/SLI/SLA, thiết kế alerting hiệu quả, tránh alert fatigue                             |
| Security hạ tầng   | Secrets & Network Security   | 1.5  | Vault/Secrets Manager (mở rộng), Network Policy, mTLS ở tầng hạ tầng                     |
| Service Mesh       | Service Mesh (Istio)         | 1.5  | Traffic management, mTLS tự động, observability tích hợp — cần cho Solution Architect    |
| Assignment         | Final Assignment             | 1    | Dựng full observability stack (log + metric + trace) cho 1 hệ thống microservices có sẵn |

🎯 **Đầu ra:** tự tin vận hành, giám sát và debug hệ thống production ở quy mô thực tế.

---
## 7️⃣ Module 7 (mở rộng, tùy chọn) — Advanced Topics

*Không có thứ tự buổi cố định — chọn học theo định hướng công việc/công ty cụ thể. Phù hợp sau khi đã vững Module 0-2.*

| Chủ đề                           | Khi nào cần                                       | Nội dung chính                                                                          |
| -------------------------------- | ------------------------------------------------- | --------------------------------------------------------------------------------------- |
| GraphQL                          | Công ty dùng GraphQL thay REST                    | Schema, Resolver, N+1 problem, so sánh với REST                                         |
| Data Pipeline / ETL cơ bản       | Hướng data-heavy system                           | Batch vs Stream processing, công cụ ETL phổ biến, data warehouse cơ bản                 |
| Multi-region & Disaster Recovery | Hướng Solution/Enterprise Architect               | Backup strategy, failover, RTO/RPO, multi-region deployment                             |
| AI/LLM Integration cơ bản        | Xu hướng 2025-2026, nhiều JD backend hiện yêu cầu | RAG (Retrieval-Augmented Generation), Vector Database, gọi LLM API vào hệ thống backend |

---
## 📅 Lịch học đề xuất (tham khảo, 3 buổi/tuần)

| Giai đoạn               | Thời gian ước tính | Module                                                                                                            |
| ----------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------- |
| Giai đoạn 1             | ~10 tuần           | Module 0 – Fundamentals                                                                                           |
| Giai đoạn 2             | ~8 tuần            | Module 1 – Advanced Backend                                                                                       |
| Giai đoạn 3 (song song) | ~5-7 tuần          | Chọn 1-2 nhánh: Module 4 (Kafka), Module 5 (K8s), Module 6 (DevOps & Observability) — theo định hướng             |
| Giai đoạn 4             | ~5-6 tuần          | Module 2 – System Design                                                                                          |
| Giai đoạn 5             | ~3 tuần            | Module 3 – Working Methodology (nên làm song song/xen kẽ trong suốt quá trình học, đặc biệt trước khi apply việc) |
| Giai đoạn 6 (tùy chọn)  | linh hoạt          | Module 7 – Advanced Topics, học khi công việc thực tế yêu cầu                                                     |

> Gợi ý: bắt đầu luyện **Interview Preparation** và cập nhật CV ngay từ giữa Module 1, không đợi đến cuối lộ trình.

---
## ✅ Cách đánh giá kết quả học tập

1. **Bài tập tuần (Weekly Assignments)** — làm ngay sau mỗi buổi học để củng cố kiến thức.
2. **Bài tập lớn cuối module (Final Assignment)** — mô phỏng dự án thực tế (VD: hệ thống đặt phòng khách sạn, Flight Booking System, Uber/Grab system...).
3. **Câu hỏi phỏng vấn (Interview Questions)** cuối mỗi module để tự kiểm tra mức độ hiểu sâu.
4. **Labs thực hành** ở Module 2, 4, 5 — thiết kế/triển khai hệ thống con cụ thể.
5. **Mock Interview** ở Module 3 để tổng duyệt trước khi phỏng vấn thật.
6. (Tuỳ chọn) **Thi chứng chỉ** CCDAK (Kafka) và/hoặc CKAD (Kubernetes) để có bằng chứng năng lực chính thức.

---
## 🧭 Định hướng nghề nghiệp sau khi hoàn thành
Hoàn thành trục chính (Module 0→3) + ít nhất 1 nhánh chuyên sâu (Kafka hoặc Kubernetes), bạn có nền tảng để phát triển theo 3 hướng:

- **Software Architect** — chuyên sâu thiết kế phần mềm, clean architecture, design pattern
- **Solution Architect** — chuyên sâu thiết kế hệ thống phân tán, tích hợp nhiều dịch vụ
- **Enterprise Architect** — chuyên sâu chiến lược công nghệ ở cấp độ tổ chức
