## Hướng dẫn cho git

## "flight rules" là gì?

Một bản hướng dẫn cho phi hành gia(bây giờ lập trình viên sử dụng git)nói về nên làm gì khi mọi chuyện tồi tệ.

Flight Rules là kinh nghiệm xương máu được ghi chép vào sổ sách mà liệt kê,từng bước một,phải làm gì nếu X xảy ra và tại sao.
Về cơ bản, chúng là các quy trình vận hành tiêu chuẩn cụ thể theo từng kịch bản cụ thể. 

NASA đã thu thập những lôi lẫm,tai họa và giải pháp kẻ từ đầu năm 1960,khi mà Mercury-era ground teams bắt đầu thu thập  "lessons learned" vào một bản tóm tắt mà bây giờ hàng nghìn trường hợp còn mơ hồ từ hỏng động cơ và tới thất bại tới trục trặc máy tính. Và cách giải quyết của bọn họ

## Quy ước cho văn bản này


Vì mục đích rõ ràng, tất cả các ví dụ trong tài liệu này sử dụng tùy chỉnh bash để chỉ ra nhánh hiện tại và có hay không có các thay đổi theo giai đoạn Nhánh được đặt trong dấu ngoặc đơn và dấu * bên cạnh tên chi nhánh cho biết các thay đổi được tùy chỉnh.

Tất cả các lệnh sẽ hoạt động với phiên bản tối thiểu là 2.13.0. Ghé thăm website git để cập nhật phiên bản git của bạn.

## Mục lục được khởi tạo bằng DocToc

## Repositories

Tôi muốn tạo một Repository cục bộ

Tôi muốn sao lưu Repository từ bên ngoài

Thay đổi các Commit

Tôi vừa commit điều gì?

Tôi viết sai trong một tin nhắn commit

Tôi commit với tên bị sai và email đã định cấu hình

Tôi muốn xóa một file từ lần commit trước đó

Tôi muốn xóa commit lần gần nhất

Xóa commit tùy ý

Tôi thử đẩy commit đã sủa đổi lên một remote,nhưng nhận được thông báo lỗi

Tôi vô tình thực hiện khôi phục cài đặt và tôi muốn lấy lại những gì tôi đã thay đổi

Tôi vô tình commit và hợp nhất chúng với nhau

Tôi vô tình commit vầ đẩy lên file chứa dữ liệu nhạy cảm

## Staging

Tôi cần thêm nhãn thay đổi theo giai đoạn vào commit trước đó

Tôi muốn stage một phần của file mới nhưng không phải cả file

Tôi muốn thay đổi một file ở 2 commit khác nhau

Tôi muốn stage cái thay đổi chưa được stage của tôi và bỏ stage cái thay đổi đã được stage

Thay đổi chưa được stage

Tôi muốn rời thay đổi chưa được stage của tôi xang một branch mới

Tôi muốn rơi thay đổi chưa được stage của tôi xang một branch khác đã tồn tại

Tôi muốn loại bỏ những thay đổi cục bộ chưa được commit(stage và chưa được stage)

Tôi muốn loại bỏ cụ thể một thay đổi chưa được stage

Tôi muốn loại bỏ cụ thể một file chưa được stage

Tôi chỉ muốn loại bỏ  thay đổi cục bộ chưa được stage

Tôi muốn loại bỏ tất cả file untracked

Tôi muốn bỏ satge một file đã được stage

## Branches

Tôi muốn liệt kê tất cả các branch

Tạo một brach từ một commit

Tôi lấy nhầm/đẩy nhầm branch

Tôi muốn loại bỏ commit cục bộ để brach giốn cái trên server

Tôi commit vào master thay vì brach mới

Tôi muốn giữ cả file từ một ref-ish khác

Tôi đã commit vài lần trên cùng một brach mà nó nên ở trên branch khác

Tôi vô tình xóa branch của tôi

Tôi muốn xóa một branch

Tôi muốn xóa nhiều branch 

Tôi muốn đổi tôi một branch

Tôi muốn kiểm tra một branch bên ngoài mà người khác đang làm

Tôi muốn tạo một branch bên ngoài từ cái branch cục bộ

Tôi muốn đặt branch bên ngoài đồng bội với branch cục bộ của tôi

Tôi muốn đặt HEAD của tôi mặc định điều khiển theo brand

Tôi đã thực hiện thay đổi sai branch

## Rebasing và Merging

Tôi muốn quay lại thao tác rebase/merge

Tôi đã rebase, nhưng tôi không muốn ép push

Tôi cần kết hợp commit

Chiến lược an toàn nhất

Tôi chỉ muốn kết hợp các commit chưa được đồng bộ

Tôi cần hủy merge

Tôi cần cập nhập các commit trước đây từ branch của tôi.

Kiểm tra nếu toàn bộ commit trên branch đều merge

Có thể có vấn đề về tương tác với rebase

Màn hình rebase hiển thị 'noop'

Có xung đột

## Stash

Chỉnh sửa toàn bộ Stash

Tập tin cụ thể Stash

Stash với message

Chấp thuận một stash cụ thể từ danh sách

## Finding

Tôi muốn tìm một chuỗi trong bất kỳ commmit nào

Tôi muốn tìm theo tác giả / người commit

Tôi muốn một danh sách commit chứa những tập tin cụ thể

Tìm thẻ nơi mà commit được tham chiếu

## Submodules

Sao chép tất cả các mô-đun con

Xóa một mô-đun con

## Miscellaneous Objects

Khôi phục tập tin đã bị xóa

Xóa thẻ

Khôi phục lại thẻ đã bị xóa

Xóa Patch

Xuất tập tin dưới dạng zip

Đẩy một branch và thể có cùng tên

## Tệp theo dõi

Tôi muốn thay đổi cách viết hoa của tên tập tin mà không bị thay đổi nội dung của tập tin.

Tôi muốn ghi đè tập tin cục vộ khi đang kéo git về

Tôi muốn xóa một tập từ tin Git nhưng giữ toàn bộ tập tin lại

Tôi muốn hoàn tác tệp về bản sửa đổi trước

Tôi muốn liệt kê các thay đổi của một tệp cụ thể giữa các commit hoặc branches

Tôi muốn Git bỏ qua những thay đổi của một một tập tin.

## Configuration

Tôi muốn thêm tên riêng cho một số lệnh Git

Tôi muốn thêm một thư mục trống vào kho lưu trữ

Tôi muốn lưu tên người dùng và mật khẩu cho repository

Tôi muốn khiển Git bỏ qua các quyền và thay đổi của filemode

Tôi muốn cài đặt một người dùng cục bộ

Tôi muốn thêm màu cho dòng lệnh với Git

### Tôi không nghĩ rằng tôi làm sai.

## Những Resources khác

Sách

Hướng Dẫn

Script và Tools

GUI Clients

## Repositories

## Tôi muốn khowrt tạo một Repositories cục bộ

Để khởi tạo thư mục đã tồn tại dưới dạng Git repository

(my-folder) $ git init

## Tôi muốn sao lưu một repository từ xa.

Để sao lưu (coppy) một repository từ xa cần coppy url cho repository và khởi chạy: 

$ git clone [url]

Điều này sẽ lưu nó vào một thư mục có tên giống như repository từ xa. Hãy chắc chắn rằng bạn kết nối được tới máy chủ mà bạn đang sao lưu (Hầu hết các việc này là để đảm bảo máy tính bạn bạn đã kết nối với internet).

Để sao lưu vào một thư mục có tên khác tên repository mặc định:

$ git clone [url] name-of-new-folder


## Chỉnh sửa Commits

## Tôi vừa commit gì ?
 Giả sử bạn chỉ thực hiện các thay đổi một cách ngẫu nhiên với git commit -a và bạn không chắc chắn với nội dung thực sự của commit bạn vừa tạo ra là gì. Bạn có thể hiển thị cam kết mới nhất trên HEAD của bạn với : 
 
 (master)$ git show
 
 Hoặc
 
 $ git log -n1 -p
 
 Nếu bạn muốn xem một tập tin tại một commit cụ thể, bạn cũng có thể làm điều này (trong đó <commitid> là commit mà bạn quan tâm):
  
  $ git commit --amend --only
  
  Thao tác này sẽ mở trình soạn thảo văn bản mặc định của bạn, nơi bạn có thể chỉnh sửa tin nhắn. Mặt khác, bạn hoàn toàn có thể làm tất cả điều này với một lệnh:
  
  $ git commit --amend --only -m 'xxxxxxx'
  
  Nếu bạn đã đẩy tin nhắn lên, bạn có thể sửa đổi commit và ép đẩy lên, nhưng điều này không được khuyến khích.
  
  ## Tôi đã commit sai cấu hình tên và email
  
  Nếu đó là một commit đơn hãy sửa nó
  
  $ git commit --amend --no-edit --author "New Authorname <authoremail@mydomain.com>"
  
  Một cách khác để cấu hình chính xác cài đặt trong git config --global author.(name|email) và sử dụng:
  
  $ git commit --amend --reset-author --no-edit
  
  Nếu bạn cần thay đổi toàn bộ lịch sử hãy xem treang hướng dẫn cho git filter-branch.
  
  ## Tôi muốn xóa một file từ commit trước đó
  
  ĐỂ xóa các thay đổi cho một file từ commit trước làm theo hướng dẫn sau:
  
  $ git checkout HEAD^ myfile
  
$ git add myfile

$ git commit --amend --no-edit

Trong trường hợp tệp mới được thêm vào commit và bạn muốn xóa nó (từ sao lưu Git) hãy làm theo cách sau: 

$ git rm --cached myfile

$ git commit --amend --no-edit

Điều này đặc biệt hữu ích khi bạn có một bản thay đổi mới và bạn đã commit một tập tin không cần thiết sau đó đẩy lên git để cập nhập một bản thay đổi từ xa. Lựa chọn --no-edit được sử dụng để giữ thông tin commit đã tồn tại đó

## Tôi muốn xóa commit cuối cùng của tôi

Nếu bạn cần xóa các commit đã đươc push lên, bạn có thể sử dụng mục sau. Tuy nhiên nó sẽ không thể dảo ngược những thay đổi trong lịch sử của bạn, và lịch sử của bất kỳ ai khác đã kéo về từ repository trước đó. Nếu như bạn không chắc chắn bạn không nên thực hiện thao tác này. Chú ý đọc kỹ trước khi thực hiện thao tác:

 $ git reset HEAD^ --hard
 
$ git push --force-with-lease [remote] [branch]

Nếu bạn chưa đẩy code lên, hãy đặt lại Git về trạng thái trước khi bạn commit kết quả cuối cùng của mình (Trong khi vẫn giữ các thay đổi theo từng giai đoạn)

(my-branch*)$ git reset --soft HEAD@{1}

Điều này chỉ hoạt động nếu bạn chưa đẩy những bản cập nhập mới lên. nếu bạn đã đẩy những bản cập nhập đó điều này là điều an toàn duy nhất để khiến Git hoàn tác SHAofBadCommit. Diều này sẽ tạo ra một commit mới để hòa tác tất cả các thay đôi của cam kết trước đó. Hoặc , nếu branch bạn đã cập nhập là rebase-safe(Ví dụ: các nhà phát triển khác sẽ không có khả năng kéo được bản cập nhập mới của bạn về) bạn chỉ có thể sử dụng git push --force-with-lease . Để biết thêm hãy xem phần bên trên.

Xóa commit tùy ý

Cảnh báo tương tự áp dụng như trên. Đừng bao giờ làm điều này nếu không thực sự cần thiết.

$ git rebase --onto SHA1_OF_BAD_COMMIT^ SHA1_OF_BAD_COMMIT

$ git push --force-with-lease [remote] [branch]

Hoặc làm một rebase tương tác và loại bỏ các dòng (s) tương ứng với commit (s) mà bạn muốn thấy nó được xóa.

## Tôi đã cố gắng để đẩy commit của tôi tới một remote. Nhưng tôi nhận được một thông báo lỗi

! [rejected]        mybranch -> mybranch (non-fast-forward)

error: failed to push some refs to 'https://github.com/tanay1337/webmaker.org.git'

hint: Updates were rejected because the tip of your current branch is behind

hint: its remote counterpart. Integrate the remote changes (e.g.

hint: 'git pull ...') before pushing again.

hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Chú ý rằng như với rebasing (Xem bên dưới) ## sửa đổi commit cũ với một commit mới , vì vậy bạn cần đẩy những cập nhập mới (--force-with-lease) các thay đổi của bạn nếu bạn đã sửa dổi commit trước đó đến remote của bạn. Hãy chú ý trước khi  làm điều này - luôn đẩm bảo rằng bạn đã chỉ định cụ thể một branch nào đó.

(my-branch)$ git push origin mybranch --force-with-lease

Nói chung, tránh (## force pushing) . Tốt nhất là tạo và đẩy một commit mới thay vì sửa đổi force-pushing commit vì nó sẽ gây xung đột trong lịch sử source cho bất kỳ nhà phát triển nào khác đã tương tác với branch được đề cập hoặc bất kỳ chi nhánh con nào. --force-with-lease vẫn sẽ thất bại, nếu có đó cũng đang cùng làm việc trên cùng một branch với bạn, và những lần push của bạn sẽ ghi đè lên những thay đổi đó.

Nếu bạn chắc chắn rằng không ai đang làm việc trên cùng một branch hoặc bạn muốn cập nhật nhánh ngọn một cách vô điều kiện, bạn có thể sử dụng --force (-f), nhưng nói chung tránh được điều này là tốt nhất.

## Tôi đã vô tình đã khôi phục cài đặt gốc và tôi muốn những thay đổi của mình trở lại như cũ

Nếu bạn vô tình thực hiện lệnh git reset --hard, bạn vẫn có thể lấy lại những commit của mình bình thường, vì git lưu trữ nhật ký trong vài ngày.

Chỉ hợp lệ nếu những thao tác của bạn được sao lưu, tức là, được commit hoặc stashed. git reset --hard sẽ xóa các sửa đổi không được commit

(master)$ git reflog

Bạn sẽ thấy danh sách các commit trong quá khứ của mình và commit khôi phục. Chọn SHA của commit bạn muốn undo và cài đặt lại:
 
(master)$ git reset --hard SHA1234

Và bạn nên tối ưu hóa trước khi rời khỏi

## Tôi đã vô tình commit và đẩy merge

Nếu bạn vô tình hợp nhất một branch tính năng với nhánh phát triển chính trước khi nó đã sẵn sàng để được merge, bạn vẫn có thể hoàn tác việc merge. Nhưng có một điều lệ: Một merge commit có nhiều hơn một nhánh cha (thường là hai).

Dòng lệnh sử dụng:

(feature-branch)$ git revert -m 1 <commit>
  
trong đó tùy chọn -m 1 nói để chọn số nhánh cha 1 (nhánh mà merge đã được tạo) làm nhánh cha được khôi phục lại

Lưu ý: số nhánh cha không phải là số nhận dạng commit. Thay vào đó, một cam kết hợp nhất có một dòng Merge: 8e2ce2d 86ac2e7. Số nhánh cha là chỉ mục dựa trên 1 của nhánh cha mong muốn trên dòng này, số nhận dạng đầu tiên là số 1, số thứ hai là số 2, v.v.

## Tôi vô tình commit và đẩy các tệp chứa dữ liệu nhạy cảm lên git

Nếu bạn vô tình đẩy các tệp chứa dữ liệu nhạy cảm (mật khẩu, khóa, v.v.), bạn có thể sửa đổi commit trước đó. Hãy nhớ rằng một khi bạn đã đẩy một commit lên git, bạn nên xem xét bất kỳ dữ liệu nào nó chứa để bị xâm phạm. Các bước này có thể xóa dữ liệu nhạy cảm khỏi repo công khai hoặc bản sao cục bộ của bạn, nhưng bạn không thể xóa dữ liệu nhạy cảm khỏi bản sao được kéo về của người khác. Nếu bạn đã commit mật khẩu, hãy thay đổi mật khẩu ngay lập tức. Nếu bạn đã commit khóa, hãy tạo lại khóa đó ngay lập tức. Việc sửa đổi cam kết đã đẩy là không đủ, vì bất kỳ ai cũng có thể đã kéo cam kết ban đầu chứa dữ liệu nhạy cảm của bạn trong thời gian chờ đợi.

Nếu bạn đã chỉnh sửa tệp và xóa dữ liệu nhạy cảm, hãy chạy dòng lệnh dưới:

(feature-branch)$ git add edited_file

(feature-branch)$ git commit --amend --no-edit

(feature-branch)$ git push --force-with-lease origin [branch]

Nếu bạn muốn xóa toàn bộ tệp (nhưng giữ nguyên tệp cục bộ), hãy chạy dòng lệnh dưới: 

(feature-branch)$ git rm --cached sensitive_file

echo sensitive_file >> .gitignore

(feature-branch)$ git add .gitignore

(feature-branch)$ git commit --amend --no-edit

(feature-branch)$ git push --force-with-lease origin [branch]

Ngoài ra,hãy lưu trữ dữ liệu nhạy cảm của bạn trong các biến môi trường cục bộ.

Nếu bạn muốn xóa toàn bộ tệp (và không giữ nguyên tệp cục bộ), hãy chạy dòng lệnh:

(feature-branch)$ git rm sensitive_file

(feature-branch)$ git commit --amend --no-edit

(feature-branch)$ git push --force-with-lease origin [branch]

Nếu bạn đã thực hiện các commit khác trong thời gian chờ đợi (tức là dữ liệu nhạy cảm nằm trong commit trước những commit đó), bạn sẽ phải rebase.

## Staging

Tôi cần thêm các staged theo giai đoạn cho cam kết trước đó

(my-branch*)$ git commit --amend

Nếu thấy rằng bạn không muốn thay đổi thông báo commit, bạn có thể yêu cầu git sử dụng lại tiêu đề commit:

(my-branch*)$ git commit --amend -C HEAD
