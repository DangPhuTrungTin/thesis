---


---

<h2 id="đề-tài-luận-văn">Đề tài luận văn:</h2>
<ul>
<li>Xây dựng mô hình XaaS (Anything as a Service) từ kiến trúc Open data system</li>
</ul>
<h2 id="giải-thích-thuật-ngữ">Giải thích thuật ngữ</h2>
<ul>
<li>Họ  as-a-Service nói chung dùng để diễn tả một sản phẩm được cung cấp tới người dùng thông qua internet. Một số dạng as-a-Service hiện nay như Data-as-a-service, Software-as-a-service, Service-as-a-service,… chúng có thể có trả phí hoặc không có trả phí.</li>
</ul>
<h2 id="ý-tưởng">Ý tưởng</h2>
<ul>
<li>Trong ngữ cảnh open data, Data-as-a-service đã được cung cấp bằng chứng là chúng ta có thể lưu trữ dữ liệu trên hệ thống, đồng thời hệ thống cũng cung cấp stat, visualization, API,… cho người dùng dưới hình thức public và complimentary.</li>
<li>Từ nguồn dữ liệu open nêu trên hoàn toàn có thể khai thác chúng và tạo nên những dạng as-a-service khác và chúng cũng public và complimentary, tạm  gọi là Open-as-a-service (OaaS).</li>
</ul>
<h2 id="hiện-thực">Hiện thực</h2>
<ul>
<li>Trước mắt 2 dạng OaaS sẽ có thể khai thác đó là Software-as-a-service ( ví dụ như dự báo thời tiết từ dữ liệu thời tiết trung ương), Service-as-a-service (ví dụ như dịch vụ phân tích dữ liệu tài chính và sẽ trả về các chỉ số phát triển). Dạng Software-as-a-service sẽ phụ thuộc vào nguồn data có sẳn, dạng  Service-as-a-service sẽ do người dùng cung cấp. OaaS có thể là do bên thứ 3 hoặc do chính system cung cấp.</li>
<li>Nhiệm vụ của open data system <strong>trung gian</strong> giữa người dùng và nhà phát hành dịch vụ/phần mềm . Cụ thể, ở open data portal sẽ show up <strong>web interface</strong> cho phần mềm (phầm mềm được deploy trên hệ thống) hoặc <strong>API</strong> cho dịch vụ và cung cấp giao diện quản lý respository cho owner. Phía nhà phát hành sẽ được cung cấp <strong>Source Code/API Management CLI</strong> đơn giản (gồm push, pull, start, stop)  đối với phần mềm và đăng kí API đối với dịch vụ vầ sẽ sử dụng SSH,HTTPS,… để connect vào hệ thống. CLI này là 1 dạng python script module và có thể download thông qua pip. Để đảm bảo những config của OaaS sẽ được lưu trong database thay vì trong config file, và phần giao tiếp sẽ được thực hiện trong <strong>Message Queue</strong> và các task sẽ được giao cho <strong>worker server</strong> để tránh ảnh hưởng đến hệ thống khác và portal.</li>
</ul>
<h2 id="tóm-lại">Tóm lại</h2>
<p>Để cung cấp OaaS ta cần 3 thành phần:</p>
<ul>
<li><strong>Web interface</strong> : user giao tiếp với hệ thống, nhà phát hành quản lý source code.</li>
<li><strong>CLI</strong>: nhà phát hành thông tác lên server</li>
<li><strong>Message Queue và worker server</strong>: thực hiện các request của user.</li>
</ul>
<h2 id="khả-năng-hiện-thực">Khả năng hiện thực</h2>
<ul>
<li>Đây chỉ là bản phát thảo ý tưởng nên có thể quá sức hiện thực nhưng sẽ cho thấy một cái nhìn tổng quát về OaaS.</li>
</ul>

