# BÀI TẬP SỐ 1
## PHẦN 1: PHÂN TÍCH 2 SAI LẦM CỦA NAM
### 1. Hai sai lầm trong tư duy của Nam
Sai lầm 1: Cho rằng định dạng trực quan (WYSIWYG) của Word là cần thiết cho tài liệu kỹ thuật/mã nguồn. Nam nhầm lẫn giữa việc trình bày văn bản thông thường và việc quản lý tài liệu mã nguồn. File Word (.docx) thực chất là một gói nén chứa nhiều file XML và tệp nhúng nhằng phức tạp bên trong, không phù hợp cho việc theo dõi thay đổi mã nguồn.

Sai lầm 2: Nghĩ rằng Markdown kém chuyên nghiệp chỉ vì nó là văn bản thô (Plain Text). Nam không thấy được rằng các nền tảng phát triển phần mềm hiện đại như GitHub và các AI IDE ưu tiên Markdown vì tính đồng nhất, dễ đọc trực tiếp trên trình duyệt, dễ tích hợp với hệ thống quản lý mã nguồn (Git) mà không cần phần mềm bên thứ ba như Microsoft Office.

### 2. Tại sao Markdown lại an toàn và nhẹ hơn?
Nhẹ hơn (Dung lượng nhỏ): Markdown hoàn toàn là các ký tự văn bản thô (Plain Text), không chứa các mã định dạng nhị phân, hình ảnh nhúng hay metadata phức tạp như Word. Do đó, dung lượng file .md cực kỳ nhỏ gọn (chỉ vài KB), giúp việc truyền tải, lưu trữ và đồng bộ hóa trên Git diễn ra tức thì.

An toàn hơn (Chống hỏng file & Hỗ trợ Git Diff):

Về độ bền: Nếu file Word bị mất một vài byte dữ liệu (do lỗi đường truyền), cấu trúc file XML bên trong sẽ bị hỏng và phần mềm không thể đọc được (lỗi file corrupt). Trong khi đó, với Markdown, nếu mất một vài byte, bạn chỉ bị mất vài ký tự văn bản và vẫn dễ dàng mở, đọc hoặc sửa thủ công bằng bất kỳ trình soạn thảo văn bản nào (Notepad, VS Code).

Về quản lý phiên bản (Git Diff): Khi dùng Markdown, Git có thể so sánh chính xác từng dòng bị thay đổi (thêm, bớt ký tự nào). Ngược lại, file Word lưu dữ liệu theo dạng nhị phân đóng gói, khiến hệ thống Git không thể so sánh chi tiết mà coi như toàn bộ file thay đổi, dẫn đến lỗi xung đột (Conflict) toàn cục mỗi khi có người chỉnh sửa.
