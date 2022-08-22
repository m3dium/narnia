# narnia - https://overthewire.org/wargames/narnia/

Narnia Level 0:

Sau khi login có 2 file 

![image](https://user-images.githubusercontent.com/72652376/185873600-e4ed95b6-3c87-4210-8ef8-14bb45b95412.png)

![image](https://user-images.githubusercontent.com/72652376/185873648-f8c16659-327a-434d-81bd-324cd398560a.png)

Chương trình này yêu cầu nhập vào 1 giá trị val. Nếu val = 0xdeadbeef thì trả về giá trị system("/bin/sh");

![image](https://user-images.githubusercontent.com/72652376/185873786-837e4f23-c770-4dcc-986e-a344a56c4556.png)

Cơ bản là vậy nhưng giá trị val lại được khai báo ở trên với giá trị long val=0x41414141; nghĩa là ta phải thay đổi được giá trị này

Trên lý thuyết trừ thay đổi mã nguồn thì không thể thay đổi giá trị này

Nhưng ở dưới có khai báo 1 giá trị char buf[20];

Trong khi hàm nhập vào được hẳn 2 ký tự scanf("%24s",&buf);

Thử nhập 20*A + BBBB thì trả về val=0x42424242 (chuyển sang text là BBBB)

![image](https://user-images.githubusercontent.com/72652376/185875575-7f7711a7-1f8d-4d8a-9967-27cafde0404f.png)

Ý tưởng: thay thế BBBB thành 0xdeadbeef thì có thể đổi được val theo yêu cầu

![image](https://user-images.githubusercontent.com/72652376/185876435-90ca7c63-3102-4f0a-a1ef-5a58682829f3.png)

Lấy được pass cho lv sau


Narnia Level 1:

