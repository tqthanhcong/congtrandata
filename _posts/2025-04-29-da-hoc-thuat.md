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

Tuyệt vời, cảm ơn bạn bổ sung! Dưới đây là phiên bản được viết lại với giọng văn mượt hơn, sắc sảo hơn, tập trung vào việc hiểu “luật chơi” của từng người, từng công ty. Mình cũng đã chỉnh lại các đoạn để diễn đạt rõ ràng việc bạn không sa đà vào causal inference, mà là bị cuốn vào cách nghĩ chính xác và phức tạp hơn do sợ hiểu sai. Những đoạn cuối về “luật chơi” cũng đã được mở rộng, đưa ví dụ cụ thể, sinh động hơn.

⸻

Từ người kể chuyện dễ hiểu, đến người đào quá sâu – và bài học về “luật chơi” của mỗi tổ chức

Tôi bắt đầu sự nghiệp data analyst trong một ngân hàng, nơi mọi thứ chậm rãi và thận trọng. Những phân tích ở đây không cần đẹp đẽ, chỉ cần đúng. Chúng tôi dành thời gian tranh luận về từng giả định phía sau một chỉ số tài chính: “Vì sao dùng duration gap chứ không phải cash flow gap?”, “Chỉ số này có còn hợp lý khi lãi suất thay đổi?”

Ở đó, tôi học được một điều quan trọng: Phân tích không chỉ là nhìn con số, mà phải hiểu được hệ thống tư duy đứng sau nó. Một thói quen hình thành từ những câu hỏi rất căn bản: Chỉ số này phản ánh điều gì? Được xây dựng trên giả định nào? Nếu bối cảnh thay đổi, nó có còn đúng không?

Rồi tôi chuyển sang công ty công nghệ. Mọi thứ nhanh hơn, thực dụng hơn, và hướng business rõ ràng. Nhưng lạ thay, tôi lại thích nghi rất nhanh. Phân tích của tôi – vì rõ ràng, logic, dễ hiểu – được các team đón nhận nồng nhiệt. Họ bảo: “Từ hồi có bạn, slide phân tích dễ hiểu hơn hẳn.”

Tôi thấy mình hữu dụng. Và có lẽ, tôi bắt đầu tin rằng “dễ hiểu” chính là lợi thế cạnh tranh lớn nhất của mình.

Nhưng rồi, tôi bắt đầu nghe những feedback từ các bạn analyst khác:
	•	“Bạn bias nhiều lắm đó.”
	•	“Bạn chưa kiểm soát được confounders.”
	•	“Correlation này chưa chắc causal nha.”

Ban đầu tôi phản ứng. Nhưng rồi tôi khựng lại – vì chính tôi từng nói những câu y hệt như vậy, ở ngân hàng. Lúc ấy tôi từng nghĩ: “Nếu không cẩn thận, mình sẽ làm người khác hiểu sai.”

Tôi bắt đầu học nghiêm túc về causal inference. Không phải vì trend. Mà vì tôi sợ. Tôi sợ mình đã từng phân tích sai, từng bỏ qua yếu tố quan trọng nào đó mà làm người khác hành động nhầm.

Tôi đọc DAGs, học về collider, về overcontrol, về selection bias, về do-calculus. Tôi đăng ký học thêm thạc sĩ ngành thống kê. Tôi đọc paper, vẽ đồ thị, thử nghiệm mọi thứ từ matching đến IV. Không phải tôi muốn thành researcher. Tôi chỉ không muốn làm người gây hiểu lầm.

Và đúng lúc đó, công ty tôi cũng bắt đầu bước vào giai đoạn “mature về dữ liệu” – leadership bắt đầu quan tâm đến phân tích nghiêm túc, tư duy dài hạn, less hype more rigor. Tôi cảm thấy rất đúng chỗ.

Cho đến một ngày – tôi nhận ra mình đã đi quá xa.

Một chị quản lý đọc báo cáo và bảo:
	•	“Em làm công phu thật, nhưng chị đọc xong không dám action.”
	•	“Chị rối quá… có thể tóm lại cho chị 3 gạch đầu dòng không?”
	•	“Em có thể nói lại như hồi trước em hay nói không? Em từng làm mọi thứ dễ hiểu lắm mà.”

Tôi ngớ người. Vì tôi chợt thấy mình… giống hệt một anh đồng nghiệp cũ: người mà tôi từng nghĩ là “quá academic”, phân tích gì cũng dùng assumption, biểu đồ, citation, nhưng cuối cùng chẳng ai hiểu gì.

Và tôi hiểu ra: Tôi đã quên mất rằng không phải ai cũng là data analyst.

Tôi làm mọi thứ phức tạp lên, vì tôi sợ sai. Tôi sợ làm người khác hiểu sai. Nhưng trong nỗi sợ ấy, tôi lại quên một điều đơn giản: không ai hiểu điều gì nếu mình không nói đúng ngôn ngữ của họ.

⸻

Mỗi công ty, mỗi người – đều có một “luật chơi” riêng

Tôi dần nhận ra: không có một “cách phân tích đúng” cho tất cả mọi nơi. Mỗi tổ chức có một logic vận hành riêng, một thứ “luật chơi ngầm” – và nếu không hiểu điều đó, bạn sẽ luôn cảm thấy mình “bị chê”, hoặc tệ hơn: “không được hiểu”.

Dưới đây là đoạn lời khuyên đã được viết lại theo yêu cầu: mở rộng hơn, đưa ví dụ sinh động hơn, và điều chỉnh theo trải nghiệm tại công ty thứ ba. Đồng thời bỏ chi tiết “không biết action sao”, thay bằng “chị cần nhanh hơn”:

⸻

Bí quyết để một DA không chỉ sống sót – mà còn phát triển vượt bậc trong môi trường business

Khi chuyển sang công ty thứ ba – một nơi vận hành nhanh, dữ liệu nhiều tầng lớp, quyết định ra liên tục – tôi mới thực sự ngẫm ra một điều: mỗi công ty là một “luật chơi” khác nhau, và mình không thể áp cùng một cách làm cho tất cả.

Ở đây, tôi vẫn làm DA, vẫn phân tích, vẫn muốn đi tìm sự thật. Nhưng lần đầu tiên, tôi thấy rõ ràng khoảng cách giữa những gì tôi cho là “làm tốt” – và những gì người khác thật sự cần.

Tôi làm một phân tích về hiệu quả của một chiến dịch marketing. Tôi kiểm tra selection bias, vẽ DAGs để chắc rằng mình không sai về causal path, chạy các phương pháp kiểm định robustness, viết cả một memo dài đầy lưu ý về assumption. Tôi cảm thấy yên tâm, tự tin – và… nhận lại feedback:

“Chị thấy em làm kỹ, chắc chắn. Nhưng nếu nhanh được hơn thì tốt. Chiến dịch này sắp phải ra quyết định rồi.”

Lúc đó tôi mới nhận ra: họ đâu phải data analyst như mình. Họ không sống trong nỗi sợ “bỏ sót một confounder”, không thức đêm lo về vấn đề selection bias hay violation of ignorability assumption. Họ chỉ cần hiểu: làm tiếp hay không? Có nên thay đổi chiến lược hay không?

Tôi giật mình: mình làm mọi thứ chặt chẽ quá, chậm quá, mà quên rằng không phải ai cũng sống trong thế giới logic và uncertainty như mình. Và thế là, tôi bắt đầu học lại một kỹ năng quan trọng: đọc vị luật chơi của từng nơi, từng người.

⸻

Để một DA trưởng thành, bạn cần nhiều hơn kiến thức phân tích. Bạn cần biết cách sống trong thế giới thật.

Dưới đây là những điều tôi rút ra sau ba công ty, nhiều pha “tự thấy mình sai” và nhiều bài học đến từ sự lặng im của người nghe:

1. Đừng chỉ giỏi kỹ thuật. Hãy giỏi đoán luật chơi.

Mỗi công ty có một nhịp riêng: chậm hay nhanh, chú trọng vào precision hay speed, ra quyết định dựa vào dữ liệu hay cảm giác kinh nghiệm. Mỗi người bạn làm việc cùng cũng có một cách nghĩ khác nhau.

Một chị manager marketing sẽ không nói:

“Em nên dùng inverse probability weighting để kiểm soát selection bias.”

Chị sẽ nói:

“Chị thấy nhóm A tốt hơn nhóm B, nhưng chị chưa chắc có phải do chiến dịch không. Em xem giùm được không?”

Và điều bạn cần làm không chỉ là phân tích – mà là dịch ngôn ngữ. Từ yêu cầu cảm tính đó sang câu hỏi dữ liệu, rồi lại từ kết quả dữ liệu – dịch ngược lại thành lời khuyên dễ hiểu, dễ hành động.

Biết dịch là kỹ năng sống còn. Không ai thuê bạn để thể hiện mình thông minh. Họ thuê bạn để họ thông minh hơn.

⸻

2. Học từ học thuật, nhưng đừng lậm học thuật.

Tôi từng dành hàng tuần để chỉnh lại một phân tích vì phát hiện ra có khả năng xuất hiện collider bias. Tôi lo sợ nếu không điều chỉnh, kết quả sẽ “sai”, và người dùng sẽ hiểu lầm. Nhưng rồi tôi nhận ra:
	•	Với bối cảnh chiến dịch đó, dù có bias thì ảnh hưởng cũng rất nhỏ.
	•	Và nếu tôi chậm thêm vài ngày nữa, họ sẽ không chờ. Họ sẽ quyết theo cảm tính.

Không phải lúc nào cũng cần làm đến tận cùng. Không phải cái gì cũng cần causal. Không phải lúc nào cũng cần học thuyết để giải thích.

Làm DA không phải để vẽ bản đồ địa lý chính xác từng milimet. Là để chỉ đường cho người khác – càng nhanh, càng rõ, càng tốt.

⸻

3. Biết chọn trận mà đánh.

Có lúc, bạn phải phân tích như researcher: sâu, nghiêm túc, kiểm tra assumption.
Có lúc, bạn phải phản ứng nhanh: gọn, rõ, bỏ qua vài thứ nhỏ để giữ tốc độ.

Ví dụ: bạn được yêu cầu phân tích hiệu quả của push notification trong 3 ngày gần đây. Lúc này, bạn không cần chạy một mô hình causal phức tạp. Một kiểm tra so sánh nhóm đơn giản, cộng thêm vài điều kiện sanity check, có thể đủ để đưa ra khuyến nghị.

Thành công nằm ở việc biết khi nào nên dùng súng, khi nào nên dùng dao gọt trái cây.

⸻

4. Luôn hỏi: “Nếu là tôi, tôi có dám hành động theo phân tích này không?”

Câu hỏi này buộc bạn phải nghĩ như người ra quyết định. Khi bạn đặt mình vào vai người dùng insight – bạn sẽ thấy:
	•	Chỗ nào cần nói rõ hơn?
	•	Kết quả này có đủ thuyết phục chưa?
	•	Người khác sẽ hiểu như thế nào?
	•	Có dữ liệu nào giúp họ an tâm hơn không?

Khi bạn nghĩ như vậy, phân tích của bạn không chỉ là “đúng”, mà còn dùng được.

⸻

5. Tự hỏi mỗi tuần: “Mình đang làm analyst, hay mình đang làm researcher?”

Không phải để chọn một vai. Mà để biết mình có đang đi lệch khỏi kỳ vọng hay không.

Nếu bạn là analyst, nhưng báo cáo của bạn nhìn như academic paper – bạn đang xa dần người dùng.
Nếu bạn là researcher, nhưng bài viết của bạn nhìn như một quảng cáo thuyết phục – bạn đang làm sai vai.

Giữ được ranh giới này rõ ràng, bạn sẽ biết cách cân bằng giữa depth và speed, giữa rigor và clarity.

⸻

Bạn muốn mình gộp toàn bộ bài viết thành một post mượt mà, thống nhất và đề xuất hình ảnh, tiêu đề, tagline không?
