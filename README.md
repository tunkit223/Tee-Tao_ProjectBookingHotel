# Tee-Tao_ProjectBookingHotel
 
Cách xử lí code trên github:

git checkout -b "Tên nhánh": để tạo nhánh mới

git branch: để kiểm tra xem mình đang ở nhánh nào

Quy trình trước khi code thêm vào dự án:

Bước 1: git checkout "Tên nhánh mình muốn làm việc ở đó"

Bước 2: git pull origin main (lấy những thay đổi mới nhất trên main)

Bước 3: bắt đầu code

Bước 4: git add backend/ (frontend/): để thêm những gì mình code vào staging chuẩn bị cho việc commit

Bước 5: git commit -m "Thông tin những thay đổi khi code": đẩy commit code của mình

Bước 6: git push origin Tên nhánh mình muốn đẩy code lên: để đẩy code lên pull request rồi vào github merge.

Bước 7: vào github sau đó kiểm tra có thể merge thì merge

Quy trình khi code trên dự án là A->B->C còn code của mình là A->B->D nhưng D chưa commit thì:

Bước 1: git stash (để lưu các thay đổi trên nhánh mình đang làm việc)

Bước 2: git pull origin main 

Bước 3: git stash pop (để lấy những code mình đã thay đổi ra, đồng thời xử lí conflict)

Bước 4: git add backend/ (frontend/): để thêm những gì mình code vào staging chuẩn bị cho việc commit

Bước 5: git commit -m "Thông tin những thay đổi khi code": đẩy commit code của mình

Bước 6: git push origin Tên nhánh mình muốn đẩy code lên: để đẩy code lên pull request rồi vào github merge.

Bước 7: vào github sau đó kiểm tra có thể merge thì merge

Nếu đã lỡ commit D trong trường hợp đã kể trên thì dùng git reset --soft HEAD~1 để uncommit gần nhất còn nếu đã commit nhiều lần thì tìm hiểu về git pull origin main --rebase -> Sau đó sửa xung đột (nếu có), rồi: git add . git rebase --continue

