# Google Sign-In QA – Văn phòng Đảng ủy xã Lệ Ninh

Repository thử nghiệm độc lập, không phải website chính thức.

- Chỉ nghiệm thu Google Sign-In bằng Firebase Spark `vpduln-quanlynhiemvu`.
- Firestore Rules giữ nguyên chế độ từ chối toàn bộ.
- Không nhập tài liệu hoặc dữ liệu công việc thật.
- Mã nguồn từ PR #4, commit `a11d986554033d1c775083632b2ab2b0151a2002`.

Đường dẫn dự kiến sau khi bật GitHub Pages: https://vuhiep2603-blip.github.io/bo-cong-cu-le-ninh-auth-qa/nhiem-vu/

## Bật Pages

Settings → Pages → Build and deployment → Source → **GitHub Actions**.

GitHub Actions sẽ tạo và xuất bản gói tĩnh; không dùng Firebase CLI, không sửa cơ sở dữ liệu và không thay đổi website chính.

## Checklist nghiệm thu

1. Mở trang thử bằng hồ sơ trình duyệt sạch.
2. Bấm Đăng nhập bằng Google (dùng tài khoản thử đã được chấp thuận).
3. Xác nhận hiển thị “Tài khoản chưa được cấp quyền” do Firestore Rules khóa toàn bộ.
4. Bấm Đăng xuất rồi tải lại trang; không khôi phục phiên.
5. Không ghi tài liệu hoặc nhiệm vụ thật. Đăng nhập lần đầu có thể tạo user trong Firebase Authentication, nhưng không tạo hồ sơ Firestore.
