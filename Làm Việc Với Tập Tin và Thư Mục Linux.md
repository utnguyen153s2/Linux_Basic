## 1. Lệnh ls - Xem danh sách tập tin thư mục
**ls -[tùy chọn] [ đường dẫn thư mục muốn xem]**

Các tùy chọn phổ biến của lệnh ls:

| Các tùy chọn của lệnh | ý nghĩa |
| ----------------------- | ------- |
| -L                     | Hiển thị danh sách tập tin, thư mục (chỉ hiện tên). |
| -I                     | Hiển thị danh sách tập tin, thư mục(bao gồm nhiều cột: file name, size, date...) |
| -A                     | Liệt kê tất cả các tập tin, thư mục bao gồm những tập tin ẩn. |
| -R                     | Liệt kê tất cả các tập tin , thư mục kể cả các tập tin, thư mục bên trong thư mục cha |

Ngoài ra chúng ta còn có thể sử dụng "man" để xem các tùy chọn của lệnh ls.

`man ls`

### 1.1. Lệnh grep
##### Lệnh grep - lọc lại tên tập tin thư mục muốn xem

Lệnh `ls -l` của "/" cho kết quả nhiều thộng tin, nếu muốn lọc lại tên tập tin thư mục muốn xem chỉ cần thên `grep`.

` lệnh | grep [nhập ký tự muốn lọc]`

**Ví Dụ** . Muốn xem trong "/" có tập tin . thư mục nào có chứa ký tự là student thì thực hiện lệnh sau :

`ls -l | grep student`

##### Lệnh grep còn còn được dùng để tìm kiếm chuối  trong file :

`grep " chuoi " tên file `

##### Lệnh grep còn được dùng tìm kiếm chuỗi trong nhiều file cùng lúc:

` grep " chuoi " file_pattern`

 **chú ý** : `Dùng ký hiệu "*" để thực hiện tìm kiếm nhiều tập tin cùng một lúc. `

**Ví Dụ** : Tìm kiếm chuối "yum" trong các file có đuôi .txt trong thư mục /root :

` grep "yum" /root/*.txt `

## 2. Lệnh cd

Lệnh `cd` dùng để đổi sang thư mục khác.

##### Các lệnh cd thông dụng 
 - Di chuyển về thư mục gốc : cd/
 - Di chuyển đến một vị trí bất kì khi biết đường dẫn tuyệt đối: cd /etc /network
 - Di chuyển đến thư mục còn nằm trong thư mục hiện tại: cd docs hoặc./docs
 - Di chuyển đến thư mục mẹ:
 `cd..                        `
  
  Hoặc 
  
  `cd../.. : di chuyển đến thư mục mẹ hai lần `
  
  - Lệnh cd không có tham số, sẽ đưa bạn về home directory, dù bất kể bạn đang ở đâu :cd hoặc cd~
  - Lệnh cd dùng để quay về trước thư mục trước :cd -
  
  ## 3. Lệnh pwd
 Lệnh `pwd` chúng ta sẽ có ful path của thư mục mà chúng ta dang dùng ở hiện tại.
 
 `pwd`
 
 ## 4. Lệnh mkdir - dùng để tạo thư mục 
 
 Lệnh `mkdir` được sử dụng để tạo một thư mục trong thư mục hiện tại:
 
  `mkdir [tên thư mục cần tạo ]
  
  Ví Dụ : Tạo thư mục tên exampledir trong thư mục hiện tại:
  
  `mkdir exampledir `
  
  ## 5. Lệnh xóa tập tin thư mục
  ##### 5.1 Xóa tập tin :
  `rm [đường dẫn ]`
  
  Ví Dụ : Xóa tập tin abc.txt trong /usr/passwod:
  
  `rm /usr/password/abc.txt`
  
  ##### 5.2 Xóa tập tin mà không cần hỏi:
  `rm -f [ đường dẫn]`
  
  Ví Dụ : Xóa tập tin abc.txt trong /usr
  
  `rm -f /usr/password/abc.txt`
  
  ##### 5.3 Xóa thư mục
  
 `rm -rf [đường dẫn]`
 
 Ví Dụ : Xóa thư mục example trong /usr/bin:
 
 `rm -rf /usr/bin/example`
 
 ##### 5.4 : Xóa thư mục rỗng
 
`rmdir [đường dẫn ]`

Ví Dụ : Xóa thư mục trong dir trong /usr/bin:

`rmdir dir`

## 6. Lệnh sao chép tập tin :
##### 6.1 Lệnh sao chép tập tin

`cp [đường dẫn nguồn] [ đường đẫn địch]`

Ví dụ : Sao chép thư mục abc.txt trong thư mục /root sang /usr:

`cp /root/abc.txt /usr`

##### 6.2 Lệnh sao chép thư mục

`cp -r [đường dẫn nguồn] [đường dẫn đich]`

Ví dụ :Sao chép thư mục /root/networks sang /usr/bin:

`cp -r/root/network /usr/bin`

## 7. Lệnh mv - dùng để di chuyển, chuyển đổi tên

Lệnh `mv` thực hiện nhiệm vụ kép . Nó có thể thực hiện:

##### 7.1 Cần đổi tên một tập tin

`mv [đường dẫn với tên cũ] [đường dẫn với tên mới]`

Ví Dụ :Đổi tên tập tin test1.txt trong /root thành test2.txt:

`mv /root/test1.txt /root/test2.txt`
##### 7.2 Di chuyển một tập tin đến vị trí khác, trong khi đó nó có thể đổi tên cùng lúc.

 `mv [đường dẫn nguồn] [đường dẫn đích]`
 
 Ví Dụ : Di chuyển và đổi tên tệp tin test1.txt trong /root sang /etc đổi tên thành test.txt:
 
 `mv /root/test1.txt /etc/test.txt`
 
 ## 8. Lệnh touch - dùng để tạo tệp rỗng.
 Lệnh `touch` thường được dùng để thiết lập hoặc cập nhật quyền truy cập, thay đổi và sửa đổi thời gian của tệp . Theo mặc định, nó đặt lại dấu thời gian của tệp đế khớp với thời gian hiện tại.
 
 Ngoài ra lệnh `touch` còn để tạo tệp rỗng.
 
 `touch [tên tệp]`
 
 Ví Dụ : Tạo tệp test1.txt:
 
 `touch test1.txt`
 
 Lệnh `touch` còn cung cấp một số tiện ích, như tùy chọn -t cho phép bạn cài đặc thời gian của tệp.
 
 `touch -t[thời gian] [tên tệp]`
 
 Ví Dụ : Đặt thời gian cho tệp myflie, ngày 9 tháng 12 vào lúc 4 giờ chiều(12091600)
 
 `touch -t 12091600 myfile`
 
 ## 9. Dùng trình soạn thảo vi.
 
 Linux có nhiều chương trình cho phép soạn thảo văn bản như : vi emacs,joe ,pico,.. Chương trình soạn thảo văn bản thông dụng nhất đó là vi.
 
 Khi `vi` khởi động sẽ ở chế độ dòng lệnh. Để chuyển đổi sang chế độ soạn thảo nhấn phím insert. Để trở lại chế độ dòng lệnh thì chọn ESC.
 
 `vi [đường dẫn]`
 
 Ví Dụ : Tạo tập tin 123.txt và đặt trong thư mục /usr/bin với nội dung là " dung trình soạn thảo vi"
 
 **Bước 1** : Dùng lệnh vi để để tạo tập tin 123.txt. Nều tập tin này đã có thì cũng dùng vi để mở theo cú pháp trên.
 
 `vi 123.txt`
 
 **Bước 2** : Nhấn phím i để nhập nội dung " dung trinh soan thao vi".
 
 **Bước 3**: Nhấn phím ESC để nhập một tring các yêu cầu sau:
 - `q!` : Thoát mà không lưu
 - `wq` : Lưu và thoát khỏi tập tin.
 
 Các câu lệnh và tác dụng trong chế độ dòng lệnh của trình soạn thảo vi:
 
 | Câu Lệnh | Tác Dụng |
 | ------------ | ----------- |
 | ^ hoặc 0 | Di chuyển con trỏ đến vị trí bắt đầu của dòng lệnh hiện tại |
 | $ | Di chuyển con trỏ đến vị trí kết thúc của dòng hiện tại. |
 | i,a | Chèn văn bản ngay trước/sau vị trí con trỏ |
 | X | Xóa ký tự sau con chỏ |
 | Dw | Xóa một từ ( bao gầm cả ký tự trống ngay sau nó ) |
 | D | Xóa từ vị trí con trỏ đến cuối dòng |
 | d^ | Xóa tư vị trí bắt đầu dòng đến vị trí ký tự trống hay ký tự bên trái con trỏ. |
 | U | Hủy bỏ thay đổi trước đó |
 | /pattern | Tìm xâu pattern. Theo hướng tiến |
 | ?pattern | Tìm xâu pattern, theo hướng lùi về đầu văn bản. |
 | n,N | Lặp lại việc tìm kiếm theo cùng hướng / ngược hướng |
 | p,P | Dán đoạn văn bản vừa vào trước / sau con trỏ . |
 | . | Lặp lại câu lệnh  cuối |
 | Dd | Xóa dòng con trỏ đang chạy |
 | :w | Ghi lại tất cả các thay đổi của file hiện tại và tiếp tục soạn thảo |
 | :q! | Kết thúc, không lưu trữ bất kỳ thay đổi nào |
 | :ZZ | Lưu thay đổi của file hiện tại và kết thúc . |
 
 ## 10. Tạo tập tin có nội dung :
 
 ` echo " noi dung " >[ đường dẫn ]`
 
 Ghi vào dòng tiếp theo của tập tin có nội dung :
 
 ` echo " noi dung tiep theo " >>[ đường dẫn]`
 
 ## 11. Xem tập tin 
 
 Chúng ta sử dụng các lệnh để xam tệp tin :
 
 | Lệnh | Chức Năng |
 | -------- | -----------|
 | cat | Dùng để xem các tệp không quá dài . |
 | tac | Dùng để xem nội dung của một tập tin ngược bắt đầu từ dòng cuối. |
 | tess | Dùng để xem tệp lớn hơn vì đây là chương trình phân trang. |
 | tail |  Dùng để in 10 dòng cuối của tệp theo măc định . Chúng ta có thể thay đổi số dòng bằng cách thêm vào -n sau tail, n là số dòng bạn muốn. |
 | head | Dùng để in 10 dòng đầu cảu tệp theo mạc định.Chúng ta có thể thay đổi số dòng bằng cách thêm -n vào sau head, n là số dòng bạn muốn. |
 
 ## 12. Lệnh tìm kiếm 
 
 ` find [ đường dẫn] -name [ tên cần tìm]`
 
 Ví Dụ : Tìm vị trí của tập tin xyz.txt trong /ect:
 
 ` find / etc / -name xyz.txt`
 
 Ngoài việc tìm theo tên (-name ), có thể tìm theo các tùy chọn khác như : -type , user, -atime, newer,... Sử dụng lệnh man find để tìm kiếm chi tiết.
 
 ` Chú ý : Có thể dùng ký hiệu "*" để thực hiện xóa, tìm kiếm, sao chép... nhiều tập tin cùng một lúc.`
 
 ##### 12.0 Tìm theo thời gian  và size 
 
 Find có thêm cả phần lọc kết quả theo thời gian và size nữa.
 
 ##### 12.1 Size
 
 Ta có thể tìm những file có dung lượng tùy ý, bằng cách dùng  -size. Một số option thường dùng:
 
 - c : bytes
 - k : kilobytes
 - m : megabytes
 - g : gigabytes
 - b : 512-byte blocks
 
 Tìm tất cả các file nặng đúng 100 bytes:
 
 ` find / -size 100c`
 
 Tìm tất cả các file nhỏ hơn 100 bytes:
 
 `find / -size -100c`
 
 Hoặc tìm các file nặng hơn 1 GB:
 
 ` find / -size +1G`
 
 ##### 12.2 : Time
 
 Linux lưu trữ 1 vài thông tin liên quan đến thời gian như : thời gian điểm truy cập, thời gian chỉnh sửa và thời gian thay đổi file.
 
 - Access Time ( thời điểm truy cập ): Lần cuối cùng file được đọc hoặc ghi vào.
 - Modification Time ( Thời điểm chỉnh sửa ): Lần cuối nội dung file được chỉnh sửa.
 -Change Time( Thời điểm thay đổi) : Lần cuối mà inode meta-data của file bị sửa.
 
 Tương đương với các thông tin trên , ta dùng -atime, -mtime, -ctime, và cả "-" và "+" để lọc ra những thời gian trước hay sau thời gian đó.
 
 Để tìm các file được chỉnh sửa trong một ngày trước :
 
 ` find / -mtime 1`
 
 Tìm các file được truy cập trong ngày hôn qua :
 
 `find / ctime -1`
 
 Các file mà meta-data bị chỉnh sửa lần cuối là trong 3 ngày trước và hơn :
 
 ` find /-ctime +3`
 
 Hoặc tìm theo phút chứ không phải theo ngày :
 
 `find / mmin-1`
 
 Lệnh trên sẽ tìm các file được chỉnh sửa trong vòng 1 phút trước.
 
 Lệnh find còn có thể so sánh với 1 file, và trả về những file mới hơn :
 
 `find / -newer myfile`
 
##### 12.3 Tìm theo Owner và Permission
 
Chúng ta có thể tìm theo user hay group owner bằng `-user` và `-group`.

**Tìm các file mà user " test" sở hữu:

`find /-user test`

Hoặc các file mà group "newgroup" sở hữu:

` find / - group newgroup`

**Chúng ta cũng tìm được theo permission của file, bằng -perm.

Tìm những file có permission 664:

` find / -perm -664`

Hoặc những file có permission ít nhất 664, nghĩa là gồm cả các file có permission là 744:

`find / -perm -664`

##### 12.4 Kết hợp find và command khác 

Chúng ta còn có thể kết hợp ` find` và các command khác để sử lý những file vừa tìn được với `-exec`

`find find_parameters -exec command_and_params {} \;

Tìm các file có permission là 664 và chmod sang 755:

`find/ -type f -perm 644 - print -exec chmod 755 {} \;`

Tìm một file test.txt và xóa nó.

`find .-type f -name "test.txt" -exec rm -f {} \;`
  
Hoặc xóa các file có đuôi .py ở hiện tại .

`find. -type f -name "*.py" -exec rm -f {} \;`

## 13. Lệnh nén và giải nén tập tin thư mục 

Tong hệ thống Linux tồn tại một số dạng nén cơ bản như : zip ,... Dưới đây là một vài ví dụ về cách giải nén và nén với định dạng đó.

 Nén và giải nén tập tin có đuôi là .gz

`gzip [đường dẫn ]`

Ví Dụ : Nén tập tin test.txt trong thư mục /usr/bin thành test.txt.gz:

`gzip /usr/bin/test.txt                                                                                    gunzip [đường dẫn]`

Ví Dụ 2: Giải nén tập tin test.txt.gz trong thư mục /usr/bin:

` gunzip /usr/bin/test.txt`

## 14. Lệnh locate

Leenhjn` locate` giúp chúng ta tìm kiếm rất nhanh một file bất kỳ trên hệ thống Linux. Chúng ta có cú pháp sau :

` loacte [tùy chọn] [name-file]`

Chương trình ` locate` có tên gọi là `mlocate`

Cú pháp cài đặt chương trình `locate` như sau:

- Đối với CentOS/RHEL

`yum -install -y mlocate`

- Đối với Debian/Ubuntu

`apt-get install -y mlocate`

Để cập nhật lại dữ liệu cho `locate` chúng ta chạy lệnh sau : `updatedb`.

## 15. Lệnh which và lệnh whereis

##### 15.1 Lệnh which

Lệnh ` which` xác định vị trí một chương trình trong đường dẫn của người dùng.

Một số cú pháp của lệnh `which`:

Tìm kiếm biến trong mội trường PATH và hiển thị vị trí của bất kỳ tệp thực thi phù hợp nào.

`which [executable]`

Nếu có nhiều tệp thực thi khớp,hiển thị tất cả:

` which -a [executable]`

##### 15.2 Lệnh whereis

Lệnh `whereis` rất hữu ích để tìm kiếm các trang nhị phân, nguồn các lệnh trong hệ thống Linux. Cú pháp như sau:

`whereis [tuyd chọn] [command]`

## 16 Lệnh type 

Lệnh `type` trong Linux được sử dụng để tìm hiểu một câu lệnh mà chúng ta sẽ diễn giải là một lệnh thích hợp, lệnh bên ngoài hoặc bí danh (alias) của shell hiện tại. Cú pháp của lệnh này là :

`type [tùy chọn] [command]`
