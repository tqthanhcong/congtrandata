---
layout: post
title: "DA và researcher"
date: 2025-04-22 23:45:13 -0400
background: '/img/posts/02.jpg'
category: DA
---

> *“Everything should be made as simple as possible, but not simpler.”* 
> — Albert Einstein
---

## Hành trình từ chàng báo cáo viên ngân hàng, đến kẻ học thuật quá đà – và cú tỉnh ngộ về sức mạnh của sự dễ hiểu

Tôi bắt đầu sự nghiệp làm data analyst trong một ngân hàng. Mọi thứ ở đây diễn ra chậm và kỹ. Chúng tôi được kỳ vọng phải hiểu sâu về bản chất của từng chỉ số – đặc biệt là những chỉ số dùng trong quản lý tài chính và rủi ro như trong ALM (Asset-Liability Management).  

Tôi còn nhớ có những buổi họp kéo dài chỉ để tranh luận: "Tại sao lại dùng duration gap thay vì cash flow gap?", "Chỉ số này có phản ánh đúng thanh khoản thực sự không?". Và chính ở môi trường ấy, tôi học được cách đặt câu hỏi đúng – không chỉ “chỉ số ra sao?” mà là “nó phản ánh điều gì?”, “nó được xây dựng trên giả định gì?”, “khi bối cảnh thay đổi, nó có còn đúng không?”. Đó là nền tảng đầu tiên của tôi – một nền tảng tuy chậm nhưng sâu sắc.

Rồi tôi chuyển sang làm DA cho một công ty công nghệ. Mọi thứ ở đây nhanh hơn, áp lực hơn, và định hướng *business-driven* rõ rệt. Nhưng thật ngạc nhiên, tôi lại cảm thấy “vào form” rất nhanh. Những phân tích của tôi – vì rõ ràng, logic, dễ hiểu – được các team business rất đón nhận. Họ bảo tôi làm mọi thứ “dễ hiểu hơn bao giờ hết”. Tôi thấy vui. Tôi thấy mình hữu dụng.

Nhưng rồi… cũng chính khi mọi thứ đang suôn sẻ, tôi bắt đầu nhận được một số feedback từ những người trong các team DA khác:  
“Phân tích của bạn bias nhiều đó.”  
“Bạn chưa kiểm soát được confounders.”  
“Phải cẩn thận, vì correlation này chưa chắc causal.”

Ban đầu tôi hơi phản ứng. Nhưng rồi, tôi nhớ mình từng nói những câu y chang như vậy với một đồng nghiệp trước đây – một người cũng rất giỏi nhưng làm mọi thứ quá “storytelling”, quá cảm tính. Lúc đó tôi từng nghĩ: “Làm vậy là misleading người khác.”

Và thế là, tôi dừng lại và suy nghĩ nghiêm túc. Biết đâu họ đúng?

Tôi bắt đầu tìm hiểu nghiêm túc về **causal inference**. Lúc đó, tôi như được mở mắt lần nữa. Tôi bị cuốn vào những khái niệm như selection bias, confounding, overcontrol, collider. Tôi đọc sách, đọc blog, đọc cả những thread dài lê thê trên Twitter. Rồi tôi biết đến DAGs, thấy chúng đẹp như sơ đồ tư duy cho những người thích đặt câu hỏi "vì sao". Tôi học cách dùng *do-calculus*, đọc paper về propensity score, và thử nghiệm tất cả mọi thứ từ matching, inverse weighting, cho tới instrumental variables.  

Không dừng lại ở đó, tôi còn đăng ký học thạc sĩ ngành thống kê. Phần vì muốn hiểu sâu hơn, phần vì tôi bắt đầu cảm thấy… nghi ngờ chính mình. Phân tích của mình từ trước giờ có bias không? Mình có từng khiến ai ra quyết định sai không?  

Công ty lúc ấy cũng đang trong giai đoạn "chín" về mặt dữ liệu – họ bắt đầu quan tâm hơn tới những phân tích *causal*, những chiến lược dài hạn thay vì các insight mang tính ad-hoc. Tôi cảm thấy mình phù hợp hơn bao giờ hết. Tôi dành hàng giờ để viết memo, vẽ DAG, viết các cảnh báo về giả định, mô phỏng kết quả dưới các kịch bản sensitivity khác nhau.

Nhưng rồi một ngày… tôi tỉnh ra.

Tôi nhận được feedback từ chính team tôi:  
“Bài phân tích này em làm công phu thật nhưng khó hiểu quá chị không dám action.”  
“Chị đọc mà rối… em có thể tóm gọn giúp chị không?”  
“Chị vẫn không rõ cuối cùng mình nên làm gì tiếp theo.”

Cú đau nhất là khi một người chị hỏi tôi:  
“Em có thể nói như lúc trước em vẫn hay nói không? Em từng làm mọi thứ dễ hiểu lắm mà.”  
Và tôi nhận ra: mình đã đi quá xa.

Tôi nhớ lại, ngày xưa tôi từng nói đúng những câu ấy với một đồng nghiệp – người làm rất mạnh về stats nhưng nói chuyện như viết luận án. Tôi từng nói với anh ấy rằng: “Insight mà người khác không hiểu, thì không còn là insight nữa.”

Và giờ tôi đã trở thành phiên bản đó – một người nói toàn những khái niệm như ignorability assumption, identification strategy, sensitivity bounds… mà quên mất mình đang làm việc với những người không học stats như mình.

Tôi nhận ra: **tri thức mà không đi kèm sự dễ hiểu – thì nó không còn giá trị hành động**.

---

## Researcher và Data Analyst: cùng là phân tích, nhưng mục tiêu khác nhau

Tôi rút ra một điều sâu sắc: researcher và data analyst *làm việc khác nhau, vì sống trong hai thế giới khác nhau*.

**Researcher** sống trong thế giới của *chân lý* – tìm ra cái gì là đúng, bất kể tốn bao lâu.  
**Data analyst** sống trong thế giới của *quyết định* – làm sao đủ đúng để dám làm tiếp, càng nhanh càng tốt.

Trong giới học thuật, bạn sẽ được thưởng vì làm nghiên cứu chặt chẽ, mô hình đẹp, giả định rõ ràng, kết luận trung thực dù là “không có gì đáng kể”. Thậm chí nếu bạn chứng minh điều gì đó là “không causal”, bạn vẫn được công nhận – vì bạn làm đúng quy trình.  

Còn trong công ty? Nếu bạn mất 2 tuần để ra một báo cáo mà không ai hiểu, không ai dám dùng, thì công phu đến đâu cũng trở nên vô nghĩa.

**Researcher được phép không ra quyết định. Data analyst thì không.**

---

## Vậy một data analyst nên làm gì để sống sót và phát triển?

1. **Học từ học thuật, nhưng không lậm học thuật**. Biết bias là gì, biết causal là gì – nhưng cũng biết khi nào cần buông bỏ sự hoàn hảo để đưa ra hành động. Không phải cái gì cũng cần RCT.

2. **Kể chuyện giỏi như một người viết sách cho thiếu nhi**. Nếu bạn không thể giải thích phân tích của mình cho một người bạn không học stats – bạn chưa thực sự hiểu nó. Và bạn sẽ không thay đổi được ai.

3. **Luôn hỏi: phân tích này giúp người ta ra quyết định gì?** Nếu không giúp ai làm gì khác đi – thì dù kết quả có “đẹp” tới đâu, nó cũng không có giá trị trong thực tế.

---

Vậy đó, tôi chia sẻ câu chuyện này như một lời tự nhắc: Hãy tiếp tục học, tiếp tục đào sâu. Nhưng đừng quên rằng, giá trị lớn nhất của dữ liệu – là khi nó được **hiểu**, **tin**, và **dùng để hành động**.

Tuyệt, dưới đây là phần bổ sung — **"Bí quyết để DA sống sót và phát triển vượt bậc trong công ty"** — nối mạch logic và giọng văn từ bài trước:

---

## Bí quyết để một DA không chỉ sống sót – mà còn phát triển vượt bậc trong môi trường business

Sống sót là một chuyện. Nhưng để **vượt trội**, bạn cần hơn cả kỹ năng kỹ thuật. Dưới đây là những điều tôi học được – đôi khi là sau nhiều va vấp:

### 1. **Luôn giữ đầu óc “hai tầng”**  
Một tầng nghĩ như researcher: nghi ngờ, thận trọng, biết bias nằm ở đâu.  
Tầng còn lại nghĩ như business: nếu là mình, mình có dám action không? Có thể simplify xuống mức nào? Cần kết luận nhanh cỡ nào?

**Nghĩ cả hai tầng cùng lúc chính là đỉnh cao của một DA trưởng thành.**

---

### 2. **Biết khi nào cần chính xác, khi nào cần nhanh**  
Không phải phân tích nào cũng cần causal. Không phải phân tích nào cũng nên dùng mô hình machine learning. Quan trọng là biết:  
- Bối cảnh này cần độ tin cậy bao nhiêu phần trăm?  
- Action là lớn hay nhỏ?  
- Rủi ro nếu sai là gì?

**Tài năng thật sự là biết chọn đúng công cụ cho đúng tình huống – không phải lúc nào cũng mang dao mổ trâu đi chém gà.**

---

### 3. **Biết lắng nghe và “dịch” vấn đề**  
Người làm business sẽ không nói: “Tôi cần bạn chạy propensity score matching.”  
Họ sẽ nói: “Tôi muốn biết cái chiến dịch này có tác động thật không hay là trùng hợp.”  
Bạn cần học cách dịch yêu cầu – từ tiếng business sang tiếng dữ liệu, rồi từ kết quả dữ liệu ngược lại thành ngôn ngữ ra quyết định.

**Bạn là người “thông dịch” giữa thế giới số và thế giới người. Làm tốt vai trò đó, bạn sẽ không bao giờ bị thay thế.**

---

### 4. **Làm sản phẩm, không chỉ làm slide**  
Insight tốt là phải dùng được. Hãy nghĩ cách đóng gói phân tích của bạn thành:  
- Dashboard dùng hàng ngày  
- Alert tự động  
- Report định kỳ  
- Template để người khác tự phân tích sau này

**Khi bạn làm thứ người khác dùng được mà không cần bạn, lúc đó bạn thật sự có impact.**

---

### 5. **Cân bằng giữa tư duy độc lập và hợp tác**  
DA giỏi là người dám phản biện, dám đặt câu hỏi, không bị trôi theo hype. Nhưng đồng thời, cũng cần biết cách thuyết phục, cách nói chuyện để người khác muốn nghe, muốn hành động cùng mình.  

**Không ai đi một mình tới đỉnh. Và không ai được nhớ tới nếu chỉ đúng một mình.**

---

Bạn có muốn mình gom toàn bộ thành một bài hoàn chỉnh, chỉnh sửa lại cho mượt rồi đề xuất luôn tiêu đề, tagline, và hình ảnh minh họa cho bài đăng không?
