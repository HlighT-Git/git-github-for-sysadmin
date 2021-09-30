a# Table of Contents:



#             
<a name = "1"></a>
### 1. Hướng dẫn sử dụng chi tiết các file trong các folder:

<a name = "11"></a>
#### Header:
<a name = "111"></a>
- **ITPlib.hpp**: 
       Thư viện tự viết.
<a name = "112"></a>
- **Setup.hpp**: 
       Nơi chỉnh sửa chính về cả nội dung và số lượng của các file test case. Mặc định có 3 độ khó Easy, Medium, Hard, nếu cần thêm level có thể gỡ cmt và dùng thêm hàm NightMare đã có sẵn.
<a name = "12"></a>
#### Creator: Folder bao gồm code sinh input và output cho test case dựa trên solution-code. Có thể chạy tay từng cái một.
<a name = "13"></a>
#### Resources: Vai trò như tên, chứa tài nguyên hỗ trợ. Có 2 file cần chú ý đó là:
<a name = "131"></a>
- **NoteForAProblem.txt**: File này dùng để note lại các vấn đề mà người ra đề cần truyền đạt lại với người up đề. Yêu cầu **chỉ chỉnh sửa nội dung và không làm gì khác ngoài chỉnh sửa nội dung.**
<a name = "132"></a>
- **Template.docx**: File đã để sẵn form đề thi, yêu cầu **đưa đề thi đúng format vào đây và không làm gì khác**.
<a name = "14"></a>
- **Solutions**: Folder chứa solutions - các cách giải, các file được tùy chỉnh nhưng **code được sử dụng để sinh test sẽ giữ ở file `MainSolution.cpp`**.

- TimeChecker: Folder chứa file code đo và so sánh thời gian chạy của solutions. Có 2 mode là cleanMode và ngược lại. Nếu không sử dụng cleanMode, sau khi chạy Comparator.exe, trong folder sẽ có một folder Temp chứa các folder con, mỗi folder con này lại chứa test sinh out của từng solution, có thể dựa vào đây để xem các solution có đúng hoàn toàn hay không. Nếu dùng cleanMode, clean == true.

- Packager.py: python script để đóng gói, nó sẽ tự động zip 1 folder chứa:

       + Problem.docx (file Template.docx copy sang).
       + Note.txt (file NoteForAProblem.txt copy sang).
       + Setup.hpp (copy).
       + Solutions's folder.
       + Test cases's folder.
       
       =>     File zip của đề, nếu cần package và gửi đi thì chỉ cần file này là đủ.

- Generator.exe: File gánh team. Chỉ cần sửa file đề, file note, file Setup.hpp, sau đó chạy file này là đủ, mọi việc sẽ tự động.


ITPlib.hpp's Funtions (đa phần các funtion đều được viết theo dạng template nên không cần quá lo về kiểu dữ liệu):

- BigInt gần như đầy đủ operator.

- Một số hàm báo lỗi thực thi khi sinh test case.

- Random & Shuffle:
       
       + Random số nguyên.
       + Random số thực.
       + Random BigInt.
       + Random Unique Array: một vector không chứa phần tử trùng nhau theo thứ tự ngẫu nhiên.
       + Bộ Array Shuffle tráo ngẫu nhiên các phần tử trong mảng.

- Số nguyên tố:

       + Số nguyên tố thứ n. (1 < n < 5761455)
       + Kiểm tra số nguyên tố trong O(sqrt(n)/6).
       + List số nguyên tố theo serial (số thứ tự).
       + List số nguyên tố theo đoạn [L, R]. (R < 1e8)
       + Sàng Eratosthenes trong đoạn [L, R] với L, R có thể là số lớn.

- Palindrome (cấu trúc đối xứng):

       + Kiểm tra một object có đối xứng hay không.
       + Kiểm tra một array có đối xứng hay không.
       + Kiểm tra một STL Sequence Container có đối xứng hay không.

- Khác:

       + Kiểm tra số nguyên.
       + Kiểm tra số chính phương.
       + Phân tích thừa số nguyên tố.
       + Tìm list ước của một số.
       + Tìm số lượng ước của một số.


/**
     * @Modifier: HlighT.
     * @Last Date Modified: 29/09/2021.
    */
