# **Làm quen với Linux**

Chào mừng đến với thế giới của Linux, hệ điều hành được phát triển bởi hàng nghìn người trên khắp thế giới\! Trong chương này, bạn tìm hiểu về chính Linux \- nó là gì, bắt nguồn từ đâu, và tại sao nó nhận được nhiều sự chú ý như vậy. Hãy chuẩn bị đón nhận những thách thức về cách mà phần mềm được phát triển và được bán, và mở rộng tư duy của bạn để đón nhận những khả năng mới.

## **Nó có thật sự miễn phí?**

Việc thấu hiểu Linux đòi hỏi một sự thay đổi tư duy triệt để về cách bạn sở hữu và sử dụng phần mềm máy tính. (Lưu ý: Khi nói "triệt để", ý tôi là đi sâu vào tận gốc rễ của vấn đề, chứ không phải là kiểu đeo vòng hạt và cắm trại biểu tình trong tòa nhà hành chính đâu nhé.) Bước đầu tiên trong quá trình thay đổi tư duy này là bạn phải thay đổi cách hiểu thông thường của mình về từ "free" là đại diện cho sự tự do, không phải "bữa trưa miễn phí". Đúng vậy; bạn hoàn toàn có thể bán phần mềm "tự do" để thu phí... và thực tế là bạn được khuyến khích làm như vậy, miễn là bạn cũng trao lại quyền tự do tương đương cho từng người nhận phần mềm đó.

Đừng vò đầu bứt tóc quá nhiều; những khái niệm này ban đầu rất khó nắm bắt, đặc biệt là khi bạn xét đến những thói quen tư duy mà bạn đã tiếp nhận từ các bộ phận tiếp thị của ngành công nghiệp phần mềm thương mại. Có lẽ bạn không biết rằng khi bạn mua hầu hết các gói phần mềm độc quyền, bạn không thực sự sở hữu phần mềm đó. Thay vào đó, bạn chỉ được cấp quyền sử dụng phần mềm trong những giới hạn do bên cấp phép quy định.

Linux cũng có một giấy phép. Tuy nhiên, động cơ và mục đích của giấy phép này rất khác so với hầu hết các phần mềm thương mại. Thay vì sử dụng giấy phép để hạn chế việc sử dụng phần mềm, Giấy phép Công cộng Chung GNU (GPL) mà Linux sử dụng đảm bảo rằng phần mềm sẽ luôn mở cho bất kỳ ai. Không một công ty nào có thể sở hữu Linux hoặc ra lệnh về cách bạn sử dụng hay sửa đổi Linux — mặc dù họ có thể có bản quyền và thương hiệu riêng cho các phiên bản phân phối khác nhau của họ, chẳng hạn như Red Hat và SUSE. Về bản chất, bạn đã sở hữu Linux và bạn có thể sử dụng nó cho bất kỳ mục đích nào bạn thích, miễn là bạn truyền đạt lại những quyền tự do của GPL cho bất kỳ người nhận phần mềm nào tiếp theo.

## **Linux: Cuộc cách mạng hay chỉ là một hệ điều hành khác?**

Trước khi đi sâu hơn vào Linux, tôi cần phải làm rõ một số thuật ngữ.

Tux là tên chính thức của chú chim cánh cụt linh vật đại diện cho Linux. Có tin đồn rằng người tạo ra Linux, Linus Torvalds, khá thích những cư dân ăn mặc bảnh bao này của vùng Nam Cực.

Hệ điều hành là phần mềm chạy trên máy tính của bạn, xử lý mọi tương tác giữa bạn và phần cứng. Dù bạn đang viết thư, tính toán ngân sách hay quản lý các công thức nấu ăn trên máy tính, hệ điều hành chính là nguồn dưỡng khí thiết yếu cho máy tính của bạn hoạt động. Hơn nữa, một hệ điều hành không chỉ là một chương trình đơn lẻ; nó bao gồm hàng trăm chương trình và tiện ích nhỏ hơn cho phép con người chúng ta sử dụng máy tính để làm một việc gì đó hữu ích. Sau đó, bạn chạy các chương trình khác (chẳng hạn như phần mềm soạn thảo văn bản) trên nền tảng của hệ điều hành này để hoàn thành mọi việc.

Trong lịch sử công nghệ gần đây, Linux đã phát triển từ một sân chơi của dân công nghệ thành một giải pháp vững chắc cho các doanh nghiệp. Cùng một phần mềm từng bị coi là "nổi loạn" nay lại đang được áp dụng và quảng bá bởi các nhà lãnh đạo trong ngành như IBM, Hewlett-Packard, Motorola, Microsoft và Intel. Mỗi nhà sản xuất máy tính này đều xác định rằng Linux mang lại giá trị cho khách hàng của họ theo một cách nào đó (cũng như cho các hoạt động nội bộ của chính họ).

Linux từng bị gán mác là "chỉ là một hệ điều hành khác". Nhìn bề ngoài thì có vẻ như vậy, nhưng nếu bạn nhìn sâu hơn, bạn có thể thấy rằng điều này không đúng. Dự án Linux là lá cờ đầu dẫn dắt xu hướng hiện tại hướng tới mã nguồn mở và phần mềm tự do trong ngành công nghiệp máy tính. Là một hệ điều hành vững chắc nhờ vào mô hình mà nó được (và tiếp tục được) phát triển, Linux đại diện cho rất nhiều điều tốt đẹp trong việc phát triển phần mềm.

Hai điểm khác biệt cơ bản tách biệt Linux khỏi phần còn lại của nhóm các hệ điều hành:

* Linux được cấp phép theo Giấy phép Công cộng Chung GNU độc đáo và tài tình, mà bạn có thể đọc ở phần tiếp theo.  
* Linux được phát triển và duy trì bởi một đội ngũ toàn cầu gồm các lập trình viên tình nguyện và được trả lương, làm việc cùng nhau qua Internet.

Linux tuyệt vời vì nhiều lý do, bao gồm cả việc những người đã xây dựng nó từ con số không muốn nó mang những đặc tính sau:

* **Đa người dùng (Multiuser):** Nhiều hơn một người dùng có thể đăng nhập vào một máy tính cùng một lúc.  
* **Đa tiến trình (Multiprocess):** Tính đa nhiệm ưu tiên thực sự cho phép lõi hệ điều hành xử lý hiệu quả nhiều chương trình chạy cùng một lúc. Điều này rất quan trọng để cung cấp nhiều dịch vụ trên một máy tính.  
* **Đa nền tảng (Multiplatform):** Trong khi Mac OS chỉ chạy trên CPU Intel và Windows chỉ chạy trên CPU Intel và ARM, Linux hiện chạy trên hơn 24 nền tảng CPU (loại phần cứng) khác nhau, bao gồm PC dựa trên Intel 32 và 64-bit, Digital/Compaq Alpha, tất cả các biến thể của Apple Macintosh, Sun SPARC, Apple iPod, CPU ARM, và thậm chí cả Microsoft XBox.  
* **Khả năng tương tác (Interoperable):** Linux hoạt động mượt mà với hầu hết các giao thức mạng (ngôn ngữ) và hệ điều hành, cho phép bạn tương tác với người dùng và máy tính chạy Microsoft Windows, UNIX, máy tính Apple Macintosh và các nhóm hệ thống chuyên biệt khác.  
* **Khả năng mở rộng (Scalable):** Khi nhu cầu tính toán của bạn tăng lên, bạn có thể dựa vào việc Linux sẽ phát triển cùng bạn. Cùng một hệ điều hành Linux có thể chạy trên một khung ảnh điện tử nhỏ, một máy tính để bàn, hoặc một hệ thống máy chủ cỡ lớn dùng cho công nghiệp.  
* **Tính di động (Portable):** Linux chủ yếu được viết bằng ngôn ngữ lập trình C. C là một ngôn ngữ được tạo ra đặc biệt để viết phần mềm cấp hệ điều hành và có thể dễ dàng được chuyển đổi (dịch) để chạy trên phần cứng máy tính mới.  
* **Tính linh hoạt (Flexible):** Bạn có thể cấu hình hệ điều hành Linux như một máy chủ mạng, bộ định tuyến, máy trạm đồ họa, PC văn phòng, máy tính giải trí gia đình, máy chủ tệp, máy chủ web, cụm máy chủ, hoặc gần như bất kỳ thiết bị tính toán nào khác mà bạn có thể nghĩ ra.  
* **Tính ổn định (Stable):** Nhân Linux (cốt lõi của hệ điều hành) đã đạt đến mức độ trưởng thành khiến hầu hết các nhà phát triển phần mềm phải ghen tị. Việc nghe báo cáo về các máy chủ Linux chạy trong nhiều năm mà không gặp sự cố là chuyện bình thường.  
* **Tính hiệu quả (Efficient):** Thiết kế mô-đun của Linux cho phép bạn chỉ bao gồm các thành phần cần thiết để chạy các dịch vụ bạn mong muốn. Ngay cả những máy tính cũ cũng có thể sử dụng Linux và trở nên hữu ích trở lại.  
* **Tự do / Miễn phí (Free):** Đối với hầu hết mọi người, khía cạnh hấp dẫn nhất của Linux là việc nó thường có sẵn miễn phí. Làm thế nào (những nhà tư bản lẩm bẩm) mà bất kỳ ai cũng có thể tạo ra một "chiếc bẫy chuột tốt hơn" mà không có động lực thu lại lợi nhuận trực tiếp bằng tiền?

Trong chương này, tôi dự định sẽ trả lời câu hỏi cuối cùng đó cho bạn. Tôi cũng hy vọng có thể vẽ nên một bức tranh về mô hình phát triển phần mềm mã nguồn mở đã tạo ra Linux.

## **VẬY LINUX BẮT NGUỒN TỪ ĐÂU?**

Cách nhanh nhất để hiểu Linux là xem qua di sản phong phú của nó. Mặc dù việc lập trình lõi Linux bắt đầu vào năm 1991, các khái niệm thiết kế đã dựa trên hệ điều hành UNIX đã được thử thách qua thời gian.

UNIX được phát triển tại Phòng thí nghiệm Điện thoại Bell vào cuối những năm 1960\. Các kiến trúc sư ban đầu của UNIX, làm việc trong thời kỳ có rất ít hệ điều hành, muốn tạo ra một hệ thống chia sẻ dữ liệu, chương trình và tài nguyên một cách hiệu quả và an toàn \- điều chưa từng có vào thời điểm đó (và vẫn đang được tìm kiếm cho đến tận bây giờ). Từ đó, UNIX đã phát triển thành nhiều phiên bản khác nhau; cây phả hệ hiện tại của nó phức tạp đến mức trông giống như một sự phá hoại của cây sắn dây rừng\!

Năm 1991, Linus Torvalds là một sinh viên khoa học máy tính tại Đại học Helsinki ở Phần Lan. Anh ấy muốn có một hệ điều hành giống với hệ thống UNIX mà anh ấy đã bắt đầu yêu thích tại trường đại học, nhưng cả UNIX và phần cứng để chạy nó đều đắt một cách vô lý. Một phiên bản UNIX có tên là Minix có sẵn miễn phí, nhưng nó không hoàn toàn đáp ứng được nhu cầu của anh. Vì vậy, với tư cách là một sinh viên khoa học máy tính, Torvalds đã nghiên cứu Minix và sau đó bắt tay vào tự viết một phiên bản mới. Theo lời của chính anh ấy (được lưu lại cho hậu thế trên Internet vì đây là một phiên bản đầu tiên của phòng chat trực tuyến), công việc của anh ấy "chỉ là một sở thích, sẽ không lớn lao và chuyên nghiệp như GNU."

Viết một hệ điều hành không phải là một nhiệm vụ nhỏ. Ngay cả sau sáu tháng làm việc chăm chỉ, Torvalds đã đạt được rất ít tiến bộ đối với tiện ích chung của hệ thống. Anh ấy đã đăng những gì mình có lên Internet \- và phát hiện ra rằng nhiều người có chung sự quan tâm và tò mò với anh ấy. Không lâu sau, một số bộ óc thông minh nhất trên khắp thế giới đã đóng góp vào dự án của Linus bằng cách thêm các tính năng nâng cao hoặc sửa lỗi trong mã nguồn.

### **Giải phẫu một Dự án Phần mềm Mã nguồn mở**

Đối với một người quan sát thông thường (và một số người ra quyết định CNTT của công ty), Linux dường như là một sự đột biến kỳ lạ – một sinh vật nổi loạn được sinh ra ngẫu nhiên bởi sự hỗn loạn. Rốt cuộc, làm thế nào mà một thứ phức tạp và phụ thuộc vào tính kỷ luật như một hệ điều hành máy tính lại có thể được phát triển bởi một nhóm lỏng lẻo các chuyên gia máy tính tình nguyện từ khắp nơi trên thế giới?

Giống như khoa học đang không ngừng cố gắng phân loại và giải thích mọi thứ tồn tại, các nhà bình luận công nghệ vẫn đang cố gắng hiểu làm thế nào mà phương pháp tiếp cận mã nguồn mở lại có thể tạo ra phần mềm vượt trội, đặc biệt là trong những trường hợp nó không tính phí. Thường thì các lý do liên quan nhiều đến khao khát thông thường của con người là muốn lấp đầy một nhu cầu bằng một giải pháp. Khi một lập trình viên trong thế giới Linux muốn một công cụ, lập trình viên đó chỉ cần viết ra một công cụ hoặc hợp tác với những người khác cũng muốn một gói phần mềm tương tự, và họ cùng nhau viết nó.

### **GNU là ai?**

Hãy tưởng tượng phần mềm được tạo ra từ nhu cầu thay vì dự báo lợi nhuận. Mặc dù UNIX cuối cùng đã trở thành phần mềm độc quyền đắt tiền, những ý tưởng và động cơ tạo ra nó ban đầu đều dựa trên những nhu cầu thực tế. Những gì mọi người thường gọi là hệ điều hành Linux thực chất là một tập hợp các công cụ phần mềm được tạo ra với mục đích rõ ràng là giải quyết các vấn đề tính toán cụ thể.

Tốc độ phổ biến của Linux cũng sẽ không thể đạt được nếu không có tầm nhìn của một người đàn ông mà Steven Levy (tác giả cuốn sách Hackers) gọi là "Hacker MIT AI-LAB Vĩ đại Cuối cùng" – theo ý nghĩa ban đầu của từ hacker là một người sành sỏi về lập trình, chứ không phải là ý nghĩa phổ biến hiện nay ám chỉ ý đồ tội phạm. Người tiên phong và ủng hộ phần mềm tự do này là Richard Stallman.

Viện Công nghệ Massachusetts (MIT) từ lâu đã nổi tiếng là nơi nuôi dưỡng những bộ óc vĩ đại nhất trong các lĩnh vực công nghệ. Năm 1984, Stallman, một sinh viên tài năng và lập trình viên xuất sắc tại MIT, phải đối mặt với một tình huống khó xử – bán tài năng của mình cho một công ty để đổi lấy một khoản tiền lớn hay cống hiến những món quà của mình cho thế giới. Ông ấy đã làm những gì tất cả chúng ta sẽ làm... đúng không?

Stallman đã bắt đầu một hành trình tạo ra một hệ điều hành hoàn toàn tự do mà ông sẽ cống hiến cho thế giới. Ông thấu hiểu và tiếp tục sống theo đạo đức hacker nguyên thủy, tuyên bố rằng thông tin muốn được tự do. Khái niệm này không mới trong thời đại của ông. Trong những ngày đầu của ngành công nghiệp máy tính, nhiều tiến bộ đã được tạo ra bằng cách tự do chia sẻ ý tưởng và mã lập trình. Các nhóm người dùng do nhà sản xuất tài trợ đã tập hợp những bộ óc giỏi nhất để giải quyết các vấn đề phức tạp. Đạo đức này, Stallman cảm thấy, đã bị mất đi khi các công ty bắt đầu tích trữ phần mềm như tài sản trí tuệ của riêng họ với mục đích duy nhất là lợi nhuận.

Như bạn có thể đã hiểu tính đến thời điểm này, mã nguồn có thể truy cập và phổ biến rộng rãi là điều tối quan trọng để phát triển phần mềm thành công. Mã nguồn là thuật ngữ chỉ văn bản mà con người có thể đọc được (trái ngược với các chữ tượng hình không gian mạng không thể đọc được trong một tệp "thực thi") mà một lập trình viên gõ để truyền đạt các lệnh cho máy tính.

Viết các chương trình máy tính bằng mã mà máy tính có thể chạy trực tiếp là một công việc vô cùng gian nan. Phần mềm máy tính hiện đại thường được viết bằng một ngôn ngữ thân thiện với con người và sau đó được biên dịch, hoặc dịch, sang bộ lệnh bản địa của máy tính. Để thay đổi phần mềm này, một lập trình viên cần có quyền truy cập vào mã nguồn của chương trình. Hầu hết phần mềm độc quyền chỉ xuất hiện dưới dạng sản phẩm đã biên dịch trước; nhà phát triển phần mềm bảo mật chặt chẽ mã nguồn của những chương trình đó.

Sau khi xác định rằng hệ điều hành của mình sẽ được xây dựng xung quanh khuôn khổ khái niệm của UNIX, Stallman muốn tên dự án phải phân biệt hệ thống của mình với UNIX. Vì vậy, ông đã chọn từ viết tắt đệ quy GNU (phát âm là ga-new), có nghĩa là GNU's Not Unix (GNU không phải là Unix).

Để tài trợ cho dự án GNU, Stallman đã tổ chức Tổ chức Phần mềm Tự do (FSF), tổ chức này bán phần mềm mã nguồn mở để giúp nuôi sống các lập trình viên làm việc trong quá trình phát triển liên tục của nó. (Hãy nhớ rằng, chúng ta đang nói đến miễn phí theo nghĩa sự tự do, không phải là bữa trưa miễn phí). Mặc dù tổ chức này và mục tiêu tạo ra một hệ điều hành hoàn chỉnh là cần thiết và quan trọng, một mảnh ghép quan trọng hơn nhiều phải được đặt vào đúng chỗ để bảo vệ phần mềm mới này khỏi những tên cướp biển doanh nghiệp lớn – một mối quan tâm vẫn còn quá phù hợp cho đến ngày nay khi một cựu công ty Linux cố gắng đánh cắp quyền sở hữu từ nhiều thập kỷ làm việc tình nguyện của hàng ngàn người trên khắp thế giới.

Giấy phép Công cộng Chung GNU (GPL) là một giấy phép phần mềm độc đáo và sáng tạo, sử dụng luật bản quyền để bảo vệ quyền tự do của người dùng phần mềm, điều này thường trái ngược với cách thức hoạt động của bản quyền. Nói chung, bản quyền là một sự chỉ định quyền sở hữu có thể thi hành và hạn chế việc sao chép bởi bất kỳ ai ngoại trừ chủ sở hữu bản quyền. Khi phần mềm được cấp phép theo GPL, người nhận bị ràng buộc bởi luật bản quyền phải tôn trọng quyền tự do của bất kỳ ai khác trong việc sử dụng phần mềm theo bất kỳ cách nào họ chọn. Phần mềm được cấp phép bằng GPL còn được gọi là phần mềm copyleft (trái ngược với copyright). Một cách khác để nhớ GPL là thông qua kết quả cuối cùng của nó: Guaranteed Public for Life (Đảm bảo Công cộng Trọn đời).

Mặc dù công việc của Stallman đã tạo tiền đề cho sự thăng tiến nhanh chóng về mức độ phổ biến của Linux, hệ điều hành mà ông và nhóm của mình đang làm việc đã mất nhiều thời gian hơn dự kiến. Nếu bạn quan tâm đến phiên bản hoàn chỉnh, hãy truy cập www.gnu.org/software/hurd/hurd.html.

### **Tóm lại thì ai phụ trách Linux?**

Khi một dự án mã nguồn mở phát triển, nhiều người khác nhau nổi lên như những nhà lãnh đạo. Nhà lãnh đạo này thường được biết đến như là một "nhà độc tài nhân từ" (benevolent dictator) của dự án. Một người trở thành nhà độc tài nhân từ có lẽ đã dành nhiều thời gian hơn bất kỳ ai khác cho một vấn đề cụ thể và thường có một số hiểu biết sâu sắc độc đáo. Thông thường, các từ "dân chủ" và "độc tài" không bao giờ được ghép đôi trong cùng một câu, nhưng mô hình mã nguồn mở là một quá trình rất dân chủ ủng hộ sự cai trị của một nhà độc tài nhân từ.

Linus Torvalds vẫn được coi là nhà độc tài nhân từ của nhân Linux (cốt lõi của hệ điều hành). Anh ấy là người cuối cùng quyết định những tính năng nào được thêm vào nhân và những tính năng nào không. Cộng đồng tin tưởng vào tầm nhìn và sự thận trọng của anh ấy. Trong trường hợp anh ấy mất hứng thú với dự án, hoặc cộng đồng quyết định rằng anh ấy đã lẩm cẩm, một nhà lãnh đạo mới sẽ nổi lên từ những người rất có năng lực đang làm việc cùng anh ấy.

### **Einstein cũng là một tình nguyện viên**

Một người làm tình nguyện viên hoặc cống hiến thời gian cho một dự án không nhất thiết là đang cung cấp một nỗ lực hạng hai (hoặc chỉ làm việc vào cuối tuần và ngày lễ). Trên thực tế, bất kỳ chuyên gia nhân sự nào cũng sẽ nói với bạn rằng những người chọn làm một công việc theo ý chí tự do của họ sẽ tạo ra những sản phẩm chất lượng cao nhất.

Các tình nguyện viên đóng góp cho các dự án mã nguồn mở thường là những nhà lãnh đạo trong lĩnh vực của họ, những người phụ thuộc vào sự hợp tác của cộng đồng để hoàn thành những công việc hữu ích. Khái niệm mã nguồn mở không xa lạ với cộng đồng khoa học. Quá trình đánh giá đồng cấp vô tư mà các dự án mã nguồn mở bồi dưỡng là rất quan trọng trong việc xác nhận một số tính năng hoặc khả năng mới là đúng về mặt kỹ thuật.

**GHI NHỚ:** Những ai vẽ nên cộng đồng mã nguồn mở như những người vi phạm bản quyền và kẻ trộm thường hiểu lầm hoặc hoàn toàn phớt lờ những vấn đề quan trọng này. Các lập trình viên mã nguồn mở rất tự hào về công việc của họ và cũng rất quan tâm đến bản quyền của chính họ, không muốn công việc của mình bị người khác đánh cắp – do đó mới có các giấy phép như GPL. Mối quan tâm này tạo ra một bầu không khí với sự tôn trọng lớn nhất đối với bản quyền. Những kẻ cướp biện hộ rằng chúng "chỉ đang mở mã nguồn" khi đánh cắp công sức khó nhọc của người khác đang sử dụng sai thuật ngữ này một cách nghiêm trọng để xoa dịu lương tâm của chính chúng.

Nhiều người cũng đã chỉ ra rằng nếu bản quyền bị vi phạm trong mã nguồn mở, thì rất dễ nhận biết. Hãy xem tin tức và chú ý xem các tập đoàn phần mềm lớn thường xuyên bị kết tội ăn cắp mã của người khác và kết hợp nó vào công việc của riêng họ như thế nào. Nếu sản phẩm cuối cùng là mã nguồn mở, bất kỳ ai cũng có thể dễ dàng kiểm tra và đảm bảo không có thứ gì bị đánh cắp trong đó. Như bạn có thể tưởng tượng, việc theo dõi các vi phạm bản quyền như vậy sẽ khó khăn hơn rất nhiều trong một mô hình nguồn đóng.

## **Đóng gói Linux: Bản Phân phối**

Một gói hệ thống Linux hoàn chỉnh được gọi là bản phân phối (distribution). Bản phân phối Linux chứa nhân Linux, các công cụ của dự án GNU và vô số các dự án phần mềm mã nguồn mở để cung cấp các chức năng khác nhau cho hệ thống.

Có rất nhiều bản phân phối Linux khác nhau để đáp ứng gần như bất kỳ yêu cầu tính toán nào mà bạn có thể có. Hầu hết các bản phân phối được tùy chỉnh cho một nhóm người dùng cụ thể, chẳng hạn như người dùng doanh nghiệp, người đam mê đa phương tiện, nhà phát triển phần mềm, hoặc người dùng gia đình bình thường.

Mỗi bản phân phối tùy chỉnh bao gồm các gói phần mềm cần thiết để hỗ trợ các chức năng chuyên biệt, chẳng hạn như phần mềm chỉnh sửa âm thanh và video cho những người đam mê đa phương tiện, hoặc các trình biên dịch và môi trường phát triển tích hợp (IDE) cho các nhà phát triển phần mềm.

Các bản phân phối Linux khác nhau thường được chia thành ba loại:

* Bản phân phối Linux cốt lõi đầy đủ  
* Bản phân phối chuyên biệt  
* Bản phân phối dùng thử trực tiếp (Live test)

Các phần sau đây mô tả các loại bản phân phối Linux khác nhau này và đưa ra một số ví dụ về bản phân phối Linux trong từng danh mục.

### **Các bản phân phối Linux cốt lõi**

Một bản phân phối Linux cốt lõi chứa hệ điều hành Linux và GNU, một hoặc nhiều môi trường máy tính để bàn đồ họa, và gần như mọi ứng dụng Linux có sẵn, sẵn sàng để cài đặt và chạy. Bản phân phối Linux cốt lõi cung cấp cửa hàng trọn gói cho một bản cài đặt Linux hoàn chỉnh, bất kể yêu cầu của bạn là gì\!

Bảng 1-1 hiển thị một số bản phân phối Linux cốt lõi phổ biến hiện có.

**Bảng 1-1: Các Bản phân phối Linux Cốt lõi**

| Bản phân phối | Mô tả |
| :---- | :---- |
| **Slackware** | Một trong những bộ phân phối Linux nguyên bản, phổ biến với các chuyên viên (geek) Linux |
| **Red Hat** | Một bản phân phối thương mại dành cho doanh nghiệp được sử dụng chủ yếu cho máy chủ |
| **CentOS** | Phiên bản mã nguồn mở của Red Hat được thiết kế để thử nghiệm |
| **Fedora** | Một phiên bản mã nguồn mở khác của Red Hat, nhưng được thiết kế để sử dụng tại nhà |
| **Gentoo** | Bản phân phối được thiết kế cho người dùng Linux nâng cao, chỉ chứa mã nguồn Linux |
| **SUSE** | Một bản phân phối thương mại dành cho doanh nghiệp |
| **Debian** | Phổ biến với các chuyên gia Linux và các sản phẩm Linux thương mại |

Trong những ngày đầu của Linux, một bản phân phối được phát hành dưới dạng một bộ đĩa mềm. Bạn phải tải xuống các nhóm tệp và sau đó sao chép chúng theo cách thủ công vào đĩa. Thường sẽ mất 20 đĩa trở lên để tạo thành toàn bộ bản phân phối\! Không cần phải nói, đó là một trải nghiệm đau khổ.

Sau này, khi máy tính gia đình thường có sẵn đầu đĩa CD hoặc DVD, các bản phân phối Linux đã được phát hành dưới dạng bộ CD hoặc đĩa DVD đơn lẻ. Thường thì bạn sẽ tải xuống một tệp hình ảnh DVD duy nhất (thường được gọi là tệp ISO theo phần mở rộng tệp được sử dụng), sau đó ghi hình ảnh đó lên đĩa DVD. Điều đó làm cho việc cài đặt Linux dễ dàng hơn nhiều.

Ngày nay, với việc nhiều máy tính từ bỏ đầu đĩa DVD, các bản phân phối Linux vẫn được phát hành dưới dạng tệp hình ảnh ISO, nhưng giờ đây các tiện ích cho phép bạn ghi chúng lên ổ đĩa flash USB có thể khởi động. Máy tính hiện đại có khả năng khởi động từ ổ USB, vốn vẫn thường thấy trên cả máy trạm và máy chủ.

Mặc dù có nhiều tùy chọn có sẵn trong một bản phân phối là điều tuyệt vời cho các chuyên viên Linux, nó có thể trở thành cơn ác mộng đối với những người mới bắt đầu sử dụng Linux. Hầu hết các bản phân phối hỏi một loạt câu hỏi trong quá trình cài đặt để xác định ứng dụng nào cần tải theo mặc định, phần cứng nào được kết nối với PC, và cách cấu hình phần cứng. Những người mới bắt đầu thường thấy những câu hỏi này gây bối rối. Kết quả là, họ thường tải quá nhiều chương trình lên máy tính của mình hoặc tải không đủ, và sau đó phát hiện ra rằng máy tính của họ sẽ không làm được những gì họ muốn.

May mắn thay cho người mới bắt đầu, có một cách đơn giản hơn nhiều để cài đặt Linux.

### **Các bản phân phối Linux chuyên biệt**

Qua nhiều năm, một nhóm nhỏ các bản phân phối Linux mới đã xuất hiện, được thiết kế đặc biệt cho những người dùng Linux mới. Chúng thường dựa trên một trong những bản phân phối cốt lõi, nhưng chỉ chứa một tập hợp con các ứng dụng có ý nghĩa cho một khu vực sử dụng cụ thể.

Bên cạnh việc cung cấp phần mềm chuyên dụng (chẳng hạn như chỉ có các sản phẩm văn phòng cho người dùng doanh nghiệp, hoặc trò chơi cho game thủ), các bản phân phối Linux tùy chỉnh cũng cố gắng giúp người dùng Linux mới bằng cách tự động phát hiện và tự động cấu hình các thiết bị phần cứng thông thường. Điều này giúp việc cài đặt Linux trở thành một quá trình thú vị hơn nhiều.

Bảng 1-2 hiển thị một số bản phân phối Linux chuyên biệt phổ biến hiện có và lĩnh vực chuyên môn của chúng.

**Bảng 1-2: Các Bản phân phối Linux Chuyên biệt**

| Bản phân phối | Mô tả |
| :---- | :---- |
| **Mint** | Một bản phân phối máy tính để bàn được cấu hình để thay thế một máy trạm Windows tiêu chuẩn |
| **Ubuntu** | Cung cấp các bản phân phối cho máy tính để bàn và máy chủ được thiết kế để sử dụng ở trường học và gia đình |
| **MX Linux** | Một bản phân phối máy tính để bàn cho người dùng gia đình có phần cứng cũ hơn |
| **openSUSE** | Phiên bản mã nguồn mở của bản phân phối SUSE thương mại |
| **PCLinuxOS** | Một bản phân phối tập trung vào hỗ trợ thẻ đồ họa và thẻ âm thanh nâng cao |
| **Puppy** | Một bản phân phối nhỏ gọn khác chạy tốt trên các PC cũ |

**MẸO:** Đó chỉ là một phần nhỏ của các bản phân phối Linux chuyên biệt. Có hàng trăm bản phân phối Linux chuyên biệt theo đúng nghĩa đen, và nhiều bản phân phối khác đang liên tục xuất hiện trên Internet. Bất kể chuyên môn của bạn là gì, bạn có thể sẽ tìm thấy một bản phân phối Linux dành cho mình.

Bạn có thể nhận thấy rằng thường một bản phân phối Linux sẽ phát hành nhiều phiên bản khác nhau của nó để bao phủ nhiều lĩnh vực hơn. Ví dụ, Ubuntu phát hành bản phân phối riêng biệt mà mỗi bản phân phối sử dụng một môi trường máy tính để bàn khác nhau.

### **Bản phân phối Linux Live (Trực tiếp)**

Một hiện tượng tuyệt vời trong thế giới Linux là bản phân phối đĩa DVD Linux có khả năng khởi động, ban đầu được gọi là LiveDVD. Ngày nay, hầu hết các máy tính cho phép bạn khởi động bằng cách đọc hệ điều hành từ DVD hoặc ổ USB thay vì ổ cứng. Điều này cho phép bạn xem thử hệ thống Linux sẽ như thế nào mà không cần thực sự cài đặt nó.

Để tận dụng tính năng này, một số bản phân phối Linux tạo tệp ISO có thể khởi động mà bạn có thể ghi vào đĩa DVD hoặc USB. Các bản phân phối này chứa một tập hợp con của hệ thống Linux đầy đủ. Do giới hạn về kích thước, bản mẫu dùng thử không thể chứa toàn bộ hệ thống Linux, nhưng bạn sẽ ngạc nhiên về tất cả những phần mềm mà chúng có thể nhồi nhét vào\! Kết quả là, bạn có thể khởi động PC của mình từ đĩa DVD hoặc USB, rồi sau đó cài đặt các gói hệ thống còn lại bạn cần từ Internet.

Đây là một cách tuyệt vời để kiểm tra các bản phân phối Linux khác nhau mà không cần phải can thiệp rắc rối vào PC của bạn. Chỉ cần cắm DVD hoặc USB vào và khởi động\! Tất cả phần mềm Linux sẽ chạy trực tiếp từ thiết bị DVD hoặc USB. Ngày nay, hầu như mọi bản phân phối Linux đều có phiên bản Live, do đó, bạn có thể dễ dàng tải xuống một bản phân phối từ Internet và ghi nó lên DVD (hoặc USB) để chạy thử.

Một số bản phân phối Linux Live, chẳng hạn như Ubuntu, cũng cho phép bạn cài đặt bản phân phối Linux trực tiếp từ thiết bị Live. Điều này cho phép bạn khởi động bằng đĩa DVD hoặc USB, lái thử bản phân phối Linux và sau đó nếu thích, hãy cài đặt nó lên ổ cứng của bạn. Tính năng này vô cùng tiện dụng và thân thiện với người dùng.

Như với tất cả mọi thứ tốt đẹp khác, các bản phân phối Linux Live cũng có một số nhược điểm. Bởi vì bạn truy cập mọi thứ từ đĩa DVD hoặc USB, các ứng dụng chạy chậm hơn, đặc biệt nếu bạn đang sử dụng máy tính và ổ đĩa DVD cũ hơn, chậm hơn. Ngoài ra, bất kỳ thay đổi nào bạn thực hiện đối với hệ thống Linux sẽ biến mất ở lần khởi động lại tiếp theo.