Trong bài viết này mình sẽ giới thiệu cho các bạn sơ lược về `Cơ sở dử liệu Nosql`.So sánh sự khác nhau Nosql và Sql?
### 1. Cơ sở dữ liệu NoSQL 
#### 1.1 NoSQL là gì ?
*   NoSQL là một dạng Cơ sở dữ liệu (CSDL) mã nguồn mở và được viết tắt bởi: None-Relational SQL. NoSQL được phát triển trên Javascript Framework với kiểu dữ liệu là JSON và dạng dữ liệu theo kiểu key và value.
*   NoSQL đang dần nổi lên như một thế lực trong giới lập trình. Nhà nhà quảng cáo NoSQL, người người sử dụng NoSQL. MEAN stack (MongoDB, Express, AngularJS, NodeJS) đang dần lấn lướt, thay thế cho LAMP stack (Linux, Apache, MySQL, PHP/Python). 
*   Trước NoSQL, từng có một thứ gọi là SQL (Structure Query Language) - ngôn ngữ truy vấn có cấu trúc truy vấn trên RDBMS (Relational Database Management System) được sử dụng rất rộng rãi trong hầu hết tất cả các ứng dụng vì tính ràng buộc và đồng nhất về dữ liệu của người dùng được đảm bảo. Tuy nhiên, RDBMS vẫn còn một số khuyết điểm, việc thay đổi cấu trúc dữ liệu là rất phức tạp, đòi hỏi quá cao vần phần cứng và đặc biệt là không tối ưu về tốc độ xử lí. Cơ sở dữ liệu NoSQL ra đời để giải quyết những khuyết điểm đó.
#### 1.2 Tại sao nên dùng NoSQL?
*   Với đặc điểm là nâng cao khả năng thay đổi và mở rộng hệ thống một cách dễ dàng, NoSQL còn tối ưu về hiệu suất, tốc độ xử lí, bỏ qua các cơ chế ràng buộc và không đòi hỏi quá cao về phần cứng.
*   Dữ liệu trong NoSql được lưu dưới dạng Document, Object. Truy vấn dễ dàng và nhanh hơn nhiều so với RDBMS.
*   NoSQL có thể làm việc tốt với dữ liệu dạng không có cấu trúc.
*   Việc thay đổi cấu trúc dữ liệu (thêm, xóa trường hoặc bảng) rất dễ dàng và nhanh gọn
*   Vì không đặt nặng tính ACID của các transactions và tính nhất quán của dữ liệu, NoSQL DB có thể mở rộng, chạy trên nhiều máy cách dễ dàng.
*   So sánh một số tính năng chính giữa SQL và NoSQL:

| Tính năng  | SQL | NoSQL |
| -------- | -------- | -------- |
| Hiệu năng  | 	Kém hơn NoSQL vì khi truy vấn nó phải tính toán, kiểm tra và xử lý các mối quan hệ giữa các bảng. | Tốt hơn SQL vì nó bỏ qua các ràng buộc.  |
| Mở rộng theo chiều ngang     | Có thể thực hiện được nhưng quá trình mở rộng sẽ rất phức tập nếu đã tồn tại dữ liệu trong database.     | Mở rộng dể dàng.     |
| Phần cứng |	Đòi hỏi phần cứng cao	|Không đòi hỏi quá cao về phần cứng  |
| Thay đổi số node trong hệ thống|	Vì tính nhất quán về dữ liệu nên khi thêm hay xóa một node cần phải shutdown hệ thống trong một khoảng thời gian	|Vì có tính nhất quán cuối nên sẽ không cần phải shutdown hệ thống     |
| Truy vấn và báo cáo	|Dễ dàng sử dụng ngôn ngữ SQL query để truy vấn trực tiếp dữ liệu từ Database hoặc dùng công cụ hỗ trợ để lấy báo cáo	|Việc lấy báo cáo dữ liệu trực tiếp từ NoSQL chưa được hổ trợ tốt, thực hiện chủ yếu thông qua giao diện ứng dụng     | 
| Mở rộng dữ liệu|	Khi muốn bổ sung thêm cột cho một bảng, chúng ta phải khai báo trước	|Không cần khai báo trước  |
| Ứng dụng	|Sử dụng để xây dựng những hệ thống có quan hệ chặt chẽ và cần tính đồng nhất về dữ liệu như: tài chính, ngân hàng, chứng khoán,…	|Sử dụng xây dựng những hệ thống lưu trữ thông tin lớn, không quá quan trọng về vấn đề đồng nhất dữ liệu trong một thời gian nhất định. VD như: báo chí, mạng xã hội, diễn đàn, shopping,…     | 

#### 1.3 Các loại NoSQL Database
##### a. Key – value: 
Dữ liệu được lưu dưới dạng key-value giống Dictionary trong C#, ArrayList trong Java.
+ DB tiêu biểu: Riak, Redis, MemCache, CouchBase.
+ Ứng dụng: Do tốc độ truy xuất nhanh, nên key-value thường được dùng để làm cache cho ứng dụng.
![alt text](https://websolutions.com.vn/wp-content/uploads/2019/01/2-15.png)
##### b.  	Column Family:
Dữ liệu được lưu trong DB dưới dạng các cột, thay vì các hàng như SQL. Mỗi hàng sẽ có một key/id riêng biệt. Điều khác biệt là các hàng trong một bảng sẽ có số lượng cột khác nhau.
+ DB tiêu biểu: Cassandra (Phát triển bởi Facebook), HyperTable, Apache HBase.
+ Ứng dụng: Column-family DB được sử dụng khi ta cần ghi một số dữ liệu lớn, big data.

![alt text](https://techinsight.com.vn/wp-content/uploads/2016/12/14785892887194.png)
##### c. Graph DB:
Dữ liệu trong graph DB sẽ được lưu dưới dạng các node, mỗi node có 1 label, 1 số properties như một row trong SQL. Các node được nối với nhau bằng các relationship. Graph DB tập trung nhiều vào các relationship của các node, áp dụng nhiều thuật toán để tăng tốc.
+ DB tiêu biểu: Neo4j, InfinityGraph, OrientDB, hypergraphDB.
+ Ứng dụng: Khi cần truy vấn các mối quan hệ, graph DB truy vấn nhanh và dễ hơn nhiều so với DB. Được dùng trong Mạng nơ-ron, chuyển tiền bạc, mạng xã hội (tìm bạn bè), giới thiệu sản phẩm (dựa theo sở thích/ lịch sử,...).
##### d.  	Document DB
Mỗi Object sẽ được lưu dưới dạng Document. Dữ liệu được lưu dưới dạng JSON, XML.
+ DB tiêu biểu: MongoDB(*), RavenDB, CouchDB, OrientDB.
+ Ứng dụng: Do nhanh và linh động, document DB thường đóng vai trò làm DB các ứng dụng prototype, big data.
#### 1.4  Một số khái niệm mới trong NoSQL
+   Fields – tương đương với khái niệm Columns trong SQL
+   Document – thay thế khái niệm row trong SQL. Đây cũng chính là khái niệm làm nên sự khác biệt giữa NoSQL và SQL, 1 document chứa số cột (fields) không cố định trong khi 1 row thì số cột(columns) là định sẵn trước.
+   Collection – tương đương với khái niệm table trong SQL. Một collection là tập hợp các document. Điều đặc biệt là một collection có thể chứa các document hoàn toàn khác nhau.
+   Key-value – cặp từ khóa – giá trị được dùng để lưu trữ dữ liệu trong NoSQL
+   Cursor – tạm dịch là con trỏ. Chúng ta sẽ sử dụng cursor để lấy dữ liệu từ database.
+   Indexes ~ counterparts: Trong các hệ cơ sở dữ liệu quan hệ, các cột được định nghĩa theo bảng còn với hệ cơ sở dữ liệu không ràng buộc, các cột được định nghĩa ở mỗi document. Bởi thế, các document quản lí gần như tất cả, các collection không cần quản lí chặt chẽ những gì đang xảy ra trong nó nữa .
#### 1.5 Ưu điểm và hạn chế của NoSQL

| Ưu điểm	|Nhược điểm  |
| -------- | -------- | 
|  Vì không có Schema nên dữ liệu thay đổi linh hoạt và ít bị đóng khung hơn.  Cấu trúc của một đối tượng rõ ràng.Không có các JOIN phức tạp.Có thể mở rộng dữ liệu dễ dàng không cần lo đến các vấn đề như khóa chính, khóa ngoại, kiểm tra ràng buộc.Đảm bảo chỉ cập nhật một tài liệu lưu trữ duy nhất. Cho phép lưu bất kỳ loại dữ liệu nào tại bất cứ đâu, ở bất cứ thời điểm nào mà không cần xác thực|  Ưu điểm cũng chính là nhược điểm của NoSQL khi nó không đòi hỏi dữ liệu phải liên kết chặt chẽ và thống nhất.Không có transaction để phục vụ cho các ứng dụng như ngân hàng, quản lý kho,…Các ứng dụng cần sử dụng JOIN|
### 2. Tìm hiểu và cài đặt MongoDB
#### 2.1 MongoDB là gì?
+  MongoDB là một hệ quản trị cơ sở dữ liệu mã nguồn mở và là cơ sở dữ liệu thuộc NoSQL phổ biến nhất. MongoDB được viết bằng C++ và được hàng triệu người sử dụng, xếp thứ 4 trong số các hệ thống cơ sở dữ liệu phổ biến nhất (tính đến tháng 2/2015).
+  MongoDB lưu các dữ liệu trong các document dạng JSON thay vì dạng bảng như CSDL quan hệ nên truy vấn sẽ rất nhanh cung cấp hiệu suất cao, tính khả dụng cao và khả năng mở rộng dễ dàng. 
#### 2.2 MongoDB với RDBMS.
Một vài sự khác nhau giữa các MongoDB và RDBMS (Cơ sở dữ liệu quan hệ):


| SQL DB |MongoDB |
| -------- | -------- |
| Database|Database |
|Table|Collection|
|Row	|Document|
|Column|	Field|
|Join|Embeded documents, linking|
|Primary Key (tự chọn)	|Primary key (mặc định _id)|

Mình tiến hành thực hiện một số các truy vấn cơ bản trên MongoDB và SQL Server để so sánh thời gian thực hiện của 2 hệ quản trị CSDL này. Chúng em thực hiện các truy vấn trên Cơ sở dữ liệu giống nhau, các thao tác giống nhau, thực hiện các thao tác cho các đối tượng giống nhau để đảm bảo tính công bằng và kết quả so sánh chính xác nhất. 
Dưới đây là kết quả thực hiện của từng truy vấn và kết quả so sánh tổng hợp
###### a. Thời gian thực hiện truy vấn tìm kiếm SQL Server (select)
![alt text](https://images.viblo.asia/fdd35fb8-0150-4936-9a2b-ba122b9978dc.png)
###### b: Thời gian thực hiện truy vấn tìm kiếm MongoDB (find) 
![alt text](https://images.viblo.asia/0a748a4a-c7c9-4ab7-a209-074d18fdb65e.png)
###### c: Thời gian thực hiện câu lệnh thêm mới SQL Server (insert into)
![alt text](https://images.viblo.asia/fb536759-cae7-415b-9101-0845dd10ae9c.png)
###### d: Thời gian thực hiện câu lệnh thêm mới MongoDB (insert)
![alt text](https://images.viblo.asia/1507c889-508b-48a5-a76d-91c5b936db08.png)
###### e: Thời gian thực hiện câu lệnh cập nhật SQL Server (update)
![alt text](https://images.viblo.asia/a1e6e189-e5d3-450e-bd21-6f24e93e52e6.png)
###### f: Thời gian thực hiện câu lệnh cập nhật MongoDB (update)
![alt text](https://images.viblo.asia/1127ee8f-074c-4d2b-b9dd-116631ced176.png)
###### g: Thời gian thực hiện câu lệnh xóa SQL Server (delete)
![alt text](https://images.viblo.asia/2329e0db-a095-4088-9d6d-0cb91e692a9f.png)
###### h: Thời gian thực hiện câu lệnh xóa MongoDB (remove) 
![alt text](https://images.viblo.asia/e7b3ae8e-0c43-452b-a970-14bc5166a977.png)

#### 2.3 Tại sao nên sử dụng MongoDB?
Bởi vì MongoDB:
+   Lưu trữ hướng tài liệu - dữ liệu được lưu trữ dưới dạng tài liệu kiểu JSON.
+   Chỉ mục trên bất kỳ thuộc tính
+   Nhân rộng và sẵn sàng cao.
+   Tự động bảo vệ.
+   Truy vấn phong phú.
+  Cập nhật nhanh tại chỗ.
+  Hỗ trợ chuyên nghiệp bởi MongoDB
 #### 2.4 Khi nào nên dùng MongoDB
Ví dụ như các hệ thống realtime (thời gian thực) yêu cầu phản hồi nhanh, Các hệ thống bigdata với yêu cầu truy vấn nhanh hay các hệ thống có lượng request lớn thì MongoDB sẽ là sự lựa chọn ưu tiên hơn CSDL quan hệ. Tùy theo dự án và trường hợp cụ thể để sử dụng CSDL quan hệ hay sử dụng MongoDB đem lại hiệu quả cao.
#### Link tham khảo:
http://expressmagazine.net/development/2330/dinh-nghia-mongodb-nosql-la-gi https://viblo.asia/p/tim-hieu-ve-mongodb-4P856ajGlY3#_8-khi-nao-nen-su-dung-mongodb--7 https://stackjava.com/mongodb/uu-nhuoc-diem-cua-mongodb-khi-nao-nen-dung-mongodb.html