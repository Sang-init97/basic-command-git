# Các lệnh cơ bản trong GIT

## git config
    - Git config là câu lệnh mà chúng ta phải thực thi đầu tiên cài đặt git lên máy. Câu lệnh này sẽ giúp các bạn thiết lập tên và email cá nhân của bạn, những thông tin này sẽ đính kèm trong mọi commit của bạn

    ví dụ:  
        - git config --global user.name "Your Name"
        - git config --global user.email "Your Email"

## git init 
    - Đây là câu lệnh đầu tiên khi chúng ta bắt đầu một dự án mới
    
    ví dụ:  
        - git init
        - git init <your respoitory name> // nếu muốn đặt tên cho repo với lệnh

## git clone
    - Câu lệnh này sẽ giúp chúng ta download một repository đã tồn tại sẵn trên khô lưu trữu (github, gitlab v.v) về máy

    ví dụ: - git clone <Your project URL>

## git add
    - Git add là câu lệnh giúp chúng ta thêm tất cả các file code mới mới hoặc các file code được chỉnh sửa vào repositor

    ví dụ: 
        - git add your_file_name // thêm 1 file vào staging area
        - git add * // thêm tất cả file (file mới hoặc file chỉnh sửa vào staging area)

## git commit 
    - Đây là câu lệnh được sử dụng phổ biến nhất, câu lệnh này sẽ giúp chúng ta lưu các thay đổi ở các file trong vùng staging area xuống repository.

    ví dụ: 
        - git commit -m "your useful commit change"
        - git commit -a -m "Ghi chú về commit" // -a giống như gọi add .
        - git commit --amend -m "Thông tin về commit" // Thay thế commit cuối bằng tham số --amend

## git status
    - Câu lệnh này cho phép bạn xem tình trạng hiện tại của mã nguồn như có bao nhiêu file được thêm mới hoặc chỉnh sửa.  Những file nào đang nằm trong vùng staging area hoặc đang nằm ngoài staging area.

    ví dụ: 
        - git status

## git branch
    - Trong một Git repository luôn luôn tồn tại nhiều nhánh riêng biệt dùng để triển khai một tính năng nào đó độc lập với các nhánh khác.

    ví dụ:
        - git branch // hiển thị các branch hiện có trong git
        - git branch <new_branch_name> <branch_origin> // tạo 1 branch mới từ branch origin
        - git checkout -b <branch_name> // tạo 1 branch mới và checkout sang branch mới
        - git check <branch_name> // di chuyển tới branch
        - git branch -d <branch_name> // để xóa branch hiện tại

## git remote
    - Nếu muốn lưu trữ repository này lên một dich vụ lưu trữu git từ xa nào đó chẳng hạn như gitlab, github thì các bạn cần phải sử dụng git remote để kết nối giữa chúng.

    ví dụ:
        - git remote add <shortname> <url> // git remote add origin URL

## git push 
    - Khi đã kết nối giữa local và dịch vụ lưu trữ git, chúng ta cần sử dụng lệnh git push để đồng bộ những thay đổi được commit trên local lên dich vụ lưu trữ.

    ví dụ:
        - git push -u <short_name> <your_branch_name> // git push -u origin feature_branch
        - git push --set-upstream origin <eature_branch> // Ngoài ra trước khi sử dụng git push các bạn nên cấu hình origin và upstream.

## git fetch 
    - Git được sử dụng để làm việc nhóm, quản lý mã nguồn. Ngoài những commit của bạn thì còn vô số commit khác của các thành viên khác trong team. Sử dụng git fetch sẽ giúp chúng ta cập nhật tất cả những thông tin mới như commit, branch

    ví dụ: 
        - git fetch

## git pull
    - Câu lệnh này sẽ download tất cả những nội dung (không chỉ là metadata như git fetch) từ dịch vụ lưu trữ xuống local repository.

    ví dụ:
        - git pull <remote_url> // git pull origin

## git log or git shortlog
    - Với câu lệnh git log các bạn có thể xem tất cả những commit trước đó được sắp xếp theo thứ tự commit gần nhất cho đến những commit cũ hơn.

    ví dụ:
        - git log
        - git shortlog

## git rm
    - Đôi lúc các bạn muốn xoá một file từ code base, trong trường hợp này các bạn có thể sử dụng git rm.

    ví dụ: 
        git rm <your file name>
## git merge
    - Git merge cho phép các bạn kết mã nguồn và những thay đổi trên một branch khác vào branch hiện tại.

    ví dụ:  
        - git merge <branch_name>

    - Câu lệnh này sẽ kết hợp những thay đổi trên branch có tên là <branch_name> vào branch hiện tại.   

## git rebase 
    - Git rebase tương tự như git merge, nó sẽ kết hợp 1 branch vào branch hiện tại với một ngoại lệ, git rebase sẽ ghi lại tất cả các lịch sử commit.

    ví dụ:  
        - git rebase <base> // base chính là vị trí mà commit sẽ forward ở đây

    
## git cherry pick
    - Git cherry-pick là một lệnh hữu ích. Đó là một lệnhcho phép bạn chọn bất kỳ commit nào từ một branch bất kỳ và áp dụng nó vào một branch hiện tại

    ví dụ:  
        - git cherry-pick <commit-hash>

## git tag 
    - Trong Git, các thẻ tag rất hữu ích và bạn có thể sử dụng chúng để quản lý bản phát hành. Bạn có thể coi thẻ Git giống như một nhánh sẽ không thay đổi. Nó quan trọng hơn đáng kể nếu bạn đang phát hành công khai

    ví dụ:  
        - git tag -a v1.0.0

## git diff     
    - Nếu các bạn muốn so sánh một file code nào thay đổi những gì trước khi commit thì các bạn có thể sử dụng

    ví dụ:  
        - git diff // Khi có sự thay đổi của thư mục làm việc mà chưa chỉ mục, thì có thể xem sự thay đổi của nó với commit cuối
        - git diff --staged // Kiểm tra sự thay đổi của index (staging) với commit cuối
        - git diff hash-commit1 hash-commit2 // Kiểm tra thay đổi giữa hai commit
        - git diff branch1 branch2 // kiểm tra sự thay đổi của 2 nhánh

## git reset
    - Khi đã thực hiện commit, commit đó chưa public (chưa đẩy lên Remote Repo bằng lệnh git push) thì bạn có thể hủy (undo) commit đó với hai trường hợp bằng lệnh git reset như sau

    ví dụ: 
                               HEAD~1
        - git reset --soft <commit/HEAD> // con trỏ HEAD sẽ chuyển về commit cha. Đồng thời những thay đổi của commit cuối được chuyển vào vùng staging nhằm để có cơ hội commit lại hoặc sửa đổi

        - git reset --hard HEAD~1 // hủy luôn mà không dưa vào trong staging
