===Quy trình thường gặp:

git switch -c ten-tinh-nang
Code, rồi add, rồi commit
git switch main, rồi git merge ten-tinh-nang
git push

====Xem tình trạng
bash
git status        # file nào đã sửa, file nào đã add
git log --oneline # xem lịch sử commit, mỗi commit một dòng
git diff          # xem chi tiết đã sửa dòng nào (bấm q để thoát)

git status là lệnh nên chạy nhiều nhất. Không chắc chuyện gì đang xảy ra thì chạy nó.

====Lưu và đẩy code

bash
git add .                     # add tất cả file đã sửa
git add App.js                # chỉ add một file
git commit -m "Them nut dang nhap"
git push

======Lấy code về

bash
git clone https://github.com/<user>/<repo>.git  # tải repo về máy lần đầu
git pull                                         # cập nhật code mới nhất từ GitHub

Làm nhóm thì nên git pull trước khi bắt đầu code mỗi ngày.

========IV. Nhánh (branch)

Nhánh giống như một bản nháp riêng: bạn thử tính năng mới mà không làm hỏng code chính (main).

bash
git branch                    # xem các nhánh, dấu * là nhánh đang đứng
git switch -c dang-nhap       # tạo nhánh mới tên "dang-nhap" và chuyển sang
git switch main               # quay về nhánh main
git merge dang-nhap           # (đang ở main) gộp code từ nhánh dang-nhap vào
git push -u origin dang-nhap  # đẩy nhánh mới lên GitHub

