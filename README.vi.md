# Agent Ops Clinic — Phòng thực hành vận hành AI Agent

Dự án giáo dục song ngữ được xây bằng **OpenAI Codex CLI** cho chiến dịch ứng tuyển Codex Ambassador 2026. Đây là **mô phỏng vận hành**, không gọi API mô hình, không tự triển khai sản phẩm và không xử lý dữ liệu khách hàng thật.

## Chạy ứng dụng
Cần Python 3 để mở máy chủ local (không cần đăng nhập, không cần API key):

```bash
git clone https://github.com/xuanhieu/agent-ops-clinic
cd agent-ops-clinic
python3 -m http.server 4173 --bind 127.0.0.1
```

Mở `http://127.0.0.1:4173` trong trình duyệt. Nhấn VI để đổi sang tiếng Việt.

## Chạy kiểm thử
Cần Node.js phiên bản có hỗ trợ `node --test`:

```bash
node --test
node scripts/smoke.mjs
```

Chạy các lệnh trên từ thư mục gốc của repo (thư mục chứa `index.html`). Kết quả kiểm lại ngày 29/10/2026: 36/36 unit test pass; 3/3 luồng smoke pass. Trên Chrome headless mô phỏng kích thước 390 và 1440 CSS px không có tràn ngang.

## Bài học thực hành 20 phút
1. **Phút 0–3:** Giải thích khác biệt giữa agent tự đề xuất, người phê duyệt và hệ thống kiểm soát.
2. **Phút 3–7:** Chọn một trong ba tình huống Startup / Cộng đồng / Giáo dục; đọc yêu cầu và các nhiệm vụ.
3. **Phút 7–12:** Cho nhiệm vụ tiến đến Review; cố gắng Publish khi chưa giải quyết rủi ro, quan sát hệ thống chặn.
4. **Phút 12–16:** Phê duyệt/khắc phục rủi ro (mô phỏng), chỉnh hạn mức ngân sách phù hợp; quan sát logic khi được phép Publish.
5. **Phút 16–19:** Tải JSON sự kiện, chạy test và phân tích luồng kiểm chứng.
6. **Phút 19–20:** Tóm tắt: agent có thể đề xuất và hành động, nhưng quyền duyệt/tài nguyên/dấu vết phải rõ ràng.

## Thử thách cho người học
- Cơ bản: xác định vì sao việc công bố bị chặn trong từng trường hợp.
- Trung cấp: dùng Codex viết một test mới xác nhận khi sửa brief, các quyết định cũ không được tái sử dụng.
- Nâng cao: bổ sung một cơ chế cân bằng ngân sách và test lỗi cho cơ chế đó mà không gọi API bên ngoài.

## Ranh giới
- Toàn bộ dữ liệu, tổ chức và chi phí đều là ví dụ hư cấu.
- Không thể dùng demo để chứng minh agent thật đã chạy tác vụ, đánh giá bảo mật thực tế hay bảo vệ production.
- Không nhập bí mật hoặc dữ liệu thật trong workshop.
- Source và nội dung có thể được chia sẻ công khai sau khi người sở hữu kiểm tra quyền sở hữu và giấy phép.
