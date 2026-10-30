# 1. Vấn đề là gì?

Dự án cần lưu trữ code cảm biến, chia sẻ báo cáo và trao đổi công việc. Nếu không quản lý tốt sẽ dễ mất dữ liệu, lộ mật khẩu và bỏ sót nhiệm vụ.

# 2. Yêu cầu là gì?

- Chức năng 1 (Lưu trữ): Thiết lập mô hình Hybrid Workflow cho đội Dev để code luôn an toàn.

- Chức năng 2 (Chia sẻ): Thiết lập phân quyền cho nhà đầu tư (chỉ xem báo cáo) và đối tác cung cấp thiết bị (được bình luận góp ý).

- Chức năng 3 (Giao tiếp): Chuyển đổi các thảo luận về lỗi cảm biến thành các Task có Deadline trong Enterprise Workspace.

# 3. Cách làm ra sao?

**a. Cấu trúc Folder:**
- `sensors`: Lưu code cảm biến.
- `reports`: Lưu báo cáo.
- `documents`: Lưu tài liệu.
- `.env`: Lưu mật khẩu, không chia sẻ.

**b. Cấu trúc Channel:**
- `#announcements`: Thông báo.
- `#technical`: Trao đổi kỹ thuật.
- `#tasks`: Quản lý công việc.
- `#general`: Trao đổi chung.

**c. Phân quyền:**

| Đối tượng | Quyền |
|---|---|
| Đội Dev | Editor |
| Nhà đầu tư | Viewer |
| Đối tác | Commenter |
| Trưởng dự án | Owner |

**d. Quy trình làm việc:**
- Lưu code trên máy và bật Auto Sync để đồng bộ lên Cloud.
- Bật Version History để khôi phục code khi cần.
- Chuyển lỗi cảm biến thành Task và đặt Deadline.
- Dùng Transfer Ownership để bàn giao dự án.

**e. Khôi phục khi folder sensors bị xóa:**
1. Mở Recycle Bin trên Cloud.
2. Tìm folder `sensors` và chọn Restore.
3. Kiểm tra lại dữ liệu sau khi khôi phục.
