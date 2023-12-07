---
layout: post
title: "Tóm gọn các bài toán DA phải giải quyết"
subtitle: "Liệt kê ngắn gọn và tổng quát các bài toán mà DA phải làm và những phương pháp phù hợp để giải quyết."
date: 2023-12-02 23:45:13 -0400
background: '/img/posts/01.jpg'
category: DA
---

DA dùng data để giúp các team liên quan giải quyết vấn đề của riêng họ. Chúng có rất nhiều dạng khác nhau và mỗi case đều có những bối cảnh riêng. Nếu mỗi lần thực hiện phân tích, DA lại ngồi suy nghĩ cách làm, ngồi gõ thủ công lại các đoạn SQL, vẽ lại các chart mình vừa nghĩ ra thì thực sự khá mất công.

Vậy nên nếu cố gắng tổng quát hoá lại các bài toán DA thường giải và tìm ra phương pháp phù hợp để giải và thiết kế 1 hệ thống "bán auto" thì công việc chắc sẽ trơn tru hơn.

![Demo Image](https://datasciencedojo.com/wp-content/uploads/16-995x1030.jpeg)

## Mô tả chủ thể

Bài toán này thì cũng giống như đề bài tập làm văn mô tả ("Hãy mô tả con vật mà em yêu thích").

![Demo Image](https://i.ytimg.com/vi/hwqpkljWdUw/maxresdefault.jpg)

Bài toán này thường diễn ra ở 2 trường hợp:
- Hoặc stakeholder đang gặp vấn đề mới, sản phẩm mới và chưa biết gì nhiều, cần thông tin gì đó làm cơ sở để phát triển thêm kế hoạch và chiến lược
- Hoặc stakeholder đã có những cách giải quyết vấn đề, chỉ cần những thông tin mô tả để lấp đầy vào chỗ trống trong plan

Ví dụ: Marketing manager: Anh đã có kinh nghiệm trong việc tạo chương trình khuyến mãi cho user, anh đang cần biết user behavior của mình để áp dụng các kiến thức của mình để chạy chương trình tốt nhất. 

Đây chắc là bài toán dễ làm nhất, đối với dạng này, chúng ta cứ apply 2 bước:
1. Thực hiện làm descriptive statistic cho các entity: mean, min, max, median, p25, p75, mod, distribution. Chẳng hạn trong ví dụ này là mô tả về tuổi, city, tần suất mua hàng của user
2. Nhìn toàn bộ bảng thống kê và tóm tắt lại các điểm chính, điểm bất thường,... thường sẽ là: 
- Data point có xu hướng tập trung về 1 khu vực 
- Outlier


### Tìm xu hướng đang nổi tự nhiên

"Trend năm nay là trà chanh giã tay, không bắt kịp được là mất cơ hội"
"Tuy nhóm khách hàng trẻ tuổi của chúng ta còn ít nhưng thị phần đang tăng rất nhanh, cần phải chú ý để có những sản phẩm phù hợp"

Đó là những

Một trong những công việc quan trọng khác của DA là phân tích xu hướng. Điều này có nghĩa là xác định xu hướng tăng trưởng, sự suy giảm, hoặc các mẫu hành vi theo thời gian. Phân tích này giúp cho các doanh nghiệp có thể dự đoán và điều chỉnh chiến lược kinh doanh của mình một cách hiệu quả.

### Đo Lường Hiệu Suất

Đo lường hiệu suất là việc đánh giá và so sánh hiệu suất của các chiến dịch, sản phẩm, hoặc dịch vụ. Nó không chỉ giúp xác định các yếu tố thành công, mà còn giúp nhận ra những điểm yếu cần cải thiện. Điều này đóng vai trò quan trọng trong việc tối ưu hóa nguồn lực và nâng cao hiệu quả hoạt động.

### Phân tích Nguyên Nhân

Khi một vấn đề xảy ra, việc tìm ra nguyên nhân gốc rễ là cực kỳ quan trọng. Phân tích nguyên nhân giúp DA xác định được điều gì đã dẫn đến một sự kiện hoặc một kết quả cụ thể. Việc này đòi hỏi sự hiểu biết sâu sắc về dữ liệu và khả năng phân tích tinh tế.

### Tối Ưu Hoá Quy Trình

Cuối cùng, DA cũng có trách nhiệm trong việc tối ưu hoá các quy trình làm việc. Điều này có nghĩa là tìm ra cách làm việc hiệu quả hơn, tiết kiệm thời gian và nguồn lực, đồng thời nâng cao chất lượng sản phẩm hoặc dịch vụ.

Tóm lại, vai trò của DA không chỉ là làm việc với số liệu, mà còn là sử dụng thông tin đó để giúp các doanh nghiệp đưa ra quyết định chính xác và phát triển bền vững. Bằng cách tiếp cận các vấn đề một cách hệ thống và có phương pháp, DA có thể tạo ra giá trị lớn cho cả tổ chức và khách hàng của họ.


Space, the final frontier. These are the voyages of the Starship Enterprise. Its five-year mission: to explore strange new worlds, to seek out new life and new civilizations, to boldly go where no man has gone before.

As I stand out here in the wonders of the unknown at Hadley, I sort of realize there’s a fundamental truth to our nature, Man must explore, and this is exploration at its greatest.

Placeholder text by [Space Ipsum](http://spaceipsum.com/). Photographs by [Unsplash](https://unsplash.com/).
