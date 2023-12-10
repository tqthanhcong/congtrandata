---
layout: post
title: "Các bài toán trong DA"
subtitle: "Một cái nhìn tổng quát theo kinh nghiệm cá nhân về các bài toán mà DA thường gặp và cách giải quyết được tôi sử dụng"
date: 2023-12-02 23:45:13 -0400
background: '/img/posts/01.jpg'
category: DA
---

DA dùng data để giúp các team liên quan giải quyết vấn đề của riêng họ, vốn tồn tại ở nhiều dạng khác nhau và mang những bối cảnh riêng. Nếu mỗi lần thực hiện phân tích, DA lại ngồi suy nghĩ cách làm, ngồi gõ thủ công lại các đoạn SQL, vẽ lại các chart mình vừa nghĩ ra thì thực sự khá mất công.

Lúc mới làm DA, tôi rất mong muốn tìm được một bí kíp nào đó tổng quát hoá lại các bài toán DA thường giải và nêu ra phương pháp giải quyết phù hợp để bản thân chỉ cần học và áp dụng cho nhanh. Trải qua một thời gian làm việc và học hỏi từ đồng nghiệp, tôi tự tạo cho mình một quy trình "công nghiệp hoá" để áp dụng vào công việc bản thân, tôi gọi nó là "Phương pháp DA"

Phương pháp DA được tạo thành bằng cách vay mượn và tổng hợp các hệ thống trong các ngành data science, problem solving, thống kê, marketing và trải nghiệm của bản thân.

Đầu tiên chúng ta sẽ đi qua các bài toán mà DA thường gặp và cách làm, sau đó sẽ đến phần làm sao xác định được vấn đề mình đang gặp nằm ở nhóm nào để có phương án giải quyết phù hợp.

<img src="https://datasciencedojo.com/wp-content/uploads/16-995x1030.jpeg" style="width:300px;"/>

### Mô tả

3 công việc cần làm: mô tả thống kê, mô tả tương quan và segment, làm theo thứ tự cho tới khi giải quyết được vấn đề

#### Mô tả thống kê

Bài toán này thì cũng giống như đề bài tập làm văn "Hãy mô tả con vật mà em yêu thích". Trong DA thì sẽ là hãy mô tả user behavior, hãy mô tả sản phẩm mới, hãy mô tả phản ứng của người dùng,..., tất nhiên là với các phiên bản diễn đạt khác nhau.

<img src="https://i.ytimg.com/vi/hwqpkljWdUw/maxresdefault.jpg" style="width:300px;"/>

Ví dụ: Marketing manager: Anh đã có kinh nghiệm trong việc tạo chương trình khuyến mãi cho user, anh đang cần phân tích user behavior để áp dụng chương trình tốt nhất. 

DA chưa có kinh nghiệm để lạc vào cái bẫy đi query cho những câu hỏi nhỏ nhỏ như: Xem thử tần suất mua hàng bình quân khoảng bao nhiêu, ra kết quả thấp quá lại suy nghĩ query gì tiếp theo, chắc sẽ xem tuổi của user là bao nhiêu, user thích mua món hàng nào,... rồi trong lúc viết có đoạn nào sai thế là phải quay lại sửa sửa, viết xong câu này lại suy nghĩ tiếp query gì tiếp theo.
Thay vào đó, hãy cứ thực hiện 3 bước:

1. Xác định các yếu tố cần mô tả, các yếu tố này chính là tập hợp những thứ tạo ra thực thể mà stakeholder đang quan tậm. Chẳng hạn với ví dụ trên, stakeholder quan tâm đến user behavior, vậy đây là các yếu tố tạo nên user behavior mà có thể đo lường được: demographic của user, tần suất mua hàng của user, mức chi tiêu của user, tỷ lệ phản ứng của user với chương trình khuyến mãi

2. Thu thập data rồi thực hiện làm descriptive statistic cho các yếu tố ấy bằng tất cả các chỉ số nổi tiếng mà các nhà thống kê đã hướng dẫn chúng ta: mean, min, max, median, p25, p75, p10, p90, mod, skewness, kurtois, outlier, hoặc xem graph distribution

*[Đọc thêm: Các loại distribution](https://www.itl.nist.gov/div898/handbook/eda/section3/eda366.htm)*

3. Sau bước 2 chúng ta có một loạt các chỉ số mô tả cho một loạt các yếu tố khác nhau. Tại đây, bằng tư duy logic, chúng ta quan sát các chỉ số này chọn lọc lại những mô tả nào có khả năng trả lời câu hỏi của stakeholder như thế nào. Chẳng hạn, với câu hỏi ví dụ, nhờ thống kê mô tả, DA trả lời được: "Khách hàng của chúng ta đa dạng ở nhiều lứa tuổi khác nhau, không thích chương trình khuyến mãi lắm vì thông thường chỉ có khoảng 2% khách hàng phản ứng với chương trình. Ngoài ra, hành vi mua hàng phân hoá khá mạnh, mặc dù 50% mua dưới 3 lần/tháng nhưng top 25% mua nhiều nhất lại mua trên 50 lần/tháng. Vì vậy chiến lược marketing lần này cần thiết kế phù hợp với đặc điểm này, ngoài ra chiến dịch cũng cần làm cho đa dạng với từng nhóm khách hàng khác nhau"


#### Mô tả tương quan

Nếu sau khi thống kê mô tả, câu hỏi của stakeholder chưa được giải quyết. Nếu trực giác mách bảo những kết luận ở phần mô tả thống kê còn hơi chung chung và cần kết nối nhiều yếu tố khác nhau, thì đó là lúc chúng ta cần phân tích sự tương quan. Thư viện python hỗ trợ rất tốt việc này. 

Chỉ cần nhìn vào ma trận tương quan giữa các cặp yếu tố, chúng ta có thể đưa ra những kết luận chi tiết hơn, hỗ trợ giải quyết vấn đề của stakeholder, ví dụ: "...25% mua nhiều nhất lại mua trên 50 lần/tháng, là nhóm khách hàng trẻ tuổi, data chỉ ra khách hàng nào mua càng nhiều sản phẩm thì độ tuổi càng trẻ, khách hàng tần suất thấp thường là khách hàng lớn tuổi hơn. Vậy nên nếu anh muốn target vào nhóm khách hàng tần suất thấp thì cần tìm thông điệp nào phù hợp với người lớn tuổi hơn"

#### Segmentation

Cuối cùng, nếu vấn đề quá phức tạp, quá nhiều yếu tố cần phải mô tả, quá nhiều thứ để nhớ mà 2 bước trên không thể nào giúp trả lời ngắn gọn, dễ hiểu, hãy segment! Segment là việc chia các đối tượng vào các nhóm với đặc điểm tập trung hơn. Chẳng hạn như ở phần trên chúng ta có kết luận khách hàng đa dạng ở nhiều lứa tuổi, vậy hãy chia nhỏ họ để các nhóm có độ tuổi tập trung hơn.

Cụ thể làm 3 bước:
1. Chọn ra các yếu tố quan trọng để segemt
2. Chọn kỹ thuật để segment bằng một trong các cách sau (hoặc kết hợp linh hoạt nhiều cách):
- **Theo strategry của stakeholder**: hỏi stakeholder xem chiến lược của họ cần chia các nhóm khách hàng ra thành những nhóm như thế nào. Cách này chia dựa theo nhu cầu từ business, có thể là những cách chia đã được giảng dạy trong giáo trình quản trị nổi tiếng.
- **Theo percentile**: Khách hàng nằm trong nhóm có độ tuổi thấp hơn trung bình & mua hàng nhiều nhất sẽ được chia vào 1 nhóm, nhóm có độ tuổi thấp hơn trung bình & mua hàng ít nhất được vào 1 nhóm,... cứ như vậy. Cách này khá hiệu quả và dễ hiểu nếu chúng ta segment dựa trên 2 yếu tố, các bí kíp về quản trị hay dùng cách này để tạo ra kim tứ đồ.
- **Dùng K-mean**: Đây là một thuật toán để cluster everything, sử dụng khá nhẹ đầu chỉ là sẽ hơi khó để giải thích cho non-tech stakeholder
3. Chạy lại các descritptive statistic cho mỗi segment.

Đến bước này, dựa trên một hệ thống góc nhìn, chúng ta sẽ thực sự hiểu về data của mình. Chúng có thể được chia ra những nhóm nào, mỗi nhóm có đặc điểm gì. Cộng với tư duy logic để áp dụng cho từng trường hợp cụ thể, DA có thể trả lời và giải quyết được nhiều vấn đề của stakeholder

Điều quan trọng là hãy lưu lại tất cả những script để mỗi lấn tính chỉ cần lấy áp số vào là ra kết quả, lặp đi lặp lại mà không cần tốn công. Đối với bài toán này, hãy chỉ dành công sức cho việc suy nghĩ cần mô tả "cái gì".

### Tìm xu hướng

Bài toán này thường phát sinh khi mọi người đang quan tâm đến sự thay đổi, thay đổi trong thị hiếu khách hàng, trong doanh số, trong thị trường,...

Cần lưu ý là ở đây tôi không nhắc tới bài toán phân tích xu hướng rồi dự báo như một bài toán điển hình của data science, mà chỉ là một bài toán đơn giản hơn nhiều:

*[Cái gì] (1)* đang *[tăng/giảm] (2)* và *[mạnh/yếu] (3)* thế nào?
Nhiệm vụ của DA ở đây là lấp đầy các vị trí (1), (2), (3). Ví dụ: "Món trà chanh giã tay đang tăng tỷ lệ đặt hàng mạnh nhất trong tất cả sản phẩm" hay "Chi phí promotion đang giảm mạnh, nghi ngờ là một nguyên nhân làm doanh số tháng này giảm mạnh".
Cách làm như sau:

(2) [tăng/giảm]: Đối với DA, đơn giản là dùng mắt thường để xác định một xu hướng là tăng, giảm hay đi ngang. Nếu không xác định được bằng, có thể kết luận là "khó xác định".

(3) [mạnh/yếu]: Một lần nữa chúng ta có thể dùng mắt thường, hoặc dùng các kỹ thuật như CARG để xác định.

(1) [Cái gì]: Cái gì ở đây rất quan trọng. Như bạn biết, doanh thu cả công ty có thể đang tăng nhưng doanh thu của những sản phẩm cốt lõi đang giảm. Do đó, đối với các bài toán tìm xu hướng, DA sẽ cần hiểu mối quan tâm của stakeholder sau đó dùng kỹ thuật breakdown để phác hoạ được trend của những "cái gì" quan trọng. Chẳng hạn chia theo sản phẩm để tìm ra "Trà chanh giã tay" đang có trend cực kỳ mạnh, vốn không thể nhìn thấy khi phân tích trend của doanh số toàn cửa hàng.

Lặp lại điều quan trọng là chúng ta cần lưu lại các script, các hệ thống hỗ trợ phân tích loại này để có thể dùng đi dùng lại một cách tiện lợi nhất. Cứ bài toán nào cần tìm xu hướng là lôi script ra, thay một vài thông số rồi chạy và xem kết quả.


Chúng ta vừa đi qua 2 phần là mô tả và tìm xu hướng. Tôi nghĩ rằng đây là 2 bài toán cơ bản của DA. Bằng cách lưu script & thiết kế công cụ phù hợp để lặp đi lặp lại các kỹ thuật được liệt kê bên trên, tôi có câu trả lời cho khoảng 70% câu hỏi của stakeholder. Phần còn lại chỉ là vẽ chart để trình bày các câu trả lời ấy. Bài toán lớn nhất và khó nhất mà tôi gặp phải nằm ở phần sau

### Suy luận nhân quả

Có phải nhờ chiến lược mới mà khách hàng tháng vừa rồi mua hàng nhiều hơn không?... là dạng câu hỏi khó trả lời nhất trong DA. Chúng ta đang đến với mảnh đất của suy luận nhân quả

Nhân quả là một dạng tương quan đặc biệt, không phải tương quan nào cũng là nhân quả
Tương quan: người ta thấy rằng 2 hiện tượng thường xuất hiện cùng lúc (Tết đến là hoa mai nở, hoa mai nở là con nít được nhận lì xì)
Nhân quả: do hiện tượng 1 mà mới dẫn tới hiện tượng 2 (Do thời tiết phù hợp cộng với đặc điểm sinh học mà hoa mai mới nở, do là ngày Tết nên người lớn lì xì con nít)

Gọi suy luận nhân quả là khó bởi vì với những gì thể hiện trong data, bằng các kỹ thuật thông thường, chúng ta chỉ biết được thường khi đến Tết thì có hoa mai thôi chứ rất khó để xác nhận cái gì làm cho hoa mai nở. Có phải do Tết không? nếu dời ngày Tết thay vì là 1/1 âm lịch qua ngày 1/6 âm lịch thì hoa mai lúc đó có nở không? Rốt cuộc tại sao hoa mại lại nở?

À thì đương nhiên là ai cũng biết câu trả lời nhưng đó là do chúng ta có kiến thức về tự nhiên và sinh học. Chứ lấy data phân tích lên bờ xuống ruộng cũng không dám chắc được câu trả lời, vì, một lần nữa, khả năng cao là data cũng chỉ có thể chỉ ra được là 2 chúng nó hay xuất hiện cùng với nhau mà thôi.

Để suy luận nhân quả thành công, tức trả lời câu hỏi có phải "do **cái này như vậy** nên **cái kia mới như thế** hay không", chúng ta làm 1 trong 2 cách:
1. Cách 1 (tiêu chuẩn vàng): kiểm soát ngẫu nhiên (AB testing): chia tập nghiên cứu thành 2 phần, 1 phần thử nghiệm, 1 phần giữ nguyên sau đó so sánh kết quả cuối cùng của 2 nhóm để xác định tác động thực sự của chiến lược quảng cáo.
2. Cách 2 chỉ nên làm nếu không thực hiện được cách 1: Đó là sử dụng historical data để suy luận nhân quả. Với historical data, chúng ta lại có nhiều cách khác nhau để xử lý, như:
- natural experimental
- quasi-experimental
- regression
- ML model

Nếu việc suy luận quá khó, chúng ta có thể chuyển qua chiến lược khác: Phân tích tương quan giữa các yếu tố và kết luận chúng có tương quan, việc có quan hệ nhân quả hay không cần các thử nghiệm để kiểm chứng.

### Phân tích tương quan khi không thể suy luận nhân quả

Đây là bài toán chúng ta thực hiện khi không có khả năng suy luận nhân quả. Cách đơn giản và công nghiệp nhất để làm đó là thực hiện linear regression với Y là "cái kia" còn X là tập hơn các biến giúp dự đoán được Y, bao gồm biến "cái này".
Dựa vào mô hình hồi quy chúng ta có thể có cái nhìn sâu sắc hơn về tương quan giữa "cái này" với "cái kia" trong bối cảnh có xét tới các yếu tố liên quan.

Nếu chúng không có tương quan, chúng cũng không có quan hệ nhân quả.
Nếu chúng có tương quan, chúng có thể có quan hệ nhân quả hoặc không. Thời gian & những thử nghiệm sẽ trả lời tất cả.


Trên đây là các bài toán mà tôi nghĩ là bao quát các vấn đề mà DA giải quyết. Tác dụng của việc tổng quát hoá này là DA có thể nhận ra có những quy trình chung thực sự có ích và có tác động lớn khi phân tích dữ liệu, từ đó, chẳng hạn như tôi, đã phải suy nghĩ cách viết script, lưu lại các câu code, tạo các hệ thống tự động sao cho có thể chạy các tính toán trên một cách ít tốn công nhất và có khả năng lặp đi lặp lại liên tục, để dành thời gian cho việc suy nghĩ các giải pháp sáng tạo, học hỏi & chia sẻ.

