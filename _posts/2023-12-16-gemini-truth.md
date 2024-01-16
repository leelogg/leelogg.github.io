---
layout: post
title: Lời nói dối của Gemini - Bước tiến mới của AI từ Google
date: 2023-12-16
categories: [Vietnamese, News, Technology]
tags: [artificial intelligence, gemini, google]
image: https://i.postimg.cc/76CrV4Kx/0-gemini-truth.jpg
---

> _“Với niềm tự hào và sự phấn khích tột cùng, tôi xin thông báo về sự ra mắt của **kỷ nguyên Gemini (The Gemini era)** - bước tiến đầu tiên hướng tới một mô hình trí tuệ nhân tạo (AI) vạn năng.”_
>
> **\- Demis Hassabis, CEO của Google DeepMind**

Được CEO Sundar Pichai của Google giới thiệu lần đầu tại [Google IO 2023](https://io.google/2023/), **Gemini** chính là mô hình ngôn ngữ (l*arge language model - LLM*) lớn nhất của Google nay đã được phát hành cho công chúng.

Qua lời miêu tả của Pichai và Hassabis, nó là một bước tiến vượt bậc trong một mô hình AI mà có sức ảnh hưởng đến mọi sản phẩm của Google: _“Một trong những điều kì diệu nhất tại thời điểm này là chúng tôi có thể cải thiện một công nghệ nền tảng và ngay lập tức, nó sẽ lan truyền khắp mọi sản phẩm của chúng tôi”_.

Đến thời điểm hiện tại, Google đã luôn bị Microsoft và OpenAI bỏ xa trong cuộc đua trí tuệ nhân tạo, đặc biệt với sự phát hành của GPT-4. Tuy nhiên, bàn cân có lẽ đang nghiêng dần về phía Google khi **Gemini** được thông báo là là mô hình đầu tiên vượt qua con người ở cấp độ chuyên gia trong khả năng hiểu ngôn ngữ đa nhiệm lớn (MMLU) và **_có thể đánh bại GPT-4 trên hầu hết mọi điểm chuẩn_**. Điều này đã đem đến lượng lớn sự hứng thú và ủng hộ đến cho Google, nhưng rất ít người đã nhìn nhận đề tài này trong một bối cảnh lớn hơn và thắc mắc: **_Liệu sự thật có đơn giản như thế?_**

**Qua bài viết này, hãy cùng mình tìm hiểu thật kỹ về Gemini, nắm rõ mọi khía cạnh của nó và đúc kết xem sự ra mắt của Gemini có ý nghĩa như thế nào cho cuộc đua trí tuệ nhân tạo.**

> _**Note**: Bài blog này được lấy cảm hứng từ video [The Gemini Lie](https://youtu.be/90CYYfl9ntM?si=_4HzNHfw1o88hQ7f) (lời nói dối Gemini) của kênh [Fireship](https://www.youtube.com/@Fireship), mình khuyến khích bạn đọc xem video và những nội dung của kênh này. Là một học sinh chuyên tin, mình đã luôn nhận được những nội dung không chỉ hữu ích mà còn cực kì thú vị, giải trí từ Fireship. Mọi tài liệu mình sử dụng trong bài blog này sẽ có ở **Tài liệu tham khảo** (cuối bài)._

## Những gì chúng ta biết

![Gemini - Mô hình mới nhất và mạnh mẽ nhất của Google](https://i.postimg.cc/tgqx7S2d/34-gemini-introduction.jpg)

_Tất nhiên, để có thể bàn về mọi khía cạnh của Gemini, ta phải xem những gì đã được tuyên bố về khả năng của nó._

Sau một thời gian tìm hiểu những tài liệu chính thức của Google về Gemini, mình đã học được nhiều thông tin nhất trong 4 tài liệu sau:

1.  [Google DeepMind \| Gemini](https://deepmind.google/technologies/gemini/#introduction): Trang web giới thiệu Gemini.
2.  [Google Blog \| Introducing Gemini: our largest and most capable AI model](https://blog.google/technology/ai/google-gemini-ai/): Bài blog của Google giới thiệu Gemini.
3.  [Google for Developers \| How it’s Made: Interacting with Gemini through multimodal prompting](https://developers.googleblog.com/2023/12/how-its-made-gemini-multimodal-prompting.html): Bài blog dùng thử các tính năng của Gemini.
4.  [Gemini: A Family of Highly Capable Multimodal Models](https://storage.googleapis.com/deepmind-media/gemini/gemini_1_report.pdf): Báo cáo kỹ thuật của Google DeepMind về Gemini.

Tuy nhiên, mọi người luôn có thể tìm hiểu kỹ hơn về Gemini qua [tuyển tập bài blog về Gemini của Google](https://blog.google/technology/ai/gemini-collection/). Mình sẽ bàn luận khá chi tiết và dài dòng về Gemini ở phần này, nếu bạn muốn tiết kiệm thời gian thì các bạn có thể xem qua [bài viết rất hay và đầy đủ của VnEconomy](https://vneconomy.vn/techconnect//google-trinh-lang-geminimo-hinh-ai-thong-minh-lon-nhat-co-nang-luc-manh-hon-canh-tranh-voi-gpt-4.htm) để nắm được những ý quan trọng. Giờ hãy cùng xem những thông tin về **Gemini** với mình nhé!

Phiên bản đầu tiên của **Gemini - Gemini 1.0** - là một nhóm gồm 3 mô hình với kích cỡ khác nhau: **Gemini Nano**, **Gemini Pro** và **Gemini Ultra**. **Nano** được thiết kế để chạy ngoại tuyến trên các thiết bị Android, **Pro** được sử dụng cho các tác vụ nâng cao hiệu suất và triển khai với quy mô lớn, và cuối cùng là **Ultra**, LLM mạnh mẽ nhất Google tạo ra, được sử dụng cho các tác vụ có tính phức tạp cao.

![3 kích thước Nano, Pro và Ultra của Gemini](https://i.postimg.cc/tgvHWJtS/1-gemini-sizes.jpg)

Google hiện đang phát hành **Gemini** qua một số cách: **Gemini Pro** đã được tích hợp vào Bard và người dùng Pixel 8 Pro sẽ nhận được các tính năng mới nhờ vào **Gemini Nano**, riêng **Gemini Ultra** sẽ được phát hành vào năm 2024. Kể từ ngày 13/12/2023, các nhà phát triển và khách hàng doanh nghiệp sẽ có thể truy cập **Gemini Pro** qua _Google Generative AI Studio_ hoặc _Vertex AI trong Google Cloud_. Tại thời điểm bài viết, **Gemini** chỉ có bằng tiếng Anh nhưng các ngôn ngữ khác chắc chắn sẽ sớm được ra mắt.

Pichai cho biết, mô hình này sẽ được tích hợp vào công cụ tìm kiếm, các sản phẩm quảng cáo, trình duyệt Chrome và hơn thế nữa. Đây là một bước tiến vừa kịp lúc để **đưa Google trở lại vào cuộc đua trí tuệ nhân tạo**.

Quay trở lại về hơn 1 năm trước, OpenAI đã cho ra mắt chatbot _ChatGPT_, và cả công ty lẫn sản phẩm đều ngay lập tức trở thành 2 cái tên nổi trội nhất trong mảng trí tuệ nhân tạo. Trong khi đó, Google - công ty đứng đằng sau sự khởi đầu của cuộc bùng nổ AI, công ty tự gọi mình là “tổ chức trí tuệ nhân tạo đầu tiên” trong gần một thập kỉ - lại thể hiện rõ sự sững sờ của họ trước sự lợi hại của ChatGPT và tốc độ chóng mặt của OpenAI. Nhưng, giờ đây, với _Gemini_, Google đã sẵn sàng đáp trả và đưa mình thành một **đối thủ đáng gờm trở về cuộc đua AI**.

Thôi, lan man nhiêu đó là quá đủ rồi nhỉ? Hãy cùng đi đến câu hỏi mà ai cũng hứng thú nhất: **_GPT-4 của OpenAI và Gemini của Google, ai là người thắng cuộc_**?

### Google tuyên bố rằng Gemini đánh bại GPT-4 ở 30 trong số 32 điểm chuẩn

---

> _“Chúng tôi đã đánh giá hiệu suất của các mô hình Gemini dựa trên một bộ tiêu chuẩn toàn diện, bao gồm một loạt nhiệm vụ về ngôn ngữ, lập trình, lý luận và các tác vụ đa phương thức,”_ bản báo cáo kỹ thuật của Google cho hay, _“Mô hình tiên tiến nhất của chúng tôi, **Gemini Ultra**, đạt được kết quả tiên tiến nhất (state-of-the-art) ở 30 trong số 32 điểm chuẩn, bao gồm 10 trong 12 điểm chuẩn phổ biến về lý luận và văn bản, 9 trong 9 điểm chuẩn khả năng hiểu hình ảnh, 6 trong 6 điểm chuẩn khả năng hiểu video và 5 trong 5 điểm chuẩn về nhận diện giọng nói và dịch thuật.”_

Không chỉ dừng ở đó, bản báo cáo còn cho biết **Gemini Ultra** chính là **mô hình đầu tiên đạt được hiệu suất con người ở cấp chuyên gia trong MMLU** - một điểm chuẩn nổi bật trong việc đánh giá kiến thức và khả năng lý luận qua một bộ bài kiểm tra - với điểm số **hơn 90%** (Nội dung này sẽ được bàn luận kĩ hơn ở cuối bài). Bạn đọc có thể xem bảng đánh giá của một vài điểm chuẩn tiêu biểu được Google đưa ra dưới đây:

![Điểm chuẩn về văn bản của Gemini](https://i.postimg.cc/T149c8HX/2-gemini-benchmark-text.jpg)
![Điểm chuẩn về đa phương thức của Gemini](https://i.postimg.cc/wxf0zJxb/3-gemini-benchmark-multimodal.jpg)

Trong những điểm chuẩn trên, điểm mạnh nổi bật nhất của **Gemini** đến từ khả năng hiểu và tương tác với video và âm thanh của nó. Mô hình đa phương thức đã là một phần trong kế hoạch **Gemini** ngay từ thời điểm ban đầu.

Google không huấn luyện những mô hình riêng biệt cho hình ảnh và giọng nói như cách mà OpenAI tạo _DALL-E_ và _Whisper_, mà nó xây dưng một mô hình đa giác quan từ đầu. DeepMind rất quan tâm tới việc nghĩ ra cách kết hợp tất cả các phương thức trên với nhau: thu thập được nhiều dữ liệu nhất có thể từ các đầu vào và giác quan, rồi đưa ra những phản hồi cũng có độ đa dạng tương tự như thế.

> _“Mô hình Gemini vốn là đa phương thức. Những mô hình này thể hiện năng lực mới lạ trong việc kết hợp các tính năng của nó qua nhiều phương thức khác nhau (ví dụ như trích xuất thông tin và bố cục không gian từ bảng, biểu đồ hoặc hình) với khả năng suy luận mạnh mẽ của một mô hình ngôn ngữ (như màn thể hiện state-of-the-art của nó trong toán và lập trình). Những mô hình này còn thể hiện tốt trong việc phân biệt chi tiết trong các input (đầu vào), tổng hợp thông tin bối cảnh trong không gian và thời gian, rồi áp dụng những khả năng này trong chuỗi frames (khung hình) video và / hoặc input âm thanh.”_

Hiện tại, những mô hình cơ bản nhất của **Gemini** có input và output (đầu vào và đầu ra) là văn bản, nhưng những mô hình mạnh mẽ hơn như **Gemini Ultra** có thể làm việc với hình ảnh, video và âm thanh. _“Nó thậm chí sẽ còn khái quát hơn trong tương lai”_, Hassabis cho biết, _“Vẫn còn nhiều thứ ta có thể khai thác như hành động hay xúc giác, những thứ giống kiểu robot hơn”. Ông cho rằng, theo thời gian, Gemini sẽ có thêm “giác quan”_, có nhận thức hơn, chính xác hơn và có căn cứ hơn trong quá trình đó. _“Những mô hình này chỉ đang dần hiểu rõ hơn thế giới quanh nó.”_

Tất nhiên, nó vẫn sẽ có những sự ngộ nhận, có những định kiến và nhiều vấn đề khác, nhưng khi biết càng nhiều, nó sẽ càng hoạt động tốt hơn.

### Suy luận phức tạp

---

Khả năng suy luận đa phương thức có thể giúp thông hiểu được các thông tin từ văn bản và hình ảnh phức tạp. Điều này cho nó khả năng khám phá được những kiến thức khó phân biệt trong một nguồn dữ liệu khổng lồ.

Nó còn có khả năng vượt trội trong việc trích xuất thông tin từ hàng ngàn tài liệu qua việc đọc, chắt lọc và hiểu những thông tin ấy, giúp đem lại những đột phá mới trong nhiều lĩnh vực từ khoa học đến tài chính.

<iframe width="560" height="315" src="https://www.youtube.com/embed/sPiOP_CB54A?si=kfXEVBAdJOtGB3DH" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Hiểu được văn bản, hình ảnh, âm thanh và hơn cả thế

---

**Gemini 1.0** được huấn luyện để nhận diện và hiểu văn bản, hình ảnh, âm thanh và nhiều phương thức khác cùng lúc. Nhờ vào đó, nó có thể hiểu được những thông tin có nhiều sắc thái hơn và có thể trả lời những câu hỏi liên quan đến các chủ đề phức tạp. Điều này đem lại cho **Gemini** khả năng giải thích và lý luận tuyệt vời trong những chủ đề như toán và vật lý.

<iframe width="560" height="315" src="https://www.youtube.com/embed/K4pX1VAxaAI?si=nfMhiK6GQN841AUK" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Khả năng lập trình nâng cao

---

Phiên bản đầu tiên của **Gemini** có thể hiểu, giải thích, và viết ra code chất lượng cao trong các ngôn ngữ phổ biến nhất như _Python_, _Java_, _C++_ và Go. Khả năng làm việc trên nhiều ngôn ngữ và suy luận về thông tin phức tạp giúp nó trở thành **một trong những mô hình hàng đầu cho việc lập trình trên thế giới**.

**Gemini Ultra** thể hiện vượt trội trong nhiều điểm chuẩn về lập trình, trong đó có _HumanEval_, một điểm chuẩn quan trọng trong việc đánh giá khả năng của nó trong nhiều tác vụ lập trình, và _Natural2Code_, tập dữ liệu nội bộ của Google, sử dụng nguồn do các tác giả tạo ra thay vì thông tin dựa trên nền tảng web.

**Gemini** còn có thể được dùng làm engine cho những hệ thống mã tiên tiến hơn. 2 năm nước, Google đã ra mắt **AlphaCode**, hệ thống AI lập trình đầu tiên có thể đạt được kết quả cạnh tranh cao trong các cuộc thi lập trình. Bằng cách sử dụng một phiên bản chuyên biệt của **Gemini**, Google đã tạo ra được **AlphaCode** 2, hệ thống vượt trội trong việc giải các bài lập trình thi đấu vượt hơn cả phạm vi toán phức tạp và khoa học máy tính lý thuyết _(theoretical computer science)_.

<iframe width="560" height="315" src="https://www.youtube.com/embed/LvGmVmHv69s?si=cEF_3nuFCVny94lh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Khi được đánh giá trên cùng nền tảng với _AlphaCode_, **AlphaCode 2** thể hiện sự phát triển vượt bậc, giải được gấp đôi lượng bài tập. Google ước tính rằng **AlphaCode 2** thể hiện tốt hơn **85% các lập trình viên thi đấu**, hơn hẳn con số (khoảng) 50% của _AlphaCode_. Màn thể hiện này sẽ có thể còn được đẩy mạnh hơn khi lập trình viên chỉ ra một vài tính chất cho mã code để **AlphaCode 2** có thể noi theo.

Bạn đọc có thể tìm hiểu kĩ hơn về AlphaCode 2 trong [bản báo cáo kỹ thuật của AlphaCode2](https://storage.googleapis.com/deepmind-media/AlphaCode2/AlphaCode2_Tech_Report.pdf).

### Đáng tin cậy hơn, quy mô hơn, và hiệu quả hơn?

---

> _“Chúng tôi đã huấn luyện **Gemini 1.0** quy mô lớn trên cơ sở hạ tầng đã được tối ưu hóa bằng AI dùng **Tensor Processing Units (TPUs) v4 và v5e** của Google. Chúng tôi đã thiết kế nó thành mô hình đáng tin cậy và dễ khai thác quy mô nhất để huấn luyện, và mô hình hiệu quả nhất để sử dụng.”_

Với _TPUs_, **Gemini** chạy nhanh hơn hẳn các mô hình nhỏ hơn trước đây. Các _AI accelerators_ (bộ tăng tốc) này đã là trọng tâm của những sản phẩm đã hỗ trợ cho hàng tỉ người dùng như _Search, YouTube, Gmail, Google Maps, Google Play_ và _Android_. Đồng thời, chúng cũng đã giúp nhiều công ty khắp thế giới huấn luyện các mô hình AI quy mô lớn một cách tiết kiệm và hiệu quả.

Bên cạnh những model mới, Google cũng đã thông báo sự ra đời của một phiên bản mới của hệ thống TPU - **Cloud TPU v5p** - được thiết kế để đào tạo các mô hình AI tiên tiến. TPU thế hệ mới này sẽ đẩy nhanh sự phát triển của **Gemini** và giúp các nhà phát triển và khách hàng doanh nghiệp huấn luyện các mô hình _Generative AI_ (mô hình AI tạo sinh) nhanh hơn, tạo cơ hội cho các sản phẩm và khả năng mới được đến với khách hàng sớm hơn.

Bạn đọc có thể nghiên cứu kĩ hơn về TPU v5p qua [bài blog của Google Cloud](https://cloud.google.com/blog/products/ai-machine-learning/introducing-cloud-tpu-v5p-and-ai-hypercomputer).

![Data center của Google](https://i.postimg.cc/J4sKznG7/4-google-data-center.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_Một hàng siêu máy tính Cloud TPU v5p AI accelerator trong một data center (trung tâm dữ liệu) của Google._

### Demo của Gemini Ultra

---

Nãy giờ bàn luận cũng khá nhiều chữ rồi, để đỡ mỏi mắt hơn, hãy cùng mình đến với thứ khiến cho nhiều người quan tâm đến Gemini nhất: **Video demo cực kì viral gần đây từ Google cho thấy khả năng điên rồ của Gemini**.

Mình sẽ bàn luận kĩ hơn về demo của Google ở phần sau. Trước khi bàn luận, nếu chưa xem thì bạn đọc nên xem thử video ngắn dưới đây đã làm chao đảo thế giới đam mê công nghệ.

<iframe width="560" height="315" src="https://www.youtube.com/embed/UIZAiXYceBI?si=F2ugdwkG9mKQAS3S" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

Khi mình xem video này lần đầu, nó đã khiến mình không khỏi há hốc mồm, **_đây quả thật là một sản phẩm điên rồ_**! **Gemini** ở đây thật sự không khác gì _Jarvis trong Iron Man_ cả! Mình xin tóm tắt ngắn ngọn những demo trong video:

> **Note**: Trong video, Gemini tương tác liên tục với người dùng thử từ Google qua video và giọng nói của họ. Nói nôm na, trong video demo, người dùng cứ như đang gọi video cho Gemini vậy. 🤔

1. Người dùng liên tục vẽ thêm những nét vẽ và **Gemini** liên tục miêu tả hình ảnh trên tờ giấy. Sau một thời gian không lâu, **Gemini** nhanh chóng đoán được thứ người dùng đang vẽ là một con vịt.  
   ![Gemini đoán hình con vịt](https://i.postimg.cc/25Q0NK34/5-gemini-demo-1.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini đoán được con vịt là thứ được vẽ qua tương tác video với người dùng._

2. Người dùng đem ra một _con vịt cao su_ màu xanh dương. Thoạt đầu, **Gemini** không biết vật liệu của nó là gì, nhưng sau khi người dùng bảo rằng con vịt kêu tiếng chít chít (tiếng Anh dùng từ _squeak_ nhưng mình chẳng biết dịch như thế nào cả) khi bị bóp, **Gemini** liền nhận ra nó là một con vịt cao su.  
    ![Gemini nhận ra vịt cao su](https://i.imgur.com/NfjK1LJ.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini nhận ra con vịt cao su sau khi biết rằng nó kêu tiếng chít chít khi bị bóp._

3. Người dùng hỏi **Gemini** cách gọi con vịt bằng vài ngôn ngữ khác. Sau khi **Gemini** cho một danh sách liệt kê vài cách ghi duck (con vịt) trong vài ngôn ngữ khác thì người dùng hỏi **Gemini** cách đọc con vịt bằng tiếng Trung Quốc. **Gemini** sau đó trả lời cách đọc bằng âm thanh và hướng dẫn người dùng cách đọc.
   ![Gemini hướng dẫn người dùng đọc tiếng Trung Quốc](https://i.postimg.cc/g26MNJWt/7-gemini-demo-3.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini nói “con vịt” bằng tiếng Trung Quốc, và hướng dẫn người dùng cách đọc._

4. Người dùng đem ra một chiếc bản đồ và yêu cầu **Gemini** nghĩ ra một trò chơi. **Gemini** đề xuất chơi trò Đoán quốc gia. Sau đó, **Gemini** liên tục đưa ra gợi ý bằng emoji và cho biết đáp án đúng sai khi người dùng chỉ vào một quốc gia trên bản đồ.
   ![Người dùng chơi trò Đoán quốc gia với Gemini](https://i.postimg.cc/RhFdfCdR/8-gemini-demo-4.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Người dùng chơi trò Đoán quốc gia với Gemini._

5. Người dùng đem 3 ly nhựa ra và giấu 1 quả bóng giấy dưới ly, **Gemini** nhận ra người dùng đang muốn **Gemini** tìm ra ly nào chứa quả bóng. **Gemini** đoán chính xác ly nào chứa quả bóng sau khi người dùng xáo trộn lên.
   ![Gemini tìm quả bóng dưới chiếc cúp khi người dùng xáo trộn.](https://i.postimg.cc/cHTTrtRC/9-gemini-demo-5.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini tìm quả bóng dưới chiếc cúp khi người dùng xáo trộn._

6. Người dùng thực hiện hành động ra kéo búa bao vài lần, và **Gemini** thành công nhận ra người dùng đang chơi _oẳn tù tì_.
   ![Gemini nhận ra người dùng đang chơi oẳn tù tì.](https://i.postimg.cc/kXLs6mbQ/10-gemini-demo-6.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini nhận ra người dùng đang chơi oẳn tù tì._

7. Người dùng đưa tay ra thể hiện hình con bươm bướm và con chó và hỏi họ đang hiện con vật gì. **Gemini** nhận diện chính xác 2 con vật.
   ![Gemini chính xác đoán được con bươm bướm và con chó.](https://i.postimg.cc/Sx8rcv6w/11-gemini-demo-7.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini chính xác đoán được con bươm bướm và con chó_

8. Người dùng đặt đồng xu dưới tay phải, nhưng khi lật tay lên lại xuất hiện đồng xu bên tay trái. **Gemini** giải thích rằng người dùng đã nhanh tay dùng thủ thuật để làm có vẻ như đồng xu biến mất.
   ![Gemini giải thích cho hiện tượng ki lạ về đồng xu.](https://i.postimg.cc/FKVVBknp/12-gemini-demo-8.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
   _Gemini giải thích cho hiện tượng ki lạ về đồng xu._

9. Người dùng đưa ra 2 đồ vật, không nói gì và **Gemini** tự động nói nên điểm giống nhau của chúng:

- Đồng xu và chiếc bánh quy: “Cả 2 đều là vật tròn.”
- Quả cam và bánh quy: “Cả 2 đều là đồ ăn. Quả cam tốt cho sức khỏe hơn so với bánh quy.”
- Quả cam và fidget spinner: “Quả cam có thể đem đến cảm giác nhẹ nhàng và vòng quay của fidget spinner cũng thế.”
- Cục rubik và fidget spinner: “Cả 2 đều là đồ chơi được trẻ em và người lớn thích thú.”
  ![Gemini mô tả điểm giống nhau giữa quả cam và fidget spinner.](https://i.postimg.cc/6QXhcfzT/13-gemini-demo-9.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
  _Gemini mô tả điểm giống nhau giữa quả cam và fidget spinner._

10. Người dùng cho 2 cuộn len với màu sắc khác nhau và yêu cầu hãy cho họ vài gợi ý một vài sản phẩm, sau đó làm điều tương tự nhưng yêu cầu hãy cho gợi ý liên quan đến động vật. **Gemini** đưa ra 3 gợi ý cho mỗi cặp len bằng văn bản và hình ảnh mô phỏng.
    ![Gemini đưa ra gợi ý tạo ra con thỏ với mũi màu hồng khi người dùng đem ra cuộn len màu xanh dương và hồng.](https://i.postimg.cc/xCsy0DQb/14-gemini-demo-10.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini đưa ra gợi ý tạo ra con thỏ với mũi màu hồng khi người dùng đem ra cuộn len màu xanh dương và hồng._

11. Người dùng đưa ra một tranh vẽ đơn giản có 2 con đường, một con đường dẫn đến hình con vịt, và một con đường dẫn đến hình con gấu và hỏi con vịt cao su nên đi đường nào. **Gemini** trả lời: _“Đường bên trái dẫn đến con vịt - một người bạn. Đường bên phải dẫn đến con gấu - một kẻ thù nguy hại. Gặp bạn bè tốt hơn gặp kẻ thù, nên con vịt cao su nên đi đường bên trái.”_  
    ![Gemini chỉ ra đúng đường đi cho con vịt.](https://i.postimg.cc/VvpqCqdf/15-gemini-demo-11.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini chỉ ra đúng đường đi cho con vịt._

12. Người dùng đem ra một bức hình nối điểm và **Gemini** chính xác nhận ra đó là hình con cua.
    ![Gemini dự đoán chính xác hình con cua.](https://i.postimg.cc/rmyNXyBk/16-gemini-demo-12.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini dự đoán chính xác hình con cua._

13. Người dùng đưa 3 bức hình theo thứ tự Mặt Trời - Sao Thổ - Trái Đất và hỏi _“Đây có phải là thứ tự đúng không?”_. **Gemini** chính xác trả lời _“Không, đây không phải là thứ tự chính xác, thứ tự đúng là Mặt Trời - Trái Đất - Sao Thổ”_.
    ![Gemini nhận diện chính xác thứ tự của 3 hành tinh.](https://i.postimg.cc/pV6Y4Hkw/17-gemini-demo-13.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini nhận diện chính xác thứ tự của 3 hành tinh._

14. Người dùng đưa 2 bức ảnh, mỗi ảnh có 2 chiếc xe khác nhau và hỏi _“Xe nào sẽ đi nhanh hơn”_. **Gemini** trả lời chính xác _“Xe bên phải nhanh hơn vì nó mang tính khí động học (mình chẳng nhớ aerodynamic tiếng Việt là gì hihi) hơn.”_
    ![Gemini chính xác chỉ ra xe bên phải nhanh hơn.](https://i.postimg.cc/prpQrGVc/18-gemini-demo-14.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini chính xác chỉ ra xe bên phải nhanh hơn._

15. Người dùng đưa ra 2 đường ray tàu lượn khác nhau và hỏi _“Cái nào vui hơn”_. **Gemini** trả lời _“Cái bên phải, vì nó có một vòng xoay.”_
    ![Gemini trả lời chính xác câu hỏi tàu lượn](https://i.postimg.cc/4xz6YhZG/19-gemini-demo-15.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Mình không đồng ý, 2 cái tệ như nhau._

16. Người dùng giữ lại bức hình tàu lượn bên phải và hỏi _“Hãy đoán xem người bên trong bức hình này đang nói gì”_. **Gemini** trả lời _“Có thể là Woohoo.”_
    ![Gemini tiếp tục trả lời đúng câu hỏi tàu lượn](https://i.postimg.cc/N0DR4q5P/20-gemini-demo-16.jpg)
    _Một lần nữa, mình không đồng ý. Đáp án đúng là “CÚ TUI”._

17. Người dùng đưa ra một tờ giấy trắng, và lần lượt vẽ thêm các hình: Guitar, amp, trống, và cây cọ. **Gemini** liên tục tương tác theo thứ tự: _“Tôi thấy bạn đang vẽ guitar”_, _“Bạn đã vẽ thêm một cái amp. Giờ nó là guitar điện. Lúc này chúng ta có thể tạo ra những bản nhạc rất ồn ào.”_, _“Với việc bạn đã thêm trống vào, bạn nghĩ sao về một ít nhạc hair metal (thể loại này là gì mình chịu luôn) từ những năm 80?”_ và _“Tôi thấy bạn đã thêm cây cọ vào, đổi sang bầu không khí bãi biển hơn nào!”. Mỗi tương tác đều đi kèm với một đầu ra âm thanh tương ứng_.
    ![Gemini liên tục tương tác mỗi khi một hình ảnh mới được vẽ thêm vào.](https://i.postimg.cc/Y9SYDnF2/21-gemini-demo-17.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini liên tục tương tác mỗi khi một hình ảnh mới được vẽ thêm vào._

18. Người dùng đưa ra một video một người đang thực hiện hành động và hỏi _“Họ đang diễn tả phim nào?”_. **Gemini** chính xác trả lời: _“Tôi nghĩ họ đang thể hiện lại cảnh phim đạn - thời gian trong phim The Matrix.”_
    ![Gemini đoán đúng được bộ phim.](https://i.postimg.cc/Y9yg56N6/22-gemini-demo-18.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini đoán đúng được bộ phim._

19. Người dùng chiếu một video về một con mèo (dễ thương) đang nhảy lên đầu tủ, dừng khi nó còn ở trên không trung và hỏi _“Bạn nghĩ điều gì sẽ xảy ra tiếp theo?”_. **Gemini** bị ăn cú lừa với câu trả lời: _“Con mèo sẽ nhảy lên tường và tiếp đất, nó sẽ là một con điểm 10 hoàn hảo (**Gemini** dùng purrfect ở đây chơi chữ perfect một cách nhạt nhẽo).”_ vì thực tế, con mèo rơi cái bịch xuống đất (tội nghiệp).
    ![Gemini bị ăn cú lừa.](https://i.postimg.cc/13x0RrkM/23-gemini-demo-19.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini bị ăn cú lừa._

20. Người dùng vẽ chòm sao Gemini và **Gemini** đoán chính xác.
    ![Gemini đoán chính xác hình ảnh chòm sao Gemini.](https://i.postimg.cc/BQPcGVVX/24-gemini-demo-20.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
    _Gemini đoán chính xác hình ảnh chòm sao Gemini._

Thật thú vị nhỉ! **Nhưng có một vài vấn đề nho nhỏ với những lời khen đẹp đẽ của Google dành cho Gemini, đặc biệt là với video demo trên…**

## Sự thật về Gemini

![Sundar Pichai lần đầu thông báo về sự ra mắt của Gemini tại hội nghị Google I/O 2023](https://i.postimg.cc/0NPpD22w/25-gemini-announcement.jpg)

_Có hai bài blog rất hay nói về **mặt còn lại của chiến dịch marketing Gemini của Google**, một là từ [Bloomberg](https://www.bloomberg.com/opinion/articles/2023-12-07/google-s-gemini-ai-model-looks-remarkable-but-it-s-still-behind-openai-s-gpt-4), và hai là từ [Big Technology](https://www.bigtechnology.com/p/googles-gemini-marketing-trick), mình vô cùng khuyến khích bạn đọc xem qua. Phần bên dưới chủ yếu là mình chỉ lấy thông tin từ hai bài blog trên và video của **Fireship**._

> **Thoạt đầu, có vẻ như ai nhìn thấy Gemini cũng không khỏi trầm trồ, phấn khích (đừng lo, vì mình cũng không phải là ngoại lệ). Tuy nhiên, thay vào đó, rất nhiều người sau khi nghiên cứu chuyên sâu hơn lại thể hiện mối lo ngại với Google. _Tại sao lại như thế?_**

### Video demo của Google

---

Qua video demo trên của Google, Gemini đã thể hiện được những khả năng:

- Nó có thể nhận diện những gì đang xảy ra trong video và phản hồi trong thời gian thực.
- Nó có thể làm việc và trả lời qua nhiều ngôn ngữ.
- Nó có thể theo dõi mọi thứ trong video đang diễn ra.
- Nó có thể nối điểm lại với nhau (gì hay thật mà).
- Nó có đầu ra đa phương thức (như ở trên nó có thể đưa ra câu trả lời văn bản đi kèm với âm thanh / hình ảnh).
- Nó là mô hình “bất cứ thứ gì → bất cứ thứ gì” (Fireship đùa rằng Gemini là “Anything to Anything model)
- Nó giỏi về logic và suy luận không gian.

Tuy nhiên, **có thể Gemini không ngầu như bạn tưởng**😅!

Google đã ghi trong phần mô tả video demo của mình: _“Trong video demo này, độ trễ đã được giảm và đầu ra của Gemini đã được rút gọn cho sự súc tích.”_ Điều đó có nghĩa là video trên đã qua chỉnh sửa, nhưng không ai ngoài Google biết nó đã được chỉnh sửa cỡ nào, chắc không sao đâu nhỉ?

![Mô tả dưới video demo Gemini của Google](https://i.postimg.cc/yxg9sDnw/26-gemini-demo-video-description.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_Phần mô tả video demo của Google._

Như mình đã nói ở trên, video demo của Google thể hiện sự tương tác giữa **Gemini** và người dùng như rằng nó là _Jarvis trong Iron Man_ - tương tác trực tiếp như người dùng đang thực hiện một cuộc gọi video cho **Gemini**.

**TUY NHIÊN!** Khi bạn đọc trong [bài blog nói rõ hơn về demo của Gemini](https://developers.googleblog.com/2023/12/how-its-made-gemini-multimodal-prompting.html), đầu vào lại không hề giống như video demo: Input được đưa vào không phải là video, cũng không phải là giọng nói của người dùng, mà là **các khung hình được cắt ra từ video và văn bản do người dùng nhập vào**. Nó khác với những gì Google ám chỉ qua video: _rằng một người có thể có một cuộc trò chuyện trôi chảy với **Gemini** trong khi nó quan sát và phản hồi trong thời gian thực với thế giới xung quanh nó._

![Người dùng đưa vào hình ảnh bàn tay và hỏi Gemini thấy gì](https://i.postimg.cc/MHCBTzFX/27-gemini-demo-blog-1.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_Một ví dụ demo của Gemini trong bài blog demo từ Google._

Không chỉ thế, một vài ví dụ trong video demo còn khác với ví dụ trong blog, như trong bài blog, khi người dùng thực hiện hành động kéo - búa - bao và đố **Gemini** đoán, văn bản đầu vào còn cho **Gemini** gợi ý rằng **_“đây là một trò chơi”_**. Trong khi đó, ở video demo, người dùng chỉ cần đưa bàn tay vào thực hiện hành động, **Gemini** sẽ tự động đoán ngay đó là trò _oẳn tù tì_.

![Người dùng đưa hình ảnh tay thể hiện kéo - búa - bao cùng với gợi ý, hỏi Gemini họ đang làm gì và nhận được câu trả lời đúng](https://i.postimg.cc/MZNVtYpx/28-gemini-demo-blog-2.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_Trong bài blog demo, Google đã phải đưa gợi ý cho Gemini._

> _“[Google] cho thấy một người dùng nói chuyện với **Gemini**, nhưng họ chỉ đang thuật lại một văn bản trò chuyện. [Google] cho thấy một video chuyển động, nhưng thực tế họ lại đưa **Gemini** hình ảnh tĩnh. [Google] cho thấy đầu ra nhanh chóng, nhưng tốc độ phản hồi đã được tua nhanh lên. [Google] cho thấy kết quả đầu ra chặt cẽ của mô hình, nhưng đã rút ngắn chúng ‘để đảm bảo sự súc tích’. [Google] cho thấy câu trả lời tuyệt vời, ngắn gọn và vẫn đầy đủ, nhưng trong blog lại đưa vào văn bản đầu vào dài hơn.”_
>
> **\- Alex Kantrowitz, Big Technology.**

Ngoài ra, Google cũng không nói rõ trong video là mô hình được sử dụng ở đây (hiển nhiên) là **Gemini Ultra**, model chưa được tung ra, nhưng lại là điểm quan tâm lớn nhất với công chúng hiện tại. Điều này rõ ràng là chủ đích của Google: _Họ muốn ta liên tưởng màn thể hiện tuyệt vời trong video đến không chỉ **Gemini Ultra**, mà còn với **Gemini Pro** và **Gemini Nano**, hai model có các điểm chuẩn kém hơn **GPT-4**._

Sự thật là, việc thổi phồng trong demo không còn là một vấn đề mới lạ trong giới công nghệ, và Google cũng không phải là ngoại lệ.  
Tuy Google đã rất minh bạch về demo với **Gemini** qua những tài liệu mà họ công khai, họ cũng đã chỉnh sửa và thay đổi rất nhiều chi tiết quan trọng về demo trong video demo vì phần lớn người xem sẽ chỉ dừng lại ở video ấy, **vì Gemini sẽ bớt ngầu đi nếu họ làm vậy, và vì Google sẽ nhận lại được sự ủng hộ to lớn từ công chúng nhờ vào đó.**

_Không biết như thế nào chứ theo mình, người tiên phong trong cuộc đua AI - Google, cảm thấy việc họ phải thổi phồng lên video demo của mình để có màn thể hiện xuất sắc hơn so với OpenAI là một điều khiến mình khá sững sờ._

### So sánh với GPT-4

---

Gemini đã nắm bắt được mọi dòng tin tức hàng đầu nhờ vào sự tuyên bố hùng hồn: **Gemini (Ultra) đã vượt qua GPT-4 trên (gần như) mọi điểm chuẩn, là mô hình tiên tiến nhất ngày nay**.

Hãy cùng mình quay lại với bảng so sánh các điểm chuẩn của **Gemini** và **GPT-4**:

![Bảng so sánh điểm chuẩn 1](https://i.postimg.cc/ZqwyN8MG/29-gemini-benchmark-report-1.jpg)
![Bảng so sánh điểm chuẩn 2](https://i.postimg.cc/wTNJrs1N/30-gemini-benchmark-report-2.jpg)

2 bảng trên cho thấy **Gemini Ultra** của _Google_ **đánh bại GPT-4** của _OpenAI_ trên hầu hết mọi điểm chuẩn. Bài đánh giá các mô hình AI này dựa trên những thứ như vật lý trung học, luật chuyên môn và các tình huống đạo đức, và cuộc đua AI hiện tại được đánh giá gần như hoàn toàn trên những khả năng như vậy.

Tuy nhiên, nếu chúng ta xem kĩ, **Gemini Ultra** chỉ đánh bại **GPT-4** bởi vài phần trăm. Nói cách khác, đúng vậy, **_mô hình tối tân nhất của Google đã đem lại được một ít sự phát triển so với mô hình mà OpenAI hoàn thành một năm trước_**, và ta còn chưa kể đến việc **_Gemini Ultra thậm chí vẫn chưa được tung ra cho công chúng_**. Hay nói thêm một cách khác hơn nữa, tính đến thời điểm hiện tại, **_OpenAI đã có ít nhất một năm để vượt qua vài phần trăm mà Gemini Ultra hơn được họ_**.  
Là một người luôn cực kì ủng hộ Google, mình thấy đây rõ ràng là một điều rất đáng quan ngại.

Ngoài ra, đừng quên một tuyên bố khác của Google quan trọng không kém: **Gemini là mô hình đầu tiên vượt qua con người ở cấp độ chuyên gia trong khả năng hiểu ngôn ngữ đa nhiệm lớn (MMLU)**.

![Gemini đạt 90,0% so với con người ở cấp độ chuyên môn là 89,8% và 86,4% của GPT-4](https://i.postimg.cc/YCwgBqFs/31-gemini-vs-human-mmlu.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_Google tự hào thông báo Gemini là mô hình đầu tiên vượt qua con người trên MMLU trên website về Gemini._

Điều thú vị ở đây là, nếu bạn chú ý kĩ, ở đây Google lại **_so sánh điểm chuẩn CoT@32 của Gemini Ultra với điểm chuẩn 5-shot_** của OpenAI. Ôi! Toàn là những ngôn từ phức tạp và những con số rối lắm! Thoạt đầu, mình cũng không hiểu và để tâm đoạn này lắm, nhưng thực ra nó cũng khá đơn giản thôi.

Trước hết, **MMLU là gì**? Bạn đọc có thể nghiên cứu kĩ hơn về MMLU trong [paper này](https://arxiv.org/pdf/2009.03300.pdf). Nhưng nói một cách đơn giản, MMLU là _một bài kiểm tra trắc nghiệm_ như SAT, gồm 57 chủ đề khác nhau, có độ khó đầy đủ từ sơ cấp đến chuyên môn nâng cao, và nó kiểm tra kiến thức về thế giới cũng như khả năng giải quyết vấn đề của một mô hình văn bản.

**CoT@32 và 5-shot thì sao**?

- **5-shot** (_Few-shot_ với k=5) nghĩa là mô hình được kiểm tra bằng cách đưa cho nó prompt với 5 ví dụ trước khi nó đưa ra lựa chọn trắc nghiệm. Nói cách khác, mô hình sẽ phải tông quát hóa những vấn đề dựa trên một tập dữ liệu cực kì giới hạn. Điều này khác với zero-shot (k=0) vì mô hình sẽ không được đưa ví dụ nào trước khi nó đưa ra đáp án cuối cùng.
- **CoT@32**, CoT ở đây viết tắt cho _Chain-of-Thought_ (chuỗi suy nghĩ), có nghĩa là mô hình sẽ có 32 bước suy luận trung gian trước khi mô hình đưa ra câu đáp án cuối cùng.

Không như trên website của Gemini, trong bài báo cáo kỹ thuật, Google không so sánh điểm chuẩn _CoT@32 với 5-shot_, mà vừa so sánh _CoT@32 với CoT@32_ và _5-shot với 5-shot_.

![Gemini Ultra đạt 90,04% ở CoT@32 và 83,7% ở 5-shot, còn GPT-4 đạt 87,29$ ở CoT@32 và 86,4% ở 5-shot](https://i.postimg.cc/W16ZNL6b/32-gemini-vs-gpt4-mmlu.jpg)

**_Điều cực kỳ thú vị ở đây là, quả thật Gemini Ultra đã vượt qua con người ở cấp độ chuyên môn trong bài kiểm tra MMLU, và quả thật nó đã vượt qua GPT-4 ở điểm chuẩn CoT@32, nhưng khi so sánh điểm chuẩn 5-shot, nó lại thua GPT-4._**

Thôi, so sánh nhiêu đấy đủ rồi! Hãy cùng mình đến với phần cuối cùng của bài blog đã khá dài này: **kết luận**.

## Kết luận

Dù bên trên, mình có nói sự thật của Google là rất đáng quan ngại, và có vẻ như đến thời điểm hiện tại, sự ra mắt của **Gemini** vẫn chưa đẩy Google lên quá xa trong cuộc đua AI, nhưng mình vẫn luôn giữ niềm tin của mình ở Google.

Google, dù bị vượt qua trong cuộc đua ấy, vẫn luôn đem đến những đóng góp to lớn và quan trọng trong giới trí tuệ nhân tạo, điển hình là **Transformer**, thứ mà mọi LLM, từ **Gemini**, _ChatGPT_ hay _Grok_ đều sử dụng. Sự ra mắt của **Gemini**, đặc biệt là **Gemini Ultra**, là một tin cực kì đáng mong đợi và là một sự phát triển đáng kể trong cuộc đua ấy.

Ngoài ra, thứ mình muốn bạn đọc rút ra được từ **Gemini** là:  
**_Tất nhiên chúng ta không nên quá đa nghi mọi lời thông báo, mọi tuyên bố được đưa ra, nhưng việc nhìn nhận một chủ đề, một vấn đề một cách khách quan, một cách toàn diện cũng vô cùng quan trọng. Dù nói gì đi chăng nữa, bản thân việc đánh giá, bản thân các điểm chuẩn, ít nhất là trong giới trí tuệ nhân tạo, chỉ là những con số mà thôi - và bản thân Google cũng thừa nhận điều đó trong bản báo cáo của họ._**

![“Việc đánh giá qua các điểm chuẩn là cực kì khó khăn và có thể bị ảnh hưởng bởi sai lạc dữ liệu.” Google ghi trong bản báo cáo kĩ thuật về Gemini.](https://i.postimg.cc/263L7qpV/33-gemini-report-evaluation-comment.jpg){: lqip="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAQEBAf/AABEIAAYACgMBEQACEQEDEQH/xAGiAAABBQEBAQEBAQAAAAAAAAAAAQIDBAUGBwgJCgsQAAIBAwMCBAMFBQQEAAABfQECAwAEEQUSITFBBhNRYQcicRQygZGhCCNCscEVUtHwJDNicoIJChYXGBkaJSYnKCkqNDU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6g4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2drh4uPk5ebn6Onq8fLz9PX29/j5+gEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoLEQACAQIEBAMEBwUEBAABAncAAQIDEQQFITEGEkFRB2FxEyIygQgUQpGhscEJIzNS8BVictEKFiQ04SXxFxgZGiYnKCkqNTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqCg4SFhoeIiYqSk5SVlpeYmZqio6Slpqeoqaqys7S1tre4ubrCw8TFxsfIycrS09TV1tfY2dri4+Tl5ufo6ery8/T19vf4+fr/2gAMAwEAAhEDEQA/APB/2X9F+JGu2ckcHirR9T8XwXHhvw9puu3umNoOhWuo+I/Gg8KweJJ/B9qviHSbzUdPQxajcQOUstVuZLuOaCBJIXg/b/F/jHPMyzng/MeJ8VUx88JkeCy+vUw2Ixaq5hl2Eq1rfWVXxF1irqpR0rSoypUcPOCoRf1agRw/s8wzClRhCjSnUdXD4f2tSpDDwnXqRp0Pbzj7WqqdPlh7WUVOTTm1zN3+BfHum6nY+OfGlld6No2oXdn4s8RWt1fy+MfiCsl7cW+sXkU13Iq6kFV7mRGmdVAUM5AAFfl8uKaVaUq1COJhRqydSjGcUpxpVHzU4yUMU4KSg0pKLcU0+V2sdtTJqsKlSE5UuaM5RlyzqOPNGTTs3TTauna6Tt0R/9k=" }
_“Việc đánh giá qua các điểm chuẩn là cực kì khó khăn và có thể bị ảnh hưởng bởi sai lạc dữ liệu.” Google ghi trong bản báo cáo kĩ thuật về Gemini._

Cuối cùng, **hãy chỉ tin khi bạn được tận mắt nhìn thấy nó**. Ở thời điểm hiện tại, thứ duy nhất tôi thấy được là **Gemini Pro** (tích hợp trong Bard), và thứ duy nhất tôi tin được là điều Google cũng không ngại che giấu: **_Gemini Pro vẫn chưa vượt qua được GPT-4 ở thời điểm hiện tại_**. Dù vậy, **Gemini Pro** tốt hơn **GPT-3.5**, và nó miễn phí (ai chẳng thích đồ miễn phí, nhỉ)!

**_Hãy dùng thử Gemini Pro, hãy trải nghiệm một cái nhìn nhỏ về thứ công nghệ mới nhất, và hãy cùng mình đón chờ thêm những thông tin giật gân mới về cuộc đua AI!_**

## Tài liệu tham khảo

1. [Youtube \| Fireship \| The Gemini Lie](https://www.youtube.com/watch?v=90CYYfl9ntM)
1. [Google DeepMind \| Gemini](https://deepmind.google/technologies/gemini/#introduction)
1. [Google Blog \| Introducing Gemini: our largest and most capable AI model](https://blog.google/technology/ai/google-gemini-ai/?utm_source=gdm&utm_medium=referral#sundar-note)
1. [Google for Developers \| How it’s Made: Interacting with Gemini through multimodal prompting](https://developers.googleblog.com/2023/12/how-its-made-gemini-multimodal-prompting.html)
1. [Gemini: A Family of Highly Capable Multimodal Models](https://storage.googleapis.com/deepmind-media/gemini/gemini_1_report.pdf)
1. [Google Blog \| Learn more about Gemini, our most capable AI model](https://blog.google/technology/ai/gemini-collection/)
1. [VnEconomy \| Google trình làng Gemini: Mô hình AI thông minh lớn nhất có năng lực mạnh hơn, cạnh tranh với GPT-4](https://vneconomy.vn/techconnect//google-trinh-lang-geminimo-hinh-ai-thong-minh-lon-nhat-co-nang-luc-manh-hon-canh-tranh-voi-gpt-4.htm)
1. [Youtube \| Google \| Gemini: Processing and understanding raw audio](https://youtu.be/D64QD7Swr3s?si=RMua_UfN7PcD2LXR)
1. [Google Blog \| Enabling next-generation AI workloads: Announcing TPU v5p and AI Hypercomputer](https://cloud.google.com/blog/products/ai-machine-learning/introducing-cloud-tpu-v5p-and-ai-hypercomputer)
1. [Youtube \| Google \| Hands-on with Gemini: Interacting with multimodal AI](https://youtu.be/UIZAiXYceBI?si=05Dtg24bYFdH4lT4)
1. [Big Technology \| Google’s Gemini Marketing Trick](https://www.bigtechnology.com/p/googles-gemini-marketing-trick)
1. [Measuring Massive Multitask Language Understanding](https://arxiv.org/pdf/2009.03300.pdf)
1. [The Verge \| Google launches Gemini, the AI model it hopes will take down GPT-4](https://www.theverge.com/2023/12/6/23990466/google-gemini-llm-ai-model)

> _Đây là bài blog đầu tiên của mình. Xui (may mắn?) thay, nó là một bài viết dài hơn mình dự định nhiều. Mình sẽ rất vui nếu nhận được góp ý của mọi người, cũng như mình sẽ cố gắng trả lời mọi bàn luận, thắc mắc và đề xuất mà mình nhận được! Hãy để lại một lời chào cho mình ở [Page Facebook của BleeVN nhé](https://www.facebook.com/bleevn)!  
> Mình đang cố gắng setup hệ thống comment, mong mọi người thông cảm!_
