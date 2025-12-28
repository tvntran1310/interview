# HTTP

## Overview of HTTP

1. [HTTP là gì và nó hoạt động như thế nào?]()
2. [HTTP là giao thức trạng thái hay không trạng thái? Tại sao nói HTTP “stateless but not sessionless”?]()
3. [Làm thế nào một trang web được hiển thị đầy đủ sau khi gửi yêu cầu HTTP?]()
4. [Proxy là gì và vai trò của proxy trong hệ thống HTTP?]()
5. [Một HTTP Request gồm những phần nào?]()
6. [Phân biệt các HTTP method chính như GET, POST, PUT, DELETE?]()
7. [Một HTTP Response gồm những thành phần nào?]()
8. [Status code là gì? Bạn có thể liệt kê vài status code thường gặp và ý nghĩa của chúng?]()
9. [HTTP/1.0 và HTTP/1.1 khác nhau ở điểm gì?]()
10. [HTTP pipelining là gì và tại sao lại ít được dùng?]()
11. [HTTP/2 đã giải quyết vấn đề gì so với HTTP/1.x?]()
12. [HTTP Cache hoạt động như thế nào và vì sao lại quan trọng?]()

## A typical HTTP session

1. [HTTP session là gì trong bối cảnh client-server?]()
2. Phần dữ liệu (body) trong HTTP request thường dùng trong trường hợp nào?
3. Từ HTTP/1.1 trở đi, phiên (session) được duy trì khác gì so với HTTP/1.0?
4. Ý nghĩa của cơ chế keep-alive trong một phiên HTTP là gì?
5. Mô tả trình tự dòng lệnh ví dụ cho một HTTP GET request và ý nghĩa của từng phần.
6. Khi server trả về status code 404 trong một phiên HTTP, điều đó có nghĩa gì?
7. Tại sao server không thể gửi dữ liệu tới client nếu client không gửi request?

## HTTP messages

1. [HTTP messages là gì và chúng được dùng để làm gì?]()
2. [Có bao nhiêu loại HTTP message và mỗi loại dùng cho mục đích gì?]()
3. [HTTP/1.x và HTTP/2 khác nhau như thế nào về cách biểu diễn message?]()
4. [Start-line trong HTTP request gọi là gì và nó gồm những phần nào?]()
5. [Status-line trong HTTP request gọi là gì và nó gồm những phần nào?]()
6. [HTTP method là gì? Hãy kể vài method phổ biến và mục đích của chúng.]()
7. [Request headers đóng vai trò gì trong HTTP request?]()
8. [Giải thích khái niệm head-of-line (HOL) blocking và cách HTTP/2 giải quyết nó.]()
9. [Trong HTTP messages, làm thế nào để xử lý multipart bodies? Cho ví dụ use-case.]()

## MIME types

1. [MIME type là gì và nó được dùng để làm gì trong HTTP?]()
2. [Tại sao browser lại dựa vào MIME type thay vì phần mở rộng file?]()
3. [Parameter trong MIME type có tác dụng gì? Cho ví dụ.]()
4. [Phân biệt discrete type và multipart type trong MIME types?]()
5. [MIME type nào dùng cho JSON và tại sao nó quan trọng trong lập trình web?]()
6. [Kể vài MIME type thông dụng cho hình ảnh (images) và giải thích tầm quan trọng của chúng.]()
7. [Vì sao application/octet-stream thường được dùng cho file nhị phân chưa xác định?]()
8. [MIME type multipart/form-data được dùng trong trường hợp nào và tại sao?]()
9. [Giải thích khi nào và tại sao dùng multipart/byteranges?]()
10. [MIME sniffing là gì và tại sao nó đôi khi là vấn đề bảo mật?]()

## Compression in HTTP

1. HTTP compression là gì và tại sao nó quan trọng đối với hiệu năng website?
2. Compression có thể giảm băng thông bao nhiêu phần trăm đối với tài liệu web điển hình?
3. Web developers cần tự _thiết kế_ cơ chế nén hay server và browser đã hỗ trợ sẵn? Vì sao?
4. Compression có thể diễn ra ở những “cấp độ” nào trong HTTP? Hãy giải thích từng cấp độ.
5. Điểm khác biệt chính giữa _file format compression_ và _HTTP end-to-end compression_ là gì?
6. Lossless và lossy compression khác nhau thế nào? Cho ví dụ trong bối cảnh web.
7. End-to-end HTTP compression hoạt động như thế nào?
8. Header nào client gửi để cho server biết các thuật toán compression mà nó hỗ trợ?
9. Header nào server dùng để cho client biết thuật toán đã được chọn?
10. Tại sao server nên gửi thêm header `Vary: Accept-Encoding` khi sử dụng compression?
11. Hai thuật toán compression phổ biến hiện nay trong HTTP là gì? So sánh ngắn gọn ưu-nhược.
12. Hop-by-hop compression khác gì so với end-to-end compression?
13. Header nào được dùng trong hop-by-hop compression để thương lượng thuật toán giữa các node trung gian?
14. Tại sao hop-by-hop compression ít được sử dụng trong thực tế?
15. Bạn nên _bật HTTP compression_ cho loại tài nguyên nào và _không nên_ bật cho loại nào? Vì sao?
16. Nếu site bạn có HTML, CSS, JS không load nhanh, bạn sẽ kiểm tra cấu hình compression ở đâu và như thế nào?
17. Thuật toán gzip và Brotli tương thích với các trình duyệt hiện đại như thế nào? Bạn có phải lo về fallback không?

## HTTP caching

1. HTTP caching là gì và mục tiêu chính của nó trong giao tiếp HTTP?
2. Cache giúp giảm tải server và tăng tốc độ tải như thế nào?
3. Phân biệt cache _private_ và _shared_ trong HTTP caching. Khi nào dùng mỗi loại?
4. Khái niệm “fresh” và “stale” trong cache là gì? Cache sử dụng tiêu chí nào để xác định chúng?
5. Header `Cache-Control: max-age` hoạt động như thế nào để xác định thời gian cache được coi là fresh?
6. Sự khác nhau giữa `Expires` và `max-age` là gì? Khi nào `max-age` được ưu tiên?
7. Cache validation là gì? Nó hoạt động ra sao trong HTTP?
8. Hai header HTTP nào thường được dùng để gửi conditional request và mục đích của chúng?
9. Khi nào server trả `304 Not Modified` và lợi ích của trả mã này là gì?
10. `Cache-Control: no-cache` khác gì với `no-store`? Khi nào bạn dùng mỗi cái?
11. Tại sao server nên thêm `Vary` header khi trả tài nguyên cacheable? Cho ví dụ `Vary` thường gặp.
12. Giải thích khi nào nên sử dụng `private`, `public`, và `immutable` trong `Cache-Control`.
13. Heuristic caching là gì và tại sao specification đề nghị luôn dùng `Cache-Control` rõ ràng?
14. Cache busting là gì? Vì sao lại cần cache busting trong thiết kế front-end?
15. Tại sao HTML (main resource) thường _khó_ cache hơn so với các subresources như CSS/JS?
16. Nếu bạn deploy 1 trang web nhưng thay đổi CSS/JS mà browser vẫn dùng bản cũ, các cách khắc phục liên quan cache là gì?
17. Khi client và shared cache cùng nhận 2 yêu cầu giống nhau cùng lúc, hiện tượng gì có thể xảy ra, và tại sao?
18. Làm sao bạn xử lý cache cho API JSON để vừa tối ưu hiệu năng vừa đảm bảo dữ liệu không lạc hậu?
19. Ưu-nhược của việc cache resources _rất lâu_ với `immutable` và cache busting so với caching thông thường là gì?
20. Những giới hạn của HTTP cache khi nội dung được cá nhân hóa theo người dùng, và bạn giải quyết như thế nào?
21. Cache dành cho SPA/API có khác so với caching tài nguyên tĩnh truyền thống không? Nêu khác biệt chính.

## HTTP authentication

1. HTTP authentication framework là gì và được định nghĩa trong RFC nào?
2. Mô tả trình tự cơ bản của một HTTP authentication challenge và response.
3. HTTP status code nào được dùng để yêu cầu xác thực tài nguyên và code nào dùng cho xác thực proxy?
4. Khi nào server nên phản hồi HTTP 403 Forbidden thay vì 401 Unauthorized?
5. Header `WWW-Authenticate` dùng để làm gì trong HTTP authentication?
6. Phân biệt `WWW-Authenticate` và `Proxy-Authenticate`.
7. Header `Authorization` chứa những gì và ở đâu trong request?
8. Header `Proxy-Authorization` dùng để làm gì?
9. HTTP Basic authentication là gì? Nêu cách hoạt động và cách credentials được truyền.
10. Tại sao Basic authentication không an toàn nếu không dùng HTTPS?
11. Kể tên vài scheme authentication khác ngoài Basic trong HTTP framework (Bearer, Digest, v.v.)
12. Bearer authentication dùng cho trường hợp gì và thường liên quan tới protocol nào?
13. Khi dùng Basic authentication để bảo vệ tài nguyên, server gửi gì để yêu cầu client gửi credentials?
14. Tại sao không nên gửi credential qua URL như `https://user:pass@host/…` trong các trình duyệt hiện đại?
15. Các authentication schemes khác nhau có ưu-nhược gì về mặt bảo mật và hỗ trợ?
16. Giải thích tại sao Basic Auth dễ bị CSRF nếu dùng không đúng cách.
17. Nếu server trả 401 và đôi khi trả 404 để _ẩn tài nguyên_, lý do là gì?
18. Trong một API REST, khi nào bạn sẽ chọn Bearer token thay vì Basic Auth?
19. Làm thế nào để xử lý xác thực khi có proxy giữa client và origin server? Nhắc tới các header cụ thể.
20. Bạn sẽ làm gì nếu client gửi sai credentials liên tục? Server nên trả gì và vì sao?

## Using HTTP cookies

1. HTTP cookie là gì và vì sao cookie cần thiết trong HTTP?
2. Cookies thường được dùng cho những mục đích nào trong ứng dụng web?
3. Cookies được gửi từ server tới client và ngược lại qua header nào?
4. Phân biệt _session cookies_ và _persistent cookies_. Cookie nào bị xóa khi nào?
5. Thuộc tính `Expires` và `Max-Age` khác nhau thế nào? Khi nào `Max-Age` được ưu tiên?
6. Làm thế nào để xóa một cookie ngay lập tức từ phía client/server?
7. Thuộc tính `Secure` là gì và nó ảnh hưởng như thế nào tới cookie?
8. Thuộc tính `HttpOnly` là gì và lợi ích bảo mật của nó ra sao?
9. Thuộc tính `Domain` và `Path` tác động tới cookie như thế nào?
10. Thuộc tính `SameSite` có các giá trị gì và mỗi giá trị kiểm soát cookie gửi trong trường hợp nào?
11. Điều gì xảy ra nếu cookie có `SameSite=None` nhưng thiếu thuộc tính `Secure`?
12. Cookie prefixes (như `__Secure-`, `__Host-`) là gì và chúng mang lại lợi ích gì về bảo mật?
13. Hãy nêu yêu cầu để một cookie có tiền tố `__Host-` hợp lệ.
14. Các cách tạo, truy cập và cập nhật cookie trong trình duyệt bằng JavaScript là gì? Và khi nào không thể dùng JavaScript để truy cập?
15. Cookies và các API lưu trữ khác như `localStorage`, `sessionStorage` khác nhau như thế nào?
16. Cookies có thể bị lợi dụng bởi tấn công nào (ví dụ XSS, session hijacking) và các biện pháp giảm thiểu ra sao?
17. Tại sao không nên lưu trữ thông tin nhạy cảm trực tiếp trong cookie?
18. Cookies có thể bị gửi tới các domain nào? Làm thế nào để kiểm soát việc này?
19. Cookies bên thứ ba (third-party cookies) là gì và chúng khác cookies cùng nguồn như thế nào?
20. Việc chặn cookies bên thứ ba có thể ảnh hưởng gì tới chức năng trang web?
21. Cookies ảnh hưởng gì tới quyền riêng tư và tracking trên web?
22. Những quy định pháp lý (như GDPR, CCPA) ảnh hưởng tới việc sử dụng cookie như thế nào?
23. Tại sao các trang web thường hiển thị banner cookie và yêu cầu người dùng đồng ý?
24. Khi bạn deploy website và người dùng phàn nàn cookie không gửi qua HTTPS, bạn sẽ kiểm tra điều gì?
25. Nêu cách server xử lý session ID bằng cookie để duy trì phiên đăng nhập.
26. Nếu một cookie không được gửi với yêu cầu từ iframe bên thứ ba, giải thích nguyên nhân liên quan tới `SameSite`.

## Redirections in HTTP

1. HTTP redirect là gì và HTTP redirect được xác định như thế nào trong giao thức?
2. HTTP redirect server gửi gì để client thực hiện chuyển hướng? Header và status code nào liên quan?
3. Phân biệt redirect _permanent_ và _temporary_ trong HTTP; server và crawler xử lý chúng như thế nào?
4. Status code `301` và `308` khác nhau thế nào về cách xử lý method HTTP và mục đích sử dụng?
5. Status code `302`, `303`, và `307` có điểm khác biệt gì về cách method và body được xử lý?
6. Có status code nào dùng cho _redirection đặc biệt_ như dùng cho cache hoặc lựa chọn nhiều URL không? Nêu chi tiết.
7. Trong trường hợp redirect sau một POST/PUT để tránh gửi lại request khi reload trang, nên dùng code nào và vì sao?
8. Những trường hợp thực tế bạn thường phải dùng HTTP redirect trong web app hoặc trang web là gì?
9. Tại sao việc sử dụng redirect quá nhiều có thể ảnh hưởng đến hiệu năng?
10. Bạn có thể cấu hình redirect ở server Apache như thế nào (ví dụ dùng `Redirect`, `RedirectMatch`)?
11. Một số cách để cấu hình redirect trên Nginx là gì?
12. Trong IIS, bạn thiết lập redirect bằng cách sử dụng gì?
13. Redirection loop là gì, và tại sao nó gây lỗi cho người dùng?
14. Server và trình duyệt phát hiện vòng lặp redirect như thế nào và kết quả có thể là gì?
15. Ngoài redirect HTTP, còn cách nào để redirect trang từ phía client không? Sử dụng công nghệ gì?
16. Trong trường hợp cả HTTP redirect, HTML redirect và JavaScript redirect cùng tồn tại trên trang, thứ tự ưu tiên như thế nào?

## HTTP conditional requests

1. HTTP conditional request là gì và tại sao HTTP lại cần khái niệm này?
2. Conditional request khác gì với request bình thường? Conditional headers đóng vai trò gì?
3. Trong bối cảnh HTTP caching, conditional request hoạt động như thế nào để tiết kiệm băng thông?
4. Validators trong HTTP là gì? Phân biệt `ETag` và `Last-Modified`.
5. Strong validation và weak validation khác nhau như thế nào trong HTTP conditional requests?
6. Giải thích header `If-Match` và kịch bản nào bạn sẽ dùng nó.
7. Header `If-None-Match` hoạt động ra sao? Nó thường được dùng với status code nào?
8. Header `If-Modified-Since` và `If-Unmodified-Since` kiểm tra gì và trong trường hợp nào nên dùng?
9. Header `If-Range` dùng để làm gì trong việc resume partial download?
10. Nếu tài nguyên không thay đổi trong conditional request, server phản hồi status code nào và vì sao?
11. Khi sử dụng `If-Match` và điều kiện thất bại, server sẽ trả gì? (status code).
12. Conditional requests giúp hỗ trợ cache update như thế nào trong vòng đời cache?
13. Giải thích cách HTTP resume một partial download và vai trò của conditional request trong đó.
14. Trong ứng dụng web có nhiều client cùng sửa tài nguyên, conditional requests giúp tránh lost update (optimistic locking) ra sao?
15. Giải thích cách dùng `If-None-Match: "*"` để đảm bảo tài nguyên chỉ được tạo nếu chưa tồn tại.
16. Trong conditional requests, ai là người tạo header (client hay server) và trong trường hợp nào?
17. Một server cần cấu hình gì để hỗ trợ conditional requests (ví dụ: ETag, Last-Modified)?
18. Nếu server không hỗ trợ HTTP/1.1 và bạn muốn dùng `If-None-Match`, bạn sẽ kiểm tra server như thế nào?
19. Khi nào bạn sẽ dùng `If-None-Match` thay vì `If-Modified-Since` trong conditional requests?
20. Trong API REST, làm sao kiểm tra tài nguyên mới trước khi cập nhật để tránh ghi đè? Bạn sẽ dùng conditional request thế nào?

## HTTP range requests

1. HTTP range request là gì và nó được dùng để làm gì?
2. Range requests hữu ích cho những ứng dụng nào? Nêu vài ví dụ.
3. Làm thế nào client biết server có hỗ trợ range requests hay không? Header nào được dùng?
4. Tại sao giá trị `none` trong `Accept-Ranges` có ý nghĩa quan trọng?
5. Header `Range` được sử dụng như thế nào để yêu cầu một phạm vi byte? Viết ví dụ cú pháp.
6. Range requests có thể yêu cầu nhiều đoạn của tài nguyên cùng lúc không? Nếu có, client sắp xếp cú pháp ra sao?
7. Trong `Range`, có thể chỉ định suffix range không? Ví dụ cách chỉ định byte cuối.
8. Server trả status code nào khi trả thành công một partial response?
9. Nếu range request vượt “out of bounds” (không hợp lệ), server trả status code gì?
10. Nếu server không hỗ trợ range requests, server phản hồi như thế nào?
11. Khi server gửi partial response, header nào chỉ rõ khoảng byte đang được trả và tổng kích thước file?
12. HTTP range request có thể trả về _multipart/byteranges_. Khi nào điều này xảy ra?
13. Trong response multipart, làm thế nào để phân biệt từng phần nội dung?
14. Header `If-Range` dùng để làm gì trong range requests?
15. Header `If-Range` có thể kết hợp với validator nào để kiểm tra tài nguyên?
16. HTTP range requests khác gì so với chunked `Transfer-Encoding`?
17. Range requests có tương thích với chunked transfer không?
18. Bạn đang thiết kế tính năng resume download: bạn sẽ kiểm tra và xử lý range request như thế nào?
19. Nếu client gửi range request nhưng server trả toàn bộ tài nguyên, bạn có thể làm gì ở phía client để xử lý?
20. Trong streaming media (audio/video), database hoặc file lớn, range requests có lợi thế gì so với tải nguyên bình thường?

## HTTP Client hints

1. Client Hints là gì và mục đích chính của nó trong giao thức HTTP?
2. Một server phải làm gì để bắt đầu nhận client hints từ trình duyệt? Header nào được sử dụng?
3. Client sử dụng client hints trong các request tiếp theo dựa trên điều kiện nào?
4. Client hints có thể được khai báo qua HTML thay vì HTTP response header không? Nếu có, làm thế nào?
5. Tại sao khi sử dụng client hints, server nên thêm các hint vào header `Vary`?
6. Việc thêm các client hints thay đổi thường xuyên như `Downlink` vào `Vary` có ảnh hưởng gì tới cache?
7. Client hints phân thành _low entropy_ và _high entropy_ là gì? Lý do phân loại này?
8. Kể ví dụ vài _low entropy hint_ và giải thích vì sao chúng an toàn hơn.
9. High entropy hints khác low entropy ở điểm nào và khi nào chúng được gửi?
10. Critical client hint là gì và làm thế nào để server yêu cầu chúng một cách bắt buộc?
11. Trình duyệt xử lý ra sao nếu một critical client hint được yêu cầu nhưng chưa gửi trong request ban đầu?
12. User agent client hints cung cấp thông tin gì và mục đích sử dụng ra sao?
13. User preference media features client hints gồm loại nào và dùng để điều chỉnh gì?
14. Device client hints và network client hints thường dùng để tối ưu nội dung nào?
15. Client hints được xem là “privacy-preserving” hơn User-Agent header như thế nào?
16. Những rủi ro về quyền riêng tư liên quan tới client hints là gì và tại sao cần cân nhắc?
17. Nếu bạn muốn tối ưu ảnh dựa trên kích thước màn hình của client, bạn sẽ dùng client hints nào và server cần cấu hình gì?
18. Khi một tài nguyên cacheable nhưng phụ thuộc vào giá trị client hint, header nào bạn bắt buộc phải khai báo trong `Vary`?

## User-Agent reduction

1. User-Agent reduction là gì và tại sao các trình duyệt áp dụng nó?
2. User-Agent string thường chứa gì và thông tin nào bị giảm sau khi áp dụng User-Agent reduction?
3. Tại sao việc dựa vào User-Agent để phát hiện trình duyệt bị xem là không đáng tin cậy?
4. Việc giảm UA ảnh hưởng tới các kỹ thuật client-side như feature detection và progressive enhancement như thế nào?
5. Trong những trường hợp nào ứng dụng web vẫn cần thông tin chi tiết tương đương UA?
6. Làm thế nào server có thể nhận lại thông tin chi tiết hơn về UA nếu cần?
7. So sánh giữa User-Agent reduction và User-Agent client hints về quyền riêng tư và cách tiếp cận.
8. Làm thế nào để truy cập các client hint về UA trong JavaScript? Property hoặc API nào được dùng?
9. Tại sao việc truy cập high-entropy client hints cần phương thức khác so với low-entropy?
10. User-Agent reduction nhằm giải quyết vấn đề privacy nào?
11. Khi giảm UA, các phần tử như _minor browser version_ được thể hiện thế nào?

## Compression Dictionary Transport

1. Compression Dictionary Transport là gì và giải pháp này nhằm mục đích gì trong HTTP?
2. Điểm khác biệt chính giữa compression bình thường (như gzip/br hoặc zstd mặc định) và Compression Dictionary Transport là gì?
3. Tại sao SDCH (Shared Dictionary Compression for HTTP) trước đây bị loại bỏ và Compression Dictionary Transport được coi là cải tiến?
4. Compression dictionary là gì và nội dung của dictionary có định dạng cụ thể hay MIME type riêng không?
5. Giải thích _delta compression_ trong bối cảnh sử dụng dictionary để nén tài nguyên liên quan đến version update (ví dụ `app.v1.js` → `app.v2.js`).
6. Header `Use-As-Dictionary` dùng để làm gì và server gửi nó trong response khi nào?
7. Trong request, header nào client gửi để báo server biết client có dictionary nào sẵn?
8. Giải thích cách `Accept-Encoding` mở rộng với giá trị như `dcb` và `dcz` trong context Compression Dictionary Transport.
9. Header `Dictionary-ID` dùng để làm gì và khi nào nó được sử dụng?
10. Khi server trả dictionary compressed response, header nào phải có để phản hồi đúng phương thức nén?
11. Ngoài dùng resource đã tải như dictionary, bạn có thể cung cấp dictionary như một tài nguyên riêng bằng cách nào?
12. Khi cung cấp dictionary như một resource riêng, cái gì cần được đảm bảo cho tài nguyên dictionary?
13. Bạn có thể tạo dictionary-compressed resources trước ở build time hoặc runtime. Ưu-nhược của hai cách này là gì?
14. Compression Dictionary Transport hỗ trợ những thuật toán nén nào?
15. Compression dictionary transport có hạn chế gì về _same-origin_ và _CORS_?
16. Tại sao dictionary có thể trở thành _tracking vector_ và điều gì có thể giới hạn công nghệ này trong trình duyệt?
17. Compression Dictionary Transport hiện có specification rõ ràng trong tiêu chuẩn HTTP/IETF không?

## Network Error Logging (NEL)

1. Network Error Logging (NEL) là gì và mục đích của nó trong HTTP?
2. NEL được kích hoạt bằng cách sử dụng header nào trong HTTP response?
3. Tại sao NEL yêu cầu một origin được trình duyệt coi là “an toàn”?
4. Các trường chính trong đối tượng JSON của header `NEL` là gì và ý nghĩa của chúng?
5. Ý nghĩa của `success_fraction` và `failure_fraction` trong NEL là gì?
6. Tại sao cần chỉ định `report_to` trong NEL? Header này tương tác với tính năng nào?
7. Tham số `include_subdomains` ảnh hưởng như thế nào tới chính sách NEL?
8. Một báo cáo lỗi mạng gửi bởi trình duyệt thông qua NEL gồm những thông tin gì?
9. Các “phase” trong báo cáo lỗi NEL có ý nghĩa gì? Nêu vài ví dụ.
10. Tại sao `status_code` là 0 trong một số báo cáo lỗi? Đó là trường hợp gì?
11. Kể vài loại lỗi mạng được nhận dạng trong NEL và ý nghĩa của chúng.
12. Trong NEL, lỗi `tcp.reset` biểu thị điều gì? Và lỗi này khác gì với `tcp.refused`?
13. Lỗi `http.error` trong NEL báo điều gì về request?
14. NEL hoạt động như thế nào cùng với Reporting API để gửi báo cáo lỗi?
15. Report endpoint được định nghĩa trong `Report-To` phải đáp ứng những yêu cầu gì?
16. Nếu bạn muốn NEL báo cáo 50% lỗi thành công và 100% lỗi thất bại, cấu hình NEL JSON sẽ như thế nào?
17. Bạn sẽ cấu hình `max_age` như thế nào nếu muốn chính sách NEL tồn tại trong một năm?
18. Tại sao NEL được coi là experimental và cần kiểm tra browser compatibility trước khi dùng?

## Content negotiation

1. Content negotiation trong HTTP là gì và mục đích của nó?
2. “Representation” và “resource” khác nhau như thế nào trong bối cảnh content negotiation?
3. Server-driven content negotiation hoạt động như thế nào? Client gửi gì và server xử lý ra sao?
4. Agent-driven (reactive) negotiation khác gì so với server-driven? Trình tự ra sao?
5. HTTP status code nào có thể xuất hiện trong agent-driven negotiation để báo lỗi hoặc lựa chọn multiple choices?
6. Header `Accept` dùng để làm gì trong content negotiation? Cho ví dụ một giá trị điển hình.
7. Header `Accept-Encoding` ảnh hưởng thế nào tới negotiation?
8. Header `Accept-Language` cũng được dùng trong negotiation. Cách thức hoạt động và các rủi ro khi dùng giá trị này để tự động chọn ngôn ngữ cho người dùng?
9. Header `User-Agent` có được liệt kê trong chuẩn content negotiation không? Tại sao server không nên dựa vào nó để chọn representation?
10. Header `Vary` phản hồi gì từ server và tại sao nó quan trọng trong content negotiation?
11. Chất lượng (q-factor) trong các `Accept*` headers là gì và ảnh hưởng thế nào tới server chọn representation?
12. Trong một header `Accept: text/html;q=0.9, application/json;q=0.8`, server nên ưu tiên gì và vì sao?
13. Nêu vài nhược điểm của server-driven content negotiation được mô tả trong tài liệu.
14. Tại sao content negotiation có thể làm giảm hiệu suất cache?
15. Trong xây dựng API (REST), bạn sẽ dùng content negotiation để chọn định dạng trả về (JSON vs XML) như thế nào?
16. Nếu server không thể tìm representation phù hợp dựa trên các `Accept` headers, server nên trả status code nào?
17. Tại sao MIME type negotiation khó mở rộng với các thuộc tính mới như kích thước màn hình hoặc thiết bị?
18. Giải thích cách client hints (như `Accept-CH`) có thể mở rộng content negotiation và ví dụ một vài hint có thể dùng.
19. Trong bối cảnh content negotiation, làm sao server nên xử lý caching khi tham số `Vary` có wildcard (`*`)?

## Browser detection using the user agent string (UA sniffing)

1. User-Agent HTTP header là gì và nó chứa những thông tin gì về trình duyệt?
2. Làm thế nào bạn có thể truy xuất user agent string trong JavaScript?
3. Tại sao việc dùng user agent string để _detect_ browser thường gây lỗi và không nên dùng? Nêu vài lý do.
4. UA sniffing có “brittle” (dễ vỡ) không? Vì sao?
5. Phần nào trong UA string khiến việc xác định browser _version_ và _name_ trở nên không đáng tin cậy?
6. Tại sao _feature detection_ thường được khuyến nghị hơn _browser detection_?
7. Cho ví dụ kiểm tra support một API bằng feature detection trong JavaScript.
8. Media queries hoặc API nào khác có thể dùng thay cho UA sniffing để tối ưu layout cho mobile?
9. Client hints có thể thay thế UA sniffing như thế nào trong HTTP context?
10. Trong UA string, token nào thường biểu thị rendering engine như Blink, Gecko hay WebKit?
11. Làm thế nào để phân biệt Safari với Chrome trong UA sniffing? Điều gì gây sai lệch?
12. Có nên dùng UA sniffing để xác định _mobile vs desktop_? Vì sao/ vì sao không?
13. Nêu vài lý do _invalid_ (không nên dùng) để thực hiện browser detection bằng UA.
14. Trong trường hợp hiếm bạn buộc phải dùng UA sniffing, bạn sẽ làm gì để giảm lỗi?
15. Trình duyệt có thể giả mạo UA như thế nào và vì sao điều này làm browser detection không đáng tin?

## Connection management in HTTP/1.x

1. Khi nói tới “connection management” trong HTTP/1.x, chúng ta đang nói tới điều gì và tại sao nó quan trọng?
2. HTTP/1.x thường dùng giao thức vận chuyển nào để mở kết nối? Nhấn mạnh đặc tính hop-by-hop của connection management.
3. Mô tả model “short-lived connections” trong HTTP/1.x và những hạn chế chính của nó.
4. Trong HTTP/1.0 model ngắn hạn là mặc định. Điều gì khiến model này không hiệu quả với các trang hiện đại?
5. Persistent connection (keep-alive) trong HTTP/1.x là gì và ưu điểm của nó so với connection ngắn?
6. HTTP/1.0 và HTTP/1.1 khác nhau như thế nào về cách cấu hình persistent connection?
7. Persistent connections có nhược điểm gì? Khi nào việc _không_ giữ kết nối mở lại là tốt hơn?
8. Header nào thường dùng để cấu hình thời gian keep-alive?
9. HTTP pipelining là gì trong HTTP/1.x và mục đích của nó?
10. Tại sao HTTP pipelining không được kích hoạt mặc định trong hầu hết trình duyệt hiện đại?
11. HTTP pipelining chỉ an toàn khi dùng với các HTTP methods nào? Vì sao?
12. HTTP pipelining đã bị _superceded_ (thay thế) bởi cơ chế nào trong HTTP/2?
13. Domain sharding là gì và nó được sử dụng như thế nào trong HTTP/1.x để cải thiện hiệu năng?
14. Tại sao domain sharding không còn được khuyến nghị khi sử dụng HTTP/2?
15. Việc mở quá nhiều kết nối song song tới cùng một domain có thể gây ra vấn đề gì?
16. Bạn đang tối ưu hiệu năng một web app dùng HTTP/1.1. Bạn sẽ ưu tiên dùng persistent connections hay non-persistent? Vì sao?
17. Nếu bạn thấy một client luôn mở từng kết nối cho mỗi request (mặc dù HTTP/1.1 hỗ trợ persistent), bạn nghi ngờ vấn đề gì và cách khắc phục?
18. Trong mô hình có proxy, làm thế nào connection management giữa client–proxy và proxy–server có thể khác nhau?

## Protocol upgrade mechanism

1. Cơ chế “protocol upgrade” trong HTTP là gì và nó dùng để làm gì?
2. Cơ chế nâng cấp giao thức này thuộc phiên bản HTTP nào và có được hỗ trợ trong HTTP/2 không?
3. Ai luôn là người khởi xướng quá trình nâng cấp giao thức? Có ngoại lệ nào không?
4. Header nào client phải gửi để yêu cầu nâng cấp giao thức? Tại sao cần nhiều hơn một header?
5. Khi server đồng ý nâng cấp, server sẽ phản hồi với status code gì và kèm theo header nào?
6. Trường hợp sử dụng phổ biến nhất của cơ chế nâng cấp giao thức là gì?
7. Khi nâng cấp sang WebSocket, ngoài `Upgrade` và `Connection`, có những header nào khác thường xuất hiện? (Hint liên quan WebSocket handshake)
8. WebSocket API của trình duyệt hỗ trợ nâng cấp giao thức như thế nào cho lập trình viên?
9. Có thể dùng cơ chế upgrade để chuyển một kết nối HTTP/1.1 sang HTTP/2? Nếu có, hạn chế là gì?
10. Cách dùng cơ chế nâng cấp để bắt đầu kết nối bảo mật (HTTPS) như thế nào?
11. Server có thể yêu cầu client upgrade lên TLS? Nếu có, server dùng status code nào?
12. Nếu server không hỗ trợ hoặc từ chối nâng cấp giao thức, server sẽ phản hồi như thế nào?
13. Sau khi gửi `101 Switching Protocols`, điều gì xảy ra với kết nối hiện tại?
14. Trong quá trình nâng cấp sang WebSocket, header `Sec-WebSocket-Key` và `Sec-WebSocket-Accept` có vai trò gì?
15. Giải thích tại sao HTTP/2 không hỗ trợ “protocol upgrade” trong cùng kết nối như HTTP/1.1.
16. Khi viết server thủ công (low-level), điều gì cần lưu ý khi xử lý Upgrade từ HTTP/1.1 sang các giao thức khác?

## Proxy servers and tunneling

1. Proxy server là gì và nó hoạt động như thế nào trong bối cảnh HTTP?
2. Phân biệt forward proxy và reverse proxy. Vai trò chính của từng loại là gì?
3. Trong một hệ thống có forward proxy, proxy có thể giúp gì cho việc ẩn danh và kiểm soát băng thông?
4. Reverse proxy thường dùng để làm gì trong các hệ thống backend?
5. Tại sao forwarding client information qua proxy lại quan trọng và các trường hợp nó bị mất?
6. Header chuẩn để forward thông tin client qua proxy là gì và vì sao chúng hữu ích?
7. Các phiên bản không chuẩn của header forward client thường thấy là gì?
8. Header nào được dùng để cung cấp thông tin về proxy trên đường truyền (không phải client)?
9. HTTP tunneling là gì và vì sao nó cần thiết khi làm việc với proxy?
10. Header hoặc method HTTP nào được dùng để mở một tunnel qua proxy? Mục đích chính của nó là gì?
11. Tại sao không phải tất cả proxy servers đều hỗ trợ method `CONNECT`, và chúng có thể hạn chế nó như thế nào?
12. Mô tả luồng hoạt động cơ bản khi một client sử dụng HTTP proxy để kết nối tới một server HTTPS.
13. Proxy Auto-Configuration (PAC) là gì và giúp ích gì cho việc điều phối request qua proxy?
14. File PAC có định dạng gì và yêu cầu MIME type nào để trình duyệt hiểu?
15. Hàm tiêu chuẩn trong PAC file là gì và nhiệm vụ của nó?
16. Khi nào bạn nên dùng reverse proxy thay vì forward proxy trong kiến trúc hệ thống backend?
17. Nếu bạn thấy một request tới server xuất hiện IP của proxy thay vì IP client, bạn sẽ làm gì để lấy lại IP gốc?
18. Khi sử dụng proxy trong ứng dụng web, những rủi ro bảo mật nào cần lưu ý?

## Practical security implementation guides

1. Mục đích chính của các practical security implementation guides là gì?
2. Tại sao không thể chỉ dựa vào một bộ hướng dẫn để bảo mật hoàn toàn một website?
3. HTTP Observatory là gì và guide này liên quan tới công cụ đó như thế nào?
4. Tại sao TLS (HTTPS) lại là bắt buộc cho các trang web hiện đại?
5. Kể tên ít nhất ba best practices liên quan tới TLS/HTTPS từ practical guides.
6. HSTS là gì và vì sao nó nên được bật cho tất cả các trang ?
7. Clickjacking là gì và làm thế nào practical guides gợi ý để ngăn chặn nó?
8. Cross-site request forgery (CSRF) là gì? Những kỹ thuật nào được khuyến nghị để chống CSRF?
9. Secure cookie configuration gồm những gì và vì sao lại quan trọng?
10. CORP (Cross-Origin Resource Policy) dùng để làm gì và mitigates loại tấn công nào?
11. Vì sao MIME type verification lại được xem là quan trọng dù mức độ ảnh hưởng thấp?
12. Content Security Policy (CSP) là gì và nó giúp ngăn chặn kiểu tấn công nào?
13. CORS nên được cấu hình như thế nào để cân bằng giữa bảo mật và tính năng?
14. Referrer Policy giúp gì cho quyền riêng tư người dùng và bảo mật?
15. Subresource Integrity (SRI) là gì và dùng trong trường hợp nào?
16. Tại sao form autocompletion đôi khi nên được tắt và khi nào nên làm điều đó?
17. Liệt kê ít nhất hai vấn đề bảo mật đối với dữ liệu người dùng nhập từ web form ngoài CSRF.
18. Theo tài liệu, nên triển khai cái gì trước khi cái gì trong danh sách guide? Giải thích lý do.
19. Có guide nào được xem là “Required”? Hãy nêu ví dụ và giải thích vì sao.
20. Guide nào có impact “Maximum” và tại sao?
21. Tài liệu nào khác ngoài MDN bạn nên biết để tăng thêm kiến thức bảo mật theo best practices?

## Permissions Policy

1. Permissions Policy là gì và mục đích chính của nó trong HTTP?
2. Permissions Policy khác gì so với Content Security Policy (CSP)?
3. Tên cũ của Permissions Policy là gì và tại sao cần chú ý khi dùng?
4. Cú pháp cơ bản của header `Permissions-Policy` như thế nào? Hãy viết ví dụ.
5. Allowlist trong Permissions Policy là gì và có những giá trị nào?
6. Giải thích ý nghĩa của mỗi giá trị allowlist: `*`, `()`, `self` và `src`.
7. Có thể dùng wildcards trong allowlist không? Ví dụ với subdomain.
8. Trong bối cảnh `<iframe>`, header Permissions Policy và attribute `allow` khác nhau ở điểm nào?
9. Quy tắc kế thừa chính sách giữa trang cha và `<iframe>` như thế nào?
10. Tại sao khi iframe điều hướng tới origin khác, việc khai báo allow origin trong `allow` attribute lại quan trọng?
11. Nếu một tính năng bị vô hiệu hoá ở parent frame, liệu child frame có thể tự bật lại nó không? Vì sao?
12. Mối quan hệ giữa Permissions Policy và Permissions API là gì?
13. Nếu Permissions Policy chặn một tính năng mạnh (như geolocation), thì Permissions API trả gì khi query trạng thái?
14. Bạn muốn vô hiệu hoá tất cả origin sử dụng camera trên trang. Viết header Permissions Policy phù hợp.
15. Bạn muốn chỉ cho phép geolocation trên `self` và một số domain tin cậy. Viết header hoặc `<iframe>` `allow` phù hợp.
16. Nếu bạn cần dùng nhiều tính năng cùng lúc (ví dụ camera và fullscreen), header Permissions Policy sẽ viết như thế nào?
17. Vì sao nên thiết lập Permissions Policy cẩn thận khi dùng third-party content như iframe?
18. Permissions Policy có tính backward-compatible như các header khác không?
19. Việc khai báo Permissions Policy có thể ảnh hưởng tới trải nghiệm người dùng hoặc tính năng web như thế nào khi quá hạn chế?

## Cross-Origin Resource Policy (CORP)

1. Cross-Origin Resource Policy là gì và nó giải quyết vấn đề gì trong bảo mật web?
2. CORP được kích hoạt bởi header HTTP nào?
3. Chính sách CORP có chặn _request_ thực tế hay không? Tại sao?
4. Danh sách ba giá trị có thể dùng với header `Cross-Origin-Resource-Policy`, và mỗi giá trị khác nhau như thế nào?
5. Giải thích sự khác nhau giữa _same-site_ và _same-origin_ trong CORP.
6. Trong trường hợp nào bạn nên dùng giá trị `cross-origin`?
7. CORP chỉ _hiệu lực_ đối với loại request nào?
8. Trình duyệt xử lý response thế nào nếu yêu cầu cross-origin _no-cors_ vi phạm CORP?
9. Sự khác nhau giữa CORP và CORS là gì?
10. CORP liên quan thế nào đến Cross-Origin Embedder Policy (COEP)?
11. Nếu không sử dụng CORS hoặc CORP, trình duyệt dùng gì theo mặc định để quyết định có cho đọc response không?
12. Viết ví dụ header `Cross-Origin-Resource-Policy` để chỉ cho phép tài nguyên đọc được nếu request từ cùng origin.
13. Bạn triển khai một API công khai nhưng muốn người khác _fetch_ dữ liệu qua `fetch()` (CORS), liệu CORP có cần thiết không? Tại sao?
14. Một số lỗi liên quan đến CORP có thể xảy ra khi dịch vụ tải PDF bị hỏng — nguyên nhân có thể liên quan gì?
15. CORP có yêu cầu MIME type specific để hoạt động không?
16. Nếu một tài nguyên được nhúng trong trang khác và hiển thị nhưng bạn không muốn _no-cors_ requests đọc nội dung — bạn sẽ cấu hình header như thế nào?

## IFrame credentialless

1. IFrame credentialless là gì và vì sao cơ chế này được giới thiệu?
2. Vấn đề của Cross-Origin-Embedder-Policy (COEP) truyền thống khi nhúng cross-origin content là gì?
3. Lợi ích chính của việc sử dụng iframe credentialless là gì trong môi trường COEP?
4. Thuộc tính `credentialless` của `<iframe>` hoạt động thế nào và có thể dùng ở đâu?
5. Nếu tài liệu tải trong một credentialless iframe muốn kiểm tra xem nó đang trong context credentialless, property nào dùng được?
6. Context “credentialless” không có quyền truy cập những gì?
7. Cookie và storage trong credentialless iframe khác gì so với trong một iframe thông thường?
8. Nonce (số dùng một lần) trong context credentialless dùng để làm gì?
9. Credentialless iframe ảnh hưởng gì tới các popup mà iframe mở ra (ví dụ OAuth)?
10. Chrome hay trình duyệt khác có bật hỗ trợ iframe credentialless theo mặc định không?
11. Credentialless iframe ảnh hưởng tới chức năng tự động điền mật khẩu (password auto-fill) như thế nào?
12. Nếu một credentialless iframe chứa các iframe con, chính sách credentialless có kế thừa xuống không? Tại sao?

## Cross-Origin Resource Sharing (CORS)

1. CORS là gì và tại sao trình duyệt cần cơ chế này?
2. Bạn hãy giải thích _same-origin policy_ và vì sao CORS được đưa ra để _bổ sung_ nó?
3. CORS hoạt động trong ngữ cảnh của API fetch/XHR như thế nào?
4. Phân biệt _simple requests_ và _preflight requests_ trong CORS. Khi nào trình duyệt gửi preflight?
5. Điều kiện nào khiến request được coi là _simple_ theo CORS? (Methods, headers, Content-Type)
6. Header nào trình duyệt gửi trong _preflight_ để thông báo method và headers dự kiến dùng?
7. `Access-Control-Allow-Origin` dùng để làm gì và server trả giá trị nào cho phép mọi origin?
8. Khi nào server _không_ nên dùng wildcard `*` trong `Access-Control-Allow-Origin`?
9. Ý nghĩa của các header: `Access-Control-Allow-Methods`, `Access-Control-Allow-Headers`, và `Access-Control-Max-Age`?
10. `Access-Control-Expose-Headers` là gì và dùng khi nào?
11. CORS có thể gửi _credentials_ như cookie hay authorization không? Và cần header nào để cho phép?
12. Làm sao để fetch request gửi cookie trong CORS? (fetch/XHR)
13. Bạn triển khai API trên domain A và frontend trên domain B. API báo lỗi “No _Access-Control-Allow-Origin_ header” trong console browser. Nguyên nhân và cách khắc phục?
14. Một request POST kèm custom header (ví dụ `X-CUSTOM`) bị CORS block. Tại sao và server cần trả header gì trong preflight?
15. Một API trả `Access-Control-Allow-Origin: *` nhưng client vẫn nhận lỗi. Nguyên nhân có thể là gì?
16. Tại sao trình duyệt _cache_ kết quả preflight và header nào điều khiển điều này?
17. Giải thích cách CORS liên quan tới việc tải web fonts cross-origin (ví dụ trong CSS `@font-face`).
18. CORS failures trong JavaScript chỉ báo lỗi chung chung. Làm thế nào để debug chúng hiệu quả?

## CORS errors

1. Khi gặp lỗi “Cross-Origin Request Blocked: The Same Origin Policy disallows reading the remote resource…” trong console, điều này nghĩa là gì và bạn nên kiểm tra gì đầu tiên?
2. Tại sao chi tiết lý do lỗi CORS không được JavaScript biết tới (ví dụ qua `fetch`)?
3. Lỗi “CORS disabled” thường xảy ra trong trường hợp nào và cách khắc phục?
4. Thông báo “CORS request did not succeed” thường chỉ ra vấn đề gì?
5. Lỗi “CORS header ‘Origin’ cannot be added” _reason_ ngụ ý điều gì? Khi nào lỗi này xuất hiện?
6. Tại sao một chuyển hướng (redirect) ngoài domain lại bị chặn trong CORS (“CORS request external redirect not allowed”)?
7. Lỗi “CORS request not http” xảy ra khi nào, và vì sao nó bị chặn?
8. Lỗi “CORS header ‘Access-Control-Allow-Origin’ missing” nghĩa là gì trên server?
9. Lỗi “CORS header ‘Access-Control-Allow-Origin’ does not match ‘xyz’” biểu thị điều gì?
10. Giải thích lỗi “Credential is not supported if the CORS header ‘Access-Control-Allow-Origin’ is ‘\*’”.
11. Lỗi “Did not find method in CORS header ‘Access-Control-Allow-Methods’” xuất hiện khi nào?
12. Vì sao thông báo “expected ‘true’ in CORS header ‘Access-Control-Allow-Credentials’” xảy ra?
13. Lỗi “invalid token ‘xyz’ in CORS header ‘Access-Control-Allow-Methods’” có thể do đâu?
14. Lỗi “invalid token ‘xyz’ in CORS header ‘Access-Control-Allow-Headers’” chỉ ra vấn đề gì?
15. Lỗi “missing token ‘xyz’ in CORS header ‘Access-Control-Allow-Headers’ from CORS preflight channel” nghĩa là gì?
16. Tại sao “Multiple CORS header ‘Access-Control-Allow-Origin’ not allowed” lại bị coi là lỗi?
17. Khi debug một lỗi CORS, bạn nên mở tab nào trong Developer Tools để xem chi tiết?
18. Tại sao lỗi CORS console còn có message `Reason: <text>` và điều này quan trọng như thế nào khi fix?
19. Một request CORS không thành công có thể _thành công_ ngoại trừ việc bị chặn vì thiếu header nào đó trên server?

## Content Security Policy (CSP)

1. Content Security Policy (CSP) là gì và mục đích chính của nó?
2. CSP giúp bảo vệ ứng dụng chống lại những loại tấn công nào? Nêu ví dụ cụ thể.
3. CSP được truyền tới trình duyệt thông qua header nào? Có cách khác để khai báo CSP không?
4. `default-src` khác gì so với các directive như `script-src` hay `img-src`?
5. Làm thế nào để chặn hoàn toàn một loại tài nguyên (ví dụ `<object>` và `<embed>`)?
6. Bạn có thể cho phép tài nguyên tải từ nhiều nguồn khác nhau như thế nào?
7. Nonce là gì trong CSP, và chúng được dùng để làm gì?
8. Giải thích sự khác nhau giữa dùng `nonces` và `hashes` trong CSP. Khi nào nên dùng mỗi kiểu?
9. Khi dùng hashes để cho phép script, external script có cần gì thêm để hoạt động?
10. Khi CSP có `script-src`, inline JavaScript sẽ bị chặn trừ khi làm gì?
11. Tại sao nên tránh dùng `'unsafe-inline'` và `'unsafe-eval'` trong CSP?
12. Keyword `'self'` trong CSP có ý nghĩa gì?
13. CSP có hỗ trợ kiểm soát theo scheme (ví dụ HTTPS) không? Cho ví dụ.
14. Bạn có thể dùng wildcard trong CSP source list không? Cho ví dụ.
15. CSP có thể bảo vệ chống clickjacking không? Directive nào liên quan?
16. Làm thế nào để yêu cầu trình duyệt tự động nâng cấp insecure requests sang HTTPS trong CSP?
17. Sự khác nhau giữa CSP enforcement mode và report-only mode là gì?
18. Header nào dùng để đặt một CSP _report-only_?
19. Violation Reporting hoạt động như thế nào với Reporting API?
20. Tại sao nên khai báo cả `report-uri` và `report-to` tạm thời trong CSP?
21. Bạn nên áp dụng CSP ở đâu trong site? Chỉ cho page chính hay mọi resource?
22. Khi triển khai CSP với frontend SPA (client-side), bạn nên cân nhắc điều gì với `<meta http-equiv>`?

## Content Security Policy errors and warnings

1. Khi console báo “The page’s settings blocked the loading of a resource: ...”, điều đó có nghĩa gì trong bối cảnh CSP?
2. Sự khác nhau giữa lỗi CSP _violation_ (blocked) và warning khi CSP ở _report-only_ mode là gì?
3. Thông báo “Tried to send report to invalid URI” nghĩa là gì và nguyên nhân thường gặp là gì?
4. Console có thể log lỗi “Couldn’t parse report URI”. Khi nào lỗi này xảy ra?
5. CSP có thể log “Couldn’t process unknown directive '%1$S'”. Tại sao lỗi này xảy ra?
6. Khi console báo “Ignoring unknown option %1$S”, điều đó có nghĩa gì?
7. Lỗi “Ignoring duplicate source %1$S” xuất hiện trong CSP khi nào?
8. Thông báo “Ignoring source … (Not supported when delivered via meta element)” ám chỉ điều gì?
9. Console có thể log “Keyword ‘strict-dynamic’ ... with no valid nonce or hash might block all scripts from loading”. Bạn giải thích nội dung thông báo này.
10. Thông báo “Ignoring ‘%1$S’ within script-src: nonce-source or hash-source specified” ám chỉ nguyên nhân gì?
11. Khi bạn thấy lỗi “Couldn’t parse invalid source %1$S”, điều này báo hiệu gì trong CSP?
12. Tại sao lỗi “Couldn’t parse invalid host %1$S” có thể xuất hiện khi cấu hình CSP?
13. Console lỗi “Couldn’t parse scheme in %1$S” và “Couldn’t parse port in %1$S” chỉ ra điều gì?
14. Lỗi “Directive '%1$S' has been deprecated. Please use directive 'worker-src' …” có ý nghĩa gì?
15. CSP có thể log “Ignoring sandbox directive when delivered in a report-only policy ‘%1$S’”. Vì sao?
16. Thông báo “An attempt to execute inline scripts has been blocked” xuất hiện khi nào?
17. Tương tự, khi nào trình duyệt log “An attempt to apply inline style sheets has been blocked”?
18. Thông báo “An attempt to call JavaScript from a string … has been blocked” liên quan tới directive nào?
19. Console CSP có thể ghi “Upgrading insecure request '%1$S' to use '%2$S'”. Bạn giải thích thông báo này.
20. Ngược lại, khi log “Blocking insecure request '%1$S'”, điều gì xảy ra?
21. Khi console thấy “This site (…) has a Report-Only policy without a report URI”, vấn đề là gì?
22. Tại sao browser có thể log “Ignoring '%1$S' … because of '%2$S' directive”?
