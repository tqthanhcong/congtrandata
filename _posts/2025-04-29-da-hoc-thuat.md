---
layout: post
title: "DA và researcher"
date: 2025-04-22 23:45:13 -0400
background: '/img/posts/02.jpg'
category: DA
---

# Từ người kể chuyện dễ hiểu đến kẻ đào quá sâu — Và bài học về "luật chơi" của Data Analyst

> *“Everything should be made as simple as possible, but not simpler.”* — Albert Einstein

### 1. Khởi đầu ở ngân hàng: Nhịp chậm và nỗi lo về giả định

Tôi bắt đầu sự nghiệp Data Analyst trong một ngân hàng — nơi mọi thứ vận hành chậm rãi và đầy thận trọng. Ở đó, một báo cáo phân tích không cần đẹp, nhưng bắt buộc phải đúng. Chúng tôi có thể dành hàng giờ chỉ để tranh luận về giả định phía sau một chỉ số tài chính: *“Tại sao đoạn này dùng duration gap chứ không phải cash flow gap?”*, hay *“Chỉ số này có còn đúng khi mặt bằng lãi suất dịch chuyển?”*

Môi trường đó rèn cho tôi một nếp nghĩ căn bản: Phân tích dữ liệu không phải là nhìn vào con số rồi phán, mà là hiểu hệ thống tư tư tưởng đứng sau con số đó. Bất kỳ chỉ số nào xuất hiện cũng phải trả lời được ba câu hỏi:

1. Nó thực sự phản ánh điều gì?
2. Nó dựa trên những giả định nào?
3. Khi bối cảnh thay đổi, nó có còn đúng không?

---

### 2. Sang công ty công nghệ: Lợi thế của sự "dễ hiểu"

Chuyển sang làm ở một công ty công nghệ, nhịp làm việc thay đổi hẳn: nhanh hơn, thực dụng hơn và áp sát vào bài toán kinh doanh. Dù xuất phát điểm khác biệt, tôi lại thích nghi rất nhanh.

Những bản phân tích của tôi — nhờ ngắn gọn, rõ ràng và mạch lạc — được các team kinh doanh đón nhận nhiệt tình. Phản hồi phổ biến nhất tôi nhận được là: *“Từ ngày có em, slide phân tích nhìn dễ hiểu hơn hẳn.”*

Tôi cảm thấy mình có giá trị. Và bắt đầu tin rằng **“diễn giải dễ hiểu”** chính là lợi thế cạnh tranh lớn nhất của mình.

---

### 3. Cái bẫy "sợ sai" và chặng đường sa đà vào Causal Inference

Mọi chuyện bắt đầu thay đổi khi tôi nhận được phản hồi từ những bạn analyst khác trong team:

* *“Cái này bị bias nhiều lắm đó.”*
* *“Em chưa kiểm soát được các yếu tố nhiễu (confounders).”*
* *“Correlation này chưa chắc đã là Causal nha.”*

Ban đầu, tôi hơi dội. Nhưng rồi tôi khựng lại — vì chính tôi ngày xưa, hồi còn ở ngân hàng, cũng từng soi xét đồng nghiệp bằng những câu y hệt như thế. Tâm lý lo sợ trỗi dậy: *“Nếu không cẩn thận, mình sẽ đưa ra phân tích sai và làm người khác ra quyết định hỏng.”*

Tôi bắt đầu lao vào học Causal Inference một cách nghiêm túc. Không phải để đùa đòi theo trend, mà vì **sợ**. Tôi sợ mình vô tình bỏ qua một biến quan trọng nào đó.

Tôi đọc về DAGs, collider, overcontrol, selection bias, do-calculus. Tôi đăng ký học Thạc sĩ Thống kê, đọc paper chuyên ngành, mày mò từ Propensity Score Matching đến Instrumental Variables (IV). Tôi không có ý định trở thành một researcher chuyên nghiệp; tôi chỉ đơn thuần không muốn trở thành kẻ đưa ra thông tin sai lệch.

Đúng lúc đó, công ty bước vào giai đoạn “data maturity” — ban lãnh đạo bắt đầu đòi hỏi các phân tích bài bản, chặt chẽ, bớt cảm tính. Tôi tự thấy mình đang đi rất đúng hướng.

---

### 4. Gáo nước lạnh: Khi sự kỹ lưỡng trở thành rào cản

Cho đến một ngày, tôi nhận gáo nước lạnh từ một chị manager:

* *“Em làm công phu thật, nhưng chị đọc xong không biết phải chốt thế nào.”*
* *“Chiến dịch sắp chạy rồi, chị cần nhanh hơn. Tóm lại cho chị 3 gạch đầu dòng được không?”*
* *“Em nói lại theo cách hồi xưa em hay nói đi. Hồi đó em giải thích dễ hiểu lắm mà.”*

Tôi ngẩn người.

Tôi nhận ra mình đã biến thành chính hình mẫu đồng nghiệp mà tôi từng không thích trước đây: một người quá academic, báo cáo lúc nào cũng dày đặc assumption, mô hình, trích dẫn, nhưng cuối cùng người cần dùng lại chẳng hiểu gì.

Trong nỗi sợ làm người khác hiểu sai, tôi đã mắc một sai lầm căn bản hơn: **nói bằng thứ ngôn ngữ mà không ai hiểu.** Stakeholder không phải là Data Analyst. Họ không sống trong nỗi sợ bỏ sót confounder hay vi phạm giả định ignorability. Họ chỉ cần trả lời câu hỏi: *Có nên chạy tiếp chiến dịch này hay không?*

---

### 5. Mỗi tổ chức một "luật chơi" — Bài học cho một DA trưởng thành

Chuyển sang công ty thứ ba — một môi trường vận hành cực nhanh, dữ liệu nhiều tầng lớp và quyết định phải đưa ra liên tục — tôi mới định hình rõ ràng: **Không có một phương pháp phân tích "chuẩn mực" cho mọi tình huống.** Mỗi tổ chức, mỗi giai đoạn đều có một "luật chơi" riêng.

Dưới đây là những bài học tôi rút ra sau nhiều lần tự thấy mình sai:

#### 1. Đừng chỉ giỏi kỹ thuật, hãy giỏi "dịch ngôn ngữ"

Một chị Marketing Manager sẽ không bao giờ bảo bạn: *“Em chạy Inverse Probability Weighting để xử lý selection bias giùm chị.”*
Chị ấy sẽ nói: *“Chị thấy nhóm A ngon hơn nhóm B, nhưng không biết có phải do chương trình khuyến mãi không. Em xem giùm chị.”*

Nhiệm vụ của bạn là dịch từ yêu cầu cảm tính đó sang bài toán dữ liệu, chạy phân tích, rồi dịch kết quả ngược lại thành một khuyến nghị đơn giản, dễ hành động. Người ta không thuê Data Analyst để chứng tỏ mình thông minh. Họ thuê bạn để giúp họ ra quyết định thông minh hơn.

#### 2. Học từ học thuật, nhưng đừng "lậm" học thuật

Tôi từng mất hàng tuần để chỉnh một báo cáo vì phát hiện có nguy cơ dính collider bias. Nhưng thực tế là: trong bối cảnh chiến dịch đó, sai số do bias gây ra là rất nhỏ, còn việc trễ hạn báo cáo sẽ khiến họ ra quyết định hoàn toàn bằng cảm tính vì không thể chờ thêm.

Làm DA không phải là vẽ một bản đồ địa lý chính xác đến từng milimet, mà là chỉ đường cho người khác đi đúng hướng — càng nhanh và rõ ràng càng tốt.

#### 3. Biết chọn "trận" mà đánh

* Có những bài toán đòi hỏi tư duy của một Researcher: sâu, chặt chẽ, kiểm tra giả định kỹ càng.
* Có những bài toán chỉ cần phản ứng nhanh: gọn, rõ, chấp nhận sai số nhỏ để giữ tốc độ.

Nếu business chỉ yêu cầu đánh giá hiệu quả của một đợt push notification trong 3 ngày, bạn không cần dựng mô hình Causal rườm rà. Một so sánh nhóm căn bản kết hợp vài bước kiểm tra logic (sanity check) là đủ để đưa ra lời khuyên. Sự trưởng thành nằm ở chỗ biết khi nào dùng súng lớn, khi nào chỉ cần dùng dao gọt trái cây.

#### 4. Luôn tự hỏi: "Nếu là mình, mình có dám chốt hạ dựa trên slide này không?"

Đặt mình vào vị trí của người ra quyết định sẽ giúp bạn biết cái gì cần làm rõ, cái gì thừa thãi, và kết quả hiện tại đã đủ thuyết phục để xuống tiền/xuống lực hay chưa.

#### 5. Định vị bản thân: Analyst hay Researcher?

Thỉnh thoảng hãy tự hỏi: *“Ranh giới làm việc của mình tuần này đang thiên về Analyst hay Researcher?”*

* Nếu làm **Analyst** mà báo cáo viết như một bài báo nghiên cứu academic — bạn đang rời xa business.
* Nếu làm **Researcher** mà phân tích hời hợt như một bài slide trình diễn — bạn đang làm sai vai.

Giữ được sự cân bằng giữa **độ sâu (rigor)** và **sự rõ ràng (clarity)** chính là năng lực cốt lõi giúp một Data Analyst đi xa trong nghề.
