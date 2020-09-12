<p align="center">
  <img src="images/cover.jpg">
</p>

- [1. Giới thiệu](#1-giới-thiệu)
- [2. Hệ thống nhúng là gì ?](#2-hệ-thống-nhúng-là-gì-)
- [3. Kĩ sư hệ thống nhúng thì làm gì ?](#3-kĩ-sư-hệ-thống-nhúng-thì-làm-gì-)
  - [3.1. Phần cứng](#31-phần-cứng)
  - [3.2. Phần mềm](#32-phần-mềm)
- [4. Vì sao mình chọn nhúng](#4-vì-sao-mình-chọn-nhúng)

# 1. Giới thiệu
Đây là bài viết đầu tiên của mình giới thiệu về hệ thống nhúng (gọi tắt là nhúng), một ngành mình đang học và làm việc tại Pháp. Những kiến thức trong bài là những gì mình được học và trải nghiệm, sau đó được viết lại theo cách hiểu của mình nên chỗ nào sai thì các bạn sửa giúp mình nha.

# 2. Hệ thống nhúng là gì ?
Lúc mới qua Pháp mình nghe các anh chị đi trước nhắc đến hệ thống nhúng nên cũng tập tành lên mạng tìm hiểu xem hệ thống nhúng là gì. Sau một hồi tìm kiếm thì lượm được vài định nghĩa "Hệ thống nhúng là một hệ thống được tích hợp cả phần cứng và phần mềm phục vụ cho các bài toán chuyên dụng trong nhiều lĩnh vực công nghiệp, tự động hóa điều khiển, quan trắc và truyền thông". Với định nghĩa này thì mình nghĩ các bạn mới học khó mà hiểu hệ thống nhúng là gì (lúc mới đọc mình chả hiểu gì cả =))). Sau một thời gian đi thực tập thì mình nghĩ

> Hệ thống nhúng là hệ thống thay thế con người làm những công việc tẻ nhạt 

Những công việc tẻ nhạt ở đây là gì, lấy ví dụ luôn cho nóng 😙

Một ví dụ dễ hiểu nhất là con robot hút bụi, những con cùi mía tầm 20-30k, nhầm 2-3tr thì nó chạy loạn xì ngầu và hút bụi ngẫu nhiên trong nhà của bạn và tất nhiên kết quả là sàn nhà không bao giờ sạch được. Những con 10 triệu trở lên thì nó sẽ lập bản đồ cái nhà của bạn luôn, rồi tự thiết kế đường đi để có thể đảm bảo sàn nhà bao giờ cũng sạch bong. Mỗi sáng trước khi ra khỏi nhà chỉ cần đạp cho nó 1 cái thì đảm bảo lúc đi làm về nhà sẽ sạch bong như đang ở với ba mẹ vậy.

Vậy ở ví dụ trên thì con robot hút bụi là 1 hệ thống nhúng hoàn chỉnh, nó giúp bạn đỡ phải lau nhà rồi đấy. Cũng như mấy cái cửa tự động mở ở siêu thị khi có người lại gần, cái điều hòa tự chỉnh hướng gió để thổi vào người,... chỉ cần để ý một chút thì bạn sẽ thấy hệ thống nhúng đang làm giúp chúng ta rất nhiều việc trong cuộc sống.

# 3. Kĩ sư hệ thống nhúng thì làm gì ?
Với ví dụ con robot hút bụi thì kĩ sư hệ thống nhúng phải thiết kế phần cứng (mạch điện, linh kiện điện tử,... các bạn thử mở cái máy hút bụi ra, nhìn vào bên trong thấy cái gì thì đó là phần cứng đấy) cũng như phần mềm (phần mềm lập bản đồ căn nhà,... mấy thứ mà có mở ra cũng chả thấy được ấy).

Do một người thì gần như không thể ôm trọn cả thiết kế phần cứng cũng như phần mềm (vì nó nhiều kiến thức lắm, như bác sĩ thì không ôm cả nội khoa lẫn ngoại khoa cùng một lúc í, chết người đó 🙅) nên mình sẽ chia thành 2 nhóm cho dễ giới thiệu nha.

## 3.1. Phần cứng
Phần cứng có thể hiểu là cái gì cứng cứng vào nhìn thấy được ấy 😤. Ví dụ như là thiết kế 1 board mạch với các linh kiện điện tử: điện trở, tụ điện, cuộn cảm,....  như cái hình dưới này nè

<p align="center">
  <img width="460" src="images/Green-Printed-Circuit-Board.jpg">
</p>

Để theo mảng này thì bạn phải nắm cực kì vững kiến thức về cách hoạt động của các linh kiện điện tử, đọc hiểu được datasheet của con chip (cái cục đen đen to nhất ấy),... và nhiều thứ cao cấp hơn nữa mà mình cũng không biết (do thấy khó quá nên mình bỏ không đu theo nữa )

## 3.2. Phần mềm
Đây là ngành mà mình đu bám nên sẽ có bài giới thiệu chi tiết sau nha, chừ giới thiệu so so mai mai đã.

Trái ngược với phần cứng thì phần mềm là những thứ mà bạn không thấy được, ví dụ như cơ thể người phần cứng là tay, chân,... thì phần mềm là tinh thần, suy nghĩ của bản thân đấy (cái gì lúc mềm lúc cứng thì là ngoại lệ rồi nhé 😶). Để đú đởn như phần cứng thì mình cũng chụp ảnh một đoạn code trong lúc thực tập của mình, nhìn giống nắc cơ à nhầm hacker không các bạn

<p align="center">
  <img width="700" src="images/Software.png">
</p>

Những bạn theo mảng này thì xác định sẽ ngồi trước máy tính 1 ngày 8 tiếng liên tục nha (do lúc trước mình nghĩ làm nhúng phần mềm thì ít ngồi trước máy tính, vào làm thì mới biết ngồi sấp mặt lợn luôn không khác gì lập trình viên cả 🙏), đồng thời các bạn phải học giỏi lập trình ngôn ngữ C và C++ nữa thì mới đu theo được. 


# 4. Vì sao mình chọn nhúng
Các bạn có thể thấy là hệ thống nhúng giúp mình làm quá trời việc, mà mình thì lười lắm nên cuộc sống càng tiện nghi thì mình càng thích. Tưởng tượng sau này nằm trên ghế búng tay phát là có 1 con robot đem đồ ăn tới, búng phát nữa thì nó lau nhà, tưới cây, giặt đồ, dỗ người yêu, cảm giác đó nó ngầu lắm các bạn à. Vậy nên mình mới theo ngành này để đem tương lai đó tới càng gần càng tốt (tới sớm còn hưởng chứ 70-80 tuổi rồi sức đâu búng tay nữa 😔).

Mình cũng thích có mấy con nô lệ chạy loăng quăng trong nhà nữa, vừa dễ bảo sai gì làm đó vừa nuôi ít tốn cơm (chứ sai vợ thì xác cmn định.....) nên vừa phát hiện ra ngành này thì mình đu theo ngay =)))

Giờ mình nghĩ các bạn cũng biết sương sương hệ thống nhúng là gì rồi đó, bài viết sau mình sẽ giới thiệu sâu hơn về lập trình phần mềm nhúng, cần chuẩn bị gì, học gì đồ rứa nha.
