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

Tôi muốn xóa các nhánh local đã bị xóa luồng trước đó

Tôi vô tình xóa branch của tôi

Tôi muốn xóa một branch

Tôi muốn xóa nhiều branch 

Tôi muốn đổi tên một branch

Tôi muốn kiểm tra một branch bên ngoài mà người khác đang làm

Tôi muốn tạo một branch bên ngoài từ cái branch cục bộ

Tôi muốn đặt branch bên ngoài đồng bội với branch cục bộ của tôi

Tôi muốn đặt HEAD của tôi mặc định điều khiển theo brand

Tôi đã thực hiện thay đổi sai branch

## Rebasing và Merging

Tôi muốn hoàn tác rebase/merge

Tôi đã rebase, nhưng tôi không muốn ép push

Tôi cần kết hợp commit

Chiến lược merge an toàn 

Tôi cần merge một nhánh vào một commit duy nhất

Tôi chỉ muốn kết hợp các commit chưa được đồng bộ

Tôi cần hủy merge

Tôi cần cập nhập các commit trước đây từ branch của tôi.

Kiểm tra nếu toàn bộ commit trên branch đều merge

Có thể có vấn đề về tương tác với rebase

Màn hình rebase hiển thị 'noop'

Có xung đột

## Stash

Chỉnh sửa toàn bộ Stash

Stash tập tin cụ thể 

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

### Tôi không biết tôi làm sai cái gì.

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

Nếu bạn biết sẵn rằng không muốn thay đổi thông báo commit, bạn có thể yêu cầu git sử dụng lại tiêu đề commit:

(my-branch*)$ git commit --amend -C HEAD

Tôi muốn stage một phần của file mới nhưng không phải cả file

Bình thường nếu bạn muốn stage một phần của file bạn sẽ chay:

$ git add --patch filename.x

-p sẽ hoạt động trong ngắn hạn. Việc này sẽ mở ra chế độ tương tác. Bạn sẽ có thể sử dụng tuỳ chọn s để cắt commit - tuy nhiên, nếu là file mới, bạn sẽ không có tuỳ chọn này. Để thêm một file mới, làm như sau:

$ git add -N filename.x

Sau đó bạn cần sử dụng tùy chọn e để chọn một cách thủ cônng cách dòng muốn thêm vào.Chạy git diff --cached hoặc git diff --staged sẽ chỉ cho bạn dòng nào bạn đã stage với các dòng vẫn lưu cục bộ

Tôi muốn thay đổi một file ở 2 commit khác nhau

git add sẽ thêm  toàn bộ file vào một commit git add -p sẽ cho phép tương tác chọn những thay đổi bạn muốn thêm.

Tôi muốn stage cái thay đổi chưa được stage của tôi và bỏ stage cái thay đổi đã được stage

Điều này khá khó.Điều tốt nhất mà tôi nghĩ ra là bạn nên stash những thay đổi chưa được stage.Rôi khởi động lại.Sau đó bật lại các chỉnh sửa được lưu trữ của bạn và thêm chúng.

$ git stash -k

$ git reset --hard

$ git stash pop

$ git add -A

Thay đổi chưa được stage

Tôi muốn rời thay đổi chưa được stage của tôi xang một branch mới

$ git checkout -b my-branch

Tôi muốn rơi thay đổi chưa được stage của tôi xang một branch khác đã tồn tại

$ git stash

$ git checkout my-branch

$ git stash pop

Tôi muốn loại bỏ những thay đổi cục bộ chưa được commit(stage và chưa được stage)

Nếu bạn muốn loại bỏ các cái đã stage cục bộ và những thay đổi chưa được stage bạn có thể làm thế này:

(my-branch)$ git reset --hard

# hoặc

(master)$ git checkout -f

Lệnh này sẽ bỏ stage tất cả những file mà bạn đã stage vơi git add:

$ git reset

Bạn cũng có thể hoàn tác các thay đổi không được commit đối với một tệp hoặc thư mục cụ thể:

$ git checkout [some_dir|file.txt]

Tuy nhiên,có một cách khác để hoàn tác tất cả các thay đổi không được cam kết (nhập dài hơn nhưng hoạt động từ bất kỳ thư mục con nào):

$ git reset --hard HEAD

Lệnh này sẽ xóa tất file ko track được cục bộ,nên chỉ những file track được còn

$ git clean -fd

-x sẽ xóa toàn bộ tất cả các tệp bị bỏ qua.

Tôi muốn loại bỏ cụ thể một thay đổi chưa được stage

Khi bạn loại một vài nhưng không phải tất cả các thay đổi trong bản sao làm việc của bạn.


Kiểm tra các thay đổi không mong muốn, giữ lại các thay đổi tốt.

$ git checkout -p

# Answer y to all of the snippets you want to drop

Một chiến lược khác bao gồm việc sủ dụng stash.Stash tất cả những thay đổi tốt,khởi động lại bản sao làm việc,gắn lại những thay đổi tốt

$ git stash -p

# Select all of the snippets you want to save

$ git reset --hard

$ git stash pop

Ngoài ra, hãy stash những thay đổi không mong muốn của bạn, và sau đó thả stash.

$ git stash -p

# Select all of the snippets you don't want to save

$ git stash drop

Tôi muốn loại bỏ cụ thể một file chưa được stage

Khi bạn muốn loại bỏ một file cụ thể trong bản sao làm việc

$ git checkout myFile

Ngoài ra ,để loại bỏ nhiều file trong bản sao làm việc,liệt kê tất cả chúng

$ git checkout myFirstFile mySecondFile

Tôi chỉ muốn loại bỏ thay đổi cục bộ chưa được stage

Khi bạn muốn loại bỏ tất cả những thay đổi cục bộ chưa được stage

$ git checkout .

Tôi muốn loại bỏ tất cả file không track được

Khi bạn muốn loại bỏ tất cả những file không track được

$ git clean -f

Tôi muốn bỏ satge một file đã được stage

Đôi khi, chúng ta có một hoặc nhiều file đã vô tình bị stage  và các tệp này chưa được commit trước đó. Để bỏ stage chúng:

$ git reset -- <filename>
 
Kết quả là bỏ stage file  và khiến chúng trông như là ko track được

# Branches

Tôi muốn liệt kê tất cả các branch

Liệt kê branch cục bộ

$ git branch

Liệt kê branch bên ngoài

$ git branch -r

Liệt kê tất cả các branch(cả cục bộ và bên ngoài)

$ git branch -a

Tạo một brach từ một commit

$ git checkout -b <branch> <SHA1_OF_COMMIT>
 
Tôi lấy nhầm/đẩy nhầm branch

Đây là một cơ hội khác để sư dụng git reflog để xem nơi HEAD của bạn chỉ tới trước khi kéo lỗi.

(master)$ git reflog

ab7555f HEAD@{0}: pull origin wrong-branch: Fast-forward

c5bc55a HEAD@{1}: checkout: checkout message goes here

Chỉ cần đặt lại branch của bạn trở lại commit mong muốn:

$ git reset --hard c5bc55a

Xong

Tôi muốn loại bỏ commit cục bộ để brach giốn cái trên server

Xác nhận rằng chưa đẩy thay đổi lên server

git status sẽ chỉ ra bao nhiêu commit của bạn đang ở phía trước ban đầu

(my-branch)$ git status

# On branch my-branch

# Your branch is ahead of 'origin/my-branch' by 2 commits.

#   (use "git push" to publish your local commits)

Một cách khác để thiết lập lại để phù hợp với ban đầu (để có giống như những gì trên điều khiển từ xa) là làm điều này:

(master)$ git reset --hard origin/my-branch

Tôi commit vào master thay vì brach mới

Tạo branch mới khi đang ở trong master

(master)$ git branch my-branch

Khởi động branch master về commit trước

(master)$ git reset --hard HEAD^

HEAD^ là viết tắt của HEAD^1 Nó đại diện cho cha đầu tiên của HEAD ,tương tự HEAD^2 đại diện cho cha thứ 2 của commit(merge có thêr có 2 cha)

Chú ý răng HEAD^2 không giống HEAD~2(Xem đường dẫn để biết thêm thông tin)

Ngoài ra nếu bạn không muốn sư dụng HEAD^ tìm ra commit hash nào mà bạn muốn đặt branch master  (git log sẽ làm được điều này). Sau đó đặt lại thành hash đó. git push sẽ đảm bảo rằng thay đổi này được phản ánh trên remote của bạn.

Lấy ví dụ nếu hash của commit mà master branch của bạn nên ở là a13b85e

(master)$ git reset --hard a13b85e
HEAD is now at a13b85e

Kiểm tra branch mới để tiếp tục làm việc:

(master)$ git checkout my-branch

Tôi muốn giữ cả file từ một ref-ish khác

Giả sử bạn có tăng đột biến mức độ làm việc (xem lưu ý), với hàng trăm thay đổi. Mọi thứ đang hoạt động. Bây giờ, bạn commit vào một branch khác để lưu công việc đó:

(solution)$ git add -A && git commit -m "Adding all changes from this spike into one big commit."

Khi bạn muốn đặt nó vào một branch(có thể feature, có thể develop), bạn quan tâm đến việc giữ toàn bộ file. Bạn muốn chia commit lớn của bạn thành những cái nhỏ hơn.

Giả sư bạn có

branch solution, với giải pháp của tăng đột biến của bạn. Phía trước develop.

branch develop, nơi bạn muốn thêm các thay đổi của bạn.

Bạn có thể giải quyết nó mang nội dung đến branch của bạn:

(develop)$ git checkout solution -- file1.txt

Việc này sẽ lấy nội dung của tập tin đó trong branch solution đến branch develop của bạn:

# On branch develop

# Your branch is up-to-date with 'origin/develop'.

# Changes to be committed:

#  (use "git reset HEAD <file>..." to unstage)
 
#

#        modified:   file1.txt

Sau đó, commit như bình thường.

Chú ý: Các giải pháp tăng đột biến được thực hiện để phân tích hoặc giải quyết vấn đề. Các giải pháp này được sử dụng để ước tính và loại bỏ sau khi mọi người hiểu rõ vấn đề. ~ Wikipedia.

Tôi đã commit vài lần trên cùng một brach mà nó nên ở trên branch khác

Giả sử bạn đang ở trên  master branch của bạn. Chạy git log, bạn thấy bạn đã thực hiện 2 commit:

(master)$ git log

commit e3851e817c451cc36f2e6f3049db528415e3c114

Author: Alex Lee <alexlee@example.com>

Date:   Tue Jul 22 15:39:27 2014 -0400

    Bug #21 - Added CSRF protection

commit 5ea51731d150f7ddc4a365437931cd8be3bf3131

Author: Alex Lee <alexlee@example.com>

Date:   Tue Jul 22 15:39:12 2014 -0400

    Bug #14 - Fixed spacing on title

commit a13b85e984171c6e2a1729bb061994525f626d14

Author: Aki Rose <akirose@example.com>

Date:   Tue Jul 21 01:12:48 2014 -0400

    First commit
    
Hãy để ý các hash commit cho mỗi lỗi (e3851e8 cho #21, 5ea5173 cho #14).  

Trước tiên, hãy đặt lại  master branch về commit chính xác (a13b85e):

(master)$ git reset --hard a13b85e

HEAD is now at a13b85e

Bây giờ, chúng ta có thể tạo ra một branch mới cho lỗi  #21:

(master)$ git checkout -b 21

(21)$

Bây giờ, hãy cherry-pick commit cho bug #21 ở trên dầu của branch. Điều này có ý nghĩa là chúng ta sẽ áp dụng commit đó, và chỉ commit đó, trực tiếp trên đầu của bất cứ head nào của chúng ta.

(21)$ git cherry-pick e3851e8

Tại thời điểm này, có khả năng là có thể có xung đột. Hãy xem phần There were conflicts trong phần tương tác rebasing trên để làm thế nào giải quyết xung đột.

Bây giờ hãy tạo một branch mới cho bug # 14, cũng dựa trên master

(21)$ git checkout master

(master)$ git checkout -b 14

(14)$

Và cuối cùng, hãy cherry-pick commit cho bug #14:

(14)$ git cherry-pick 5ea5173

Tôi muốn xóa các nhánh local đã bị xóa luồng trước đó

Khi bạn kết hợp một pull request trên GitHub, nó sẽ cho bạn tùy chọn để xóa branch đã merge trong fork của bạn. Nếu bạn không có kế hoạch tiếp tục làm việc trên branch, nó sạch hơn nếu xóa các bản sao local của branch vậy bạn sẽ không kết thúc lộn xộn lên checkout luồng làm việc của bạn với rất nhiều branch cũ.

$ git fetch -p upstream

trong đó upstream là remote bạn muốn fetch từ

Tôi vô tình xóa branch của tôi

Nếu bạn thường xuyên dẩy lên remote, bạn sẽ an toàn phần lớn thời gian. Nhưng đôi khi bạn có thể sẽ xóa các nhánh của bạn. Giả sử chúng ta tạo một branch và tạo một file mới:

(master)$ git checkout -b my-branch

(my-branch)$ git branch

(my-branch)$ touch foo.txt

(my-branch)$ ls

README.md foo.txt

Hãy thêm nó và commit.

(my-branch)$ git add .

(my-branch)$ git commit -m 'foo.txt added'

(my-branch)$ foo.txt added

 1 files changed, 1 insertions(+)
 
 create mode 100644 foo.txt
 
(my-branch)$ git log

commit 4e3cd85a670ced7cc17a2b5d8d3d809ac88d5012

Author: siemiatj <siemiatj@example.com>

Date:   Wed Jul 30 00:34:10 2014 +0200

    foo.txt added

commit 69204cdf0acbab201619d95ad8295928e7f411d5

Author: Kate Hudson <katehudson@example.com>

Date:   Tue Jul 29 13:14:46 2014 -0400

    Fixes #6: Force pushing after amending commits
    
Bây giờ chúng ta chuyển về master và 'vô tình' xóa branch của chúng ta

(my-branch)$ git checkout master

Switched to branch 'master'

Your branch is up-to-date with 'origin/master'.

(master)$ git branch -D my-branch

Deleted branch my-branch (was 4e3cd85).

(master)$ echo oh noes, deleted my branch!

oh noes, deleted my branch!

Tại thời điểm này, bạn chắc đã quen với 'reflog', một logger được nâng cấp. Nó lưu trữ lịch sử của tất cả các hành động trong repo.

(master)$ git reflog

69204cd HEAD@{0}: checkout: moving from my-branch to master

4e3cd85 HEAD@{1}: commit: foo.txt added

69204cd HEAD@{2}: checkout: moving from master to my-branch

Như bạn có thể thấy chúng ta đã có commit hash từ branch đã xóa của chúng ta. Hãy xem liệu chúng ta có thể khôi phục branch hay không?

(master)$ git checkout -b my-branch-help

Switched to a new branch 'my-branch-help'

(my-branch-help)$ git reset --hard 4e3cd85

HEAD is now at 4e3cd85 foo.txt added

(my-branch-help)$ ls

README.md foo.txt

Xem đây!chúng ta đã lấy lại được file đã bị xóa git reflog cũng vô cùng hữu dụng khi rebase sai lầm lớn. 

Tôi muốn xóa một branch

Để xoá một branch bên ngoài:

(master)$ git push origin --delete my-branch

Bạn cũng có thể viết :

(master)$ git push origin :my-branch

Để xoá một branch cục bộ:

(master)$ git branch -d my-branch

Để xoá một branch local chưa được merge đến branch hiện tại hoặc một upstream:

(master)$ git branch -D my-branch

Tôi muốn xóa nhiều branch

Giả sử bạn muốn xoá tất cả branch bắt đầu với fix/:

(master)$ git branch | grep 'fix/' | xargs git branch -d

Tôi muốn đổi tên một branch

Để đổi tên branch hiện tại(cục bộ):

(master)$ git branch -m new-name

Để đổi tên branch khác(cục bộ):

(master)$ git branch -m old-name new-name

Tôi muốn kiểm tra một branch bên ngoài mà người khác đang làm

Đầu tiên, fetch tất cả nhánh từ remote:

(master)$ git fetch --all

Giả sử bạn muốn kiêm tra  daves từ remote.

(master)$ git checkout --track origin/daves

Branch daves set up to track remote branch daves from origin.

Switched to a new branch 'daves'

(--track is shorthand for git checkout -b [branch] [remotename]/[branch])

Điều này sẽ cung cấp cho bạn một bản sao cục bộ của branch daves, và mọi cập nhật đã được push cũng sẽ được hiển thị từ remote.

Tôi muốn tạo một branch bên ngoài từ cái branch cục bộ

$ git push <remote> HEAD
 
Nếu bạn cũng muốn đặt branch từ remote như upstream cho nhánh hiện tại, sử dụng cái này thay thế:

$ git push -u <remote> HEAD
 
Với chế độ upstream và simple (mặc định trong Git 2.0) của cấu hình push.default, command sau sẽ push branch hiện tại liên quan đến branch bên ngoài được đăng ký trước đó với -u:

$ git push

Các hành động khác của git push được mô tả trong doc of push.default.

Tôi muốn đặt branch bên ngoài đồng bội với branch cục bộ của tôi

Bạn có thể thiết lập một branch bên ngoài như upstream cho branch cục bộ hiện tại bằng cách sử dụng:

$ git branch --set-upstream-to [remotename]/[branch]

# or, using the shorthand:

$ git branch -u [remotename]/[branch]

Để thiết lập branch upstream bên ngoài cho branch cục bộ khác:

$ git branch -u [remotename]/[branch] [local-branch]

Tôi muốn đặt HEAD của tôi mặc định điều khiển theo brand

Bằng cách kiểm tra các branch bên ngoài của bạn, bạn có thể thấy các branch bên ngoài mà HEAD của bạn đang theo dõi. Trong một số trường hợp, đây không phải là branch mong muốn.

$ git branch -r

  origin/HEAD -> origin/gh-pages
  
  origin/master

Để thay đổi origin/HEAD để theo dõi origin/master, bạn có thể chạy command này:

$ git remote set-head origin --auto

origin/HEAD set to master

Tôi đã thực hiện thay đổi sai branch

Bạn đã thực hiện các thay đổi chưa được commit và nhận ra bạn đang ở sai branch. Stash các thay đổi và apply chúng vào branch bạn muốn:

(wrong_branch)$ git stash

(wrong_branch)$ git checkout <correct_branch>

(correct_branch)$ git stash apply

## Rebasing và Merging

Tôi muốn hoàn tác rebase/merge

Bạn có thể đã merge hoặc rebase branch hiện tại của bạn với một branch sai hoặc bạn không thể tìm ra cách hoàn thành quá trình rebase/merge. Git lưu con trỏ original HEAD trong một biến được gọi là ORIG_HEAD trước khi làm các hành động nguy hiểm, vì vậy nó giống như khôi phục branch ở một trạng thái trước khi rebase/merge.

(my-branch)$ git reset --hard ORIG_HEAD

Tôi đã rebase, nhưng tôi không muốn ép push

Không may thay, bạn bắt buộc phải push, nếu bạn muốn những thay đổi đó được ánh xạ trên brach bên ngoài. Điều này là do bạn đã thay đổi lịch sử. Brach bên ngoài sẽ không chấp nhận thay đổi trừ khi bạn ép push. Đây là một trong những lý do chính khiến nhiều người sử dụng một luồng merge, thay vì một luồng rebasing - các nhóm lớn có thể gặp rắc rối với các developer bắt buộc push. Sử dụng điều này một cách thận trọng. Một cách an toàn hơn để sử dụng rebase không phải là để ánh xạ các thay đổi của bạn trên brach bên ngoài, và thay vào đó thực hiện các thao tác sau:

(master)$ git checkout my-branch

(my-branch)$ git rebase -i master

(my-branch)$ git checkout master

(master)$ git merge --ff-only my-branch

Để biết thêm,xem this SO thread.

Tôi cần kết hợp commit

Giả sử bạn đang làm việc trong một branch là / sẽ trở thành một pull-request đối ngược với master. Trong trường hợp đơn giản nhất tất cả những gì bạn muốn làm là kết hợp tất cả các commit thành một commit và bạn không quan tâm đến timestamps commit, bạn có thể đặt lại và commit lại. Đảm bảo rằng master branch được cập nhật và tất cả các thay đổi của bạn được commit, sau đó:

(my-branch)$ git reset --soft master

(my-branch)$ git commit -am "New awesome feature"

Nếu bạn muốn kiểm soát nhiều hơn, và cũng để bảo vệ timestamp, bạn cần phải làm một vài thứ được gọi là một tương tác rebase:

(my-branch)$ git rebase -i master

Nếu bạn không làm việc với một branch khác, bạn phải rebase liên quan tới HEAD của bạn. Nếu bạn muốn squash 2 commit cuối,lấy ví dụ bạn sẽ phải rebase lại HEAD~2. Cho 3 commit cuối, HEAD~3,...

(master)$ git rebase -i HEAD~2

Sau khi bạn chạy lệnh tương tác rebase, bạn sẽ thấy một cái gì đấy như thế này trong trình soạn thảo của bạn:

pick a9c8a1d Some refactoring
pick 01b2fd8 New awesome feature
pick b729ad5 fixup
pick e3851e8 another fix

# Rebase 8074d12..b729ad5 onto 8074d12
#
# Commands:
#  p, pick = use commit
#  r, reword = use commit, but edit the commit message
#  e, edit = use commit, but stop for amending
#  s, squash = use commit, but meld into previous commit
#  f, fixup = like "squash", but discard this commit's log message
#  x, exec = run command (the rest of the line) using shell
#
# These lines can be re-ordered; they are executed from top to bottom.
#
# If you remove a line here THAT COMMIT WILL BE LOST.
#
# However, if you remove everything, the rebase will be aborted.
#
# Note that empty commits are commented out

Tất cả những dòng bắt đầu bằng một # là các comment, chúng sẽ không ảnh hưởng đến rebase của bạn.

Sau đó bạn thay thể câu lệnh pick với những thứ trong danh sách trên, và bạn cũng có thể loại bỏ các commit bằng cách xoá các dòng tương ứng.

Ví dụ, nếu bạn khômg muốn làm gì commit cũ nhất(đầu tiên) và kết hợp  tất cả các commit sau với commit cũ thứ 2, bạn nên chỉnh sửa chữ cái bên cạnh mỗi commit ngoại trừ chữ cái đầu tiên và chữ cái thứ hai f:

pick a9c8a1d Some refactoring

pick 01b2fd8 New awesome feature

f b729ad5 fixup

f e3851e8 another fix

Nếu bạn muốn kết hợp các commit và đổi tên commit, bạn nên thêm một chữ cái r bên cạnh commit thứ 2 hay đơn giản sử dụng s thay vì f:

pick a9c8a1d Some refactoring

pick 01b2fd8 New awesome feature

s b729ad5 fixup

s e3851e8 another fix

Bạn có thể đổi tên commit sau đó trong đoạn text bật lên.

Newer, awesomer features

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
# rebase in progress; onto 8074d12
# You are currently editing a commit while rebasing branch 'master' on '8074d12'.
#
# Changes to be committed:
#   modified:   README.md
#

Nếu mọi thứ thành công, bạn sẽ thấy một cái gì đó như thế này:

(master)$ Successfully rebased and updated refs/heads/master.

Chiến lược merge an toàn 

--no-commit thực hiện merge nhưng giả vờ hợp nhất không thành công và không tự động, cho phép người dùng có cơ hội kiểm tra và tinh chỉnh thêm kết quả merge trước khi commit. no-ff duy trì bằng chứng rằng một branch tính năng đã từng tồn tại, giữ cho lịch sử dự án nhất quán.

(master)$ git merge --no-ff --no-commit my-branch

Tôi cần merge một nhánh vào một commit duy nhất

(master)$ git merge --squash my-branch

Tôi chỉ muốn kết hợp các commit chưa được đồng bộ

Đôi khi bạn có một số công việc đang tiến hành commit mà bạn muốn kết hợp trước khi bạn đẩy chúng lên upstream. Bạn không muốn vô tình kết hợp bất kỳ commit nào đã được push lên upstream vì một người khác có thể đã thực hiện các commit tham chiếu đến chúng.

(master)$ git rebase -i @{u}

Điều này sẽ làm một interactive rebase mà chỉ liệt kê các commit mà bạn chưa push, vì vậy nó sẽ an toàn để reorder/fix/squash bất cứ điều gì trong danh sách

Tôi cần hủy merge

Đôi khi việc merge có thể gây ra sự cố trong một số file nhất định, trong những trường hợp đó, chúng ta có thể sử dụng tùy chọn abort để hủy bỏ quá trình giải quyết xung đột hiện tại và cố gắng xây dựng lại trạng thái merge trước.

(my-branch)$ git merge --abort

Lệnh này có thê sử dụng từ phiên bản Git >= 1.7.4

Tôi cần cập nhập các commit trước đây từ branch của tôi.

Giả sử tôi có một  master branch, một branch feature-1 tách nhánh từ master và một branch feature-2 tách nhánh từ feature-1. Nếu tôi thực hiện commit đối với feature-1, thì commit của feature-2 không còn chính xác nữa (nó phải là phần đầu của feature-1, vì chúng ta đã phân nhánh nó). Chúng ta có thể sửa điều này với git rebase --onto.

(feature-2)$ git rebase --onto feature-1 <the first commit in your feature-2 branch that you don't want to bring along> feature-2

Điều này giúp trong các trường hợp khó nơi bạn có thể có một feature được xây dựng trên một feature khác chưa được merge và một bugfix trên branch feature-1 cần được phản ánh trong branch feature-2 của bạn.

Kiểm tra nếu toàn bộ commit trên branch đều merge

Để kiểm cháu tất cả commit trên một branch được merge vào branch khác, bạn nên diff giữa các head (hoặc mọi commit) của những branch đó:

(master)$ git log --graph --left-right --cherry-pick --oneline HEAD...feature/120-on-scroll

Việc này sẽ cho bạn biết nếu bất kỳ commit trong một nhưng không phải là branch khác, và sẽ cung cấp cho bạn một danh sách của bất kỳ nonshared giữa các branch. Một lựa chọn khác là làm điều này:

(master)$ git log master ^feature/120-on-scroll --no-merges

Có thể có vấn đề về tương tác với rebase

Màn hình chỉnh sửa rebase cho biết 'noop'

Nếu bạn thấy điều này:

noop

Điều này có nghĩa bạn đang cố rebase lại một branch mà là một commit giống hệt nhau hoặc là ahead của branch hiện tại. Bạn có thể thử:

đảm bảo  master branch của bạn là nơi nó cần

rebase lại HEAD~2 hoặc sớm hơn

Có một vài xung đột

Nếu bạn không thể hoàn tất thành công việc rebase, bạn có thể phải giải quyết xung đột.

Đầu tiên chạy git status để xem tệp nào có xung đột giữa chúng:

(my-branch)$ git status

On branch my-branch

Changes not staged for commit:

  (use "git add <file>..." to update what will be committed)
 
  (use "git checkout -- <file>..." to discard changes in working directory)

  both modified:   README.md

Trong ví dụ này,, README.md có xung đột. Mở tệp đó và tìm kiếm những điều sau:

   <<<<<<< HEAD
   some code
   =========
   some code
   >>>>>>> new-commit
   
Bạn sẽ cần phải giải quyết sự khác biệt giữa code đã được thêm vào trong commit mới của bạn (trong ví dụ, mọi thứ từ dòng ở giữa new-commit) và HEAD của bạn.

Nếu bạn muốn giữ phiên bản code của một nhánh, bạn có thể sử dụng --ours hoặc --theirs:

(master*)$ git checkout --ours README.md

Khi đang merge, sử dụng --ours để giữa các thay đổi từ branch cục bộ, hoặc --theirs để giữ các thay đổi từ branch khác.

Khi đang rebase, sử dụng --theirs để giữ các thay đổi từ branch cục bộ, hoặc --ours để giữ các thay đổi từ branch khác. Để hiểu thêm về sự hoán đổi này, hãy xem this note in the Git documentation.

Nếu việc merge phức tạp hơn, bạn có thể sử dụng trình chỉnh sửa khác biệt trực quan:

(master*)$ git mergetool -t opendiff

Sau khi bạn đã giải quyết tất cả xung đột và đã kiểm tra code của mình, git add các file đã thay đổi và sau đó tiếp tục rebase với git rebase --continue

(my-branch)$ git add README.md

(my-branch)$ git rebase --continue

Nếu sau khi giải quyết tất cả các xung đột bạn kết thúc bằng một cây giống hệt với cái trước khi thực hiện, bạn cần git rebase --skip thay thế.

Nếu bất kỳ lúc nào bạn muốn dừng toàn bộ quá trình rebase và quay trở lại trạng thái ban đầu nhánh của bạn, bạn có thể làm như thế này:

(my-branch)$ git rebase --abort

## Stash

Chỉnh sửa toàn bộ Stash

Để stash tất cả các chỉnh sửa trong thư mục làm việc

$ git stash

Nếu bạn cũng muốn stash các file chưa được track, sử dụng tuỳ chọn -u.

$ git stash -u

Stash tập tin cụ thể 

Để stash chỉ một file từ thư mục làm việc

$ git stash push working-directory-path/filename.ext

Để stash nhièu file từ thư mục làm việc

$ git stash push working-directory-path/filename1.ext working-directory-path/filename2.ext

Stash với message

$ git stash save <message>
 
Chấp thuận một stash cụ thể từ danh sách

Đầu tiên kiểm tra danh sách các stash với message sử dụng

$ git stash list

Sau đó apply một stash cụ thể từ danh sách sử dụng

$ git stash apply "stash@{n}"

Ở đây, 'n' cho biết vị trí của stash trong stack. Stash trên cùng sẽ là vị trí 0.

## Finding

Tôi muốn tìm một chuỗi trong bất kỳ commmit nào

Để tìm một chuỗi nhất định được cho vào trong bất kỳ commit nào, bạn có thể sử dụng cấu trúc sau:

$ git log -S "string to find"

Các thông số chung:

--source có nghĩa là hiển thị tên ref được đưa ra trên dòng lệnh mà mỗi lần commit đã đạt được.

--all nghĩa là bắt đầu từ mọi nhánhmeans to start from every branch.

--reverse in theo thứ tự ngược lại, nó có nghĩa là sẽ hiển thị commit đầu tiên đã thực hiện thay đổi.

Tôi muốn tìm theo tác giả / người commit

Tìm tất cả commit từ tác giả hoặc người commit bạn có thể sử dụng:

$ git log --author=<name or email>
 
$ git log --committer=<name or email>
 
Nhớ trong đầu rằng tác giả và người commit không giống nhau. --author là người ban đầu đã viết code; mặt khác, --committer, là người đã commit code thay mặt tác giả gốc.

Tôi muốn một danh sách commit chứa những file cụ thể

Để tìm tất cả các commit chưa một file cụ thể bạn có thể sử dụng:

$ git log -- <path to file>
 
Bạn thường sẽ chỉ định một đường dẫn chính xác, nhưng bạn cũng có thể sử dụng các ký tự đại diện trong đường dẫn và tên tệp:

$ git log -- **/*.js

Trong khi sử dụng ký tự đại diện, nó hữu ích để thông báo --name-status xem danh sách các tệp đã commit:

$ git log --name-status -- **/*.js

Tìm thẻ nơi mà commit được tham chiếu

Để tìm tất cả các tag có chứa một commit cụ thể

$ git tag --contains <commitid>
 
## Submodules

Sao chép tất cả các mô-đun con

$ git clone --recursive git://github.com/foo/bar.git

Nếu đã clone:

$ git submodule update --init --recursive

Xóa một mô-đun con

Tạo một submodule là khá nhanh, nhưng xóa chúng không nhanh như vậy. Các lệnh bạn cần là:

$ git submodule deinit submodulename

$ git rm submodulename

$ git rm --cached submodulename

$ rm -rf .git/modules/submodulename

## Miscellaneous Objects

Khôi phục file đã bị xóa

Đầu tiên tìm commit nơi mà lần cuối file tồn tại:

$ git rev-list -n 1 HEAD -- filename

Sau đó kiểm tra file:

git checkout deletingcommitid^ -- filename

Xóa thẻ

$ git tag -d <tag_name>

$ git push <remote> :refs/tags/<tag_name>
 
Khôi phục lại thẻ đã bị xóa

Nếu bạn muốn khôi phục thẻ đã bị xóa, bạn có thể làm được vậy bằng cách làm theo các bước sau: Trước tiên, bạn cần phải tìm thẻ không thể truy cập

$ git fsck --unreachable | grep tag

Ghi lại mã hash của tag. Sau đó, khôi phục thẻ đã xóa theo cách sau, sử git update-ref:

$ git update-ref refs/tags/<tag_name> <hash>
 
Thẻ của bạn bây giờ đã được khôi phục.

Xóa Patch

Nếu ai đó đã gửi cho bạn một pull request trên GitHub, nhưng sau đó đã xoá chúng trên fork gốc, bạn sẽ không thể clone repository của họ hoặc sử dụng git am như .diff, .patch url không khả dụng. Nhưng bạn có thể kiểm tra chính PR bằng cách sử dụng GitHub's special refs. Để fetch nội dung của PR#1 vào một branch được gọi là pr_1:

$ git fetch origin refs/pull/1/head:pr_1

From github.com:foo/bar

 * [new ref]         refs/pull/1/head -> pr_1
 
 Xuất tập tin dưới dạng zip
 
 $ git archive --format zip --output /full/path/to/zipfile.zip master
 
Đẩy một branch và thể có cùng tên
 
Nếu có một thẻ trên một remote repository mà có tên giống với một branch bạn sẽ gặp phải lỗi khi cố push nhanh với một commad chuẩn $ git push <remote> <branch>.

$ git push origin <branch>
 
error: dst refspec same matches more than one.

error: failed to push some refs to '<git server>'
 
Sửa lỗi này bằng cách chỉ định bạn muốn đẩy tham chiếu head.

$ git push origin refs/heads/<branch-name>

Nếu bạn muốn đẩy một the vào một repository từ remote có cùng tên với một branch, bạn có thể sử dụng một lệnh tương tự.

$ git push origin refs/tags/<tag-name>

Tracking các file

Tôi muốn thay đổi cách viết hoa của tên tệp mà không thay đổi nội dung của tệp

(master)$ git mv --force myfile MyFile

Tôi muốn ghi đè lên các tệp cục bộ khi thực hiện lệnh git pull

(master)$ git fetch --all

(master)$ git reset --hard origin/master

Tôi muốn xóa một tệp khỏi Git nhưng vẫn giữ tệp

(master)$ git rm --cached log.txt

Tôi muốn revert tệp về bản sửa đổi cụ thể

Giả sử mã hash của commit bạn muốn c5f567:

(master)$ git checkout c5f567 -- file1/to/restore file2/to/restore

Nếu bạn muốn revert các thay đổi được thực hiện chỉ 1 commit trước c5f567, vượt qua commit hash như c5f567~1:

(master)$ git checkout c5f567~1 -- file1/to/restore file2/to/restore

Tôi muốn liệt kê các thay đổi của một tệp cụ thể giữa các commit hoặc các branch

Giả sử bạn muốn so sánh commit cuối cùng với tệp từ commit c5f567:

$ git diff HEAD:path_to_file/file c5f567:path_to_file/file

Tương tự cho các branch khác:

$ git diff master:path_to_file/file staging:path_to_file/file

Tôi muốn Git bỏ qua những thay đổi đối với một tệp cụ thể

Điều này hoạt động tốt cho các mẫu cấu hình hoặc các tệp khác yêu cầu thêm thông tin đăng nhập cục bộ mà không được commit

$ git update-index --assume-unchanged file-to-ignore

Lưu ý rằng điều này không xóa tệp khỏi kiểm soát source - nó chỉ bị bỏ qua cục bộ. Để hoàn tác thao tác này và yêu cầu Git lưu ý các thay đổi một lần nữa, điều này sẽ xóa ignore flag:

$ git update-index --no-assume-unchanged file-to-stop-ignoring

## Cấu hình
Tôi muốn thêm bí danh cho một số lệnh Git

Trên OS X và Linux, file cấu hình git được lưu trong ~/.gitconfig. Tôi đã thêm một số bí danh mẫu mà tôi sử dụng làm shortcut (và một số lỗi chính tả phổ biến của tôi) trong phần [alias] được hiển thị như dưới đây:

[alias]
    a = add
    amend = commit --amend
    c = commit
    ca = commit --amend
    ci = commit -a
    co = checkout
    d = diff
    dc = diff --changed
    ds = diff --staged
    extend = commit --amend -C HEAD
    f = fetch
    loll = log --graph --decorate --pretty=oneline --abbrev-commit
    m = merge
    one = log --pretty=oneline
    outstanding = rebase -i @{u}
    reword = commit --amend --only
    s = status
    unpushed = log @{u}
    wc = whatchanged
    wip = rebase -i @{u}
    zap = fetch -p
    
Tôi muốn thêm một thư mục trống vào repository của tôi

Bạn không thể! Git không hỗ trợ điều này, nhưng có một cách hack. Bạn có thể tạo tệp .gitignore trong thư mục với các nội dung sau:

 # Ignore everything in this directory
 *
 # Except this file

 !.gitignore
 
Một quy ước chung khác là tạo một tệp trống trong thư mục có tiêu đề .gitkeep.

$ mkdir mydir

$ touch mydir/.gitkeep

Bạn cũng có thể đặt tên tệp là .keep, trong trường hợp dòng thứ hai ở trên sẽ touch mydir/.keep

Tôi muốn cache một username và password cho một repository

Bạn có thể có một repository yêu cầu xác thực. Trong trường hợp này bạn có thể cache một username và password vì vậy bạn không phải nhập nó vào mỗi lần push / pull. Việc xác thực có thể làm điều này cho bạn.

$ git config --global credential.helper cache

# Set git to use the credential memory cache

$ git config --global credential.helper 'cache --timeout=3600'

# Set the cache to timeout after 1 hour (setting is in seconds)

Tôi muốn làm cho Git bỏ qua các quyền và thay đổi về filemode

$ git config core.fileMode false

Nếu bạn muốn đặt hành vi này là hành vi mặc định cho người dùng đã đăng nhập, thì hãy sử dụng:

$ git config --global core.fileMode false

Tôi muốn đặt user toàn cục

Để cấu hình thông tin người dùng được sử dụng trên tất cả các repository cục bộ và để đặt tên có thể nhận dạng khi xem lại phiên bản lịch sử:

$ git config --global user.name “[firstname lastname]”

Để đặt địa chỉ email sẽ được liên kết với mỗi điểm đánh dấu lịch sử:

git config --global user.email “[valid-email]”

Tôi muốn thêm màu cho command Git

Để thiết lập màu command tự động cho Git để dễ dàng xem lại:

$ git config --global color.ui auto

Tôi không biết mình đã làm gì sai
Vì vậy, bạn đang sai - bạn reset vài thứ, hoặc bạn merge sai branch, hoặc bạn ép push và bây giờ bạn không thể tìm thấy các commit của bạn. Bạn biết là tại một số thời điểm, bạn đã làm tốt, và bạn muốn quay trở lại trạng thái bạn đang ở đó.

Đây là những gì git reflog cho. reflog theo dõi bất kỳ thay đổi nào đối với mẹo của nhánh, ngay cả khi mẹo đó không được tham chiếu bởi nhánh hoặc tag. Về cơ bản, mỗi lần HEAD thay đổi, một mục mới được thêm vào reflog. Điều này chỉ hoạt động đối với các repository cục bộ, thật đáng buồn, và nó chỉ theo dõi các chuyển động (ví dụ: không thay đổi một tệp không được ghi ở bất kỳ đâu).

(master)$ git reflog

0a2e358 HEAD@{0}: reset: moving to HEAD~2

0254ea7 HEAD@{1}: checkout: moving from 2.2 to master

c10f740 HEAD@{2}: checkout: moving from master to 2.2

Các reflog ở trên cho thấy một checkout từ master đến branch 2.2 và trở lại. Từ đó, có một thiết lập cứng để một commit cũ hơn. Hoạt động mới nhất được thể hiện ở đầu được gắn nhãn HEAD@{0}.

Nếu nó chỉ ra rằng bạn vô tình di chuyển trở lại, các reflog sẽ chứa commit master chỉ đến (0254ea7) trước khi bạn vô tình giảm 2 commit

$ git reset --hard 0254ea7

Sử dụng git reset sau đó nó có thể thay đổi master trở về commit trước đó. Điều này cung cấp sự an toàn trong trường hợp lịch sử đã vô tình thay đổi.

















