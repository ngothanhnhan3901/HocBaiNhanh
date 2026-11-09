# Học bài nhanh với AI

Web tĩnh một file (`index.html`), gồm 3 tab:

- **Học nhanh**: đọc từng từ (RSVP) với tốc độ WPM chỉnh được, nhịp độ thông minh theo dấu câu, đọc thành tiếng, 5 màu nền, đổi font và cỡ chữ, nhạc nền. Tải được file `.txt`.
- **Nhắc bài (trong tab Dò bài)**: nội dung bài mặc định được ẩn khi dò. Quên chỗ nào thì bấm 💡 để xem 1 rồi 2 chữ đầu của chỗ cần đọc tiếp (tự dò vị trí theo chữ hiện trực tiếp, nếu không có thì chọn theo câu). Mỗi lần nhắc đều ghi vào Nhật ký.
- **Dò bài**: mặc định Gemini nghe trực tiếp bản ghi âm (có hiện chữ khi đọc) rồi chấm theo ý chính hoặc sát nguyên văn, nhắc chỗ cần lưu ý.
- **Ghi âm tạo bài**: bấm 🎙 trong tab Học nhanh, đọc nội dung, Gemini chuyển giọng nói thành chữ và thêm vào ô văn bản.
- **Tùy chọn học thuộc** (tab Học nhanh, mặc định tắt): thư viện bài, nhắc ôn ngắt quãng 1·3·7·14 ngày, ẩn dần từ, học theo đoạn, luyện lại chỗ sai, tô nổi chữ giữa, tăng tốc dần.
- **Đọc nối tiếp** (tab Học nhanh): trang đưa một câu, bạn đọc câu kế tiếp bằng giọng nói. Có gợi ý, xem đáp án, kết quả lưu vào Nhật ký.
- **Chỗ hay quên** (tab Nhật ký): gom các câu hay bị nhắc, sót hoặc đọc sai, luyện riêng và nhờ AI tạo mẹo nhớ.
- **Nhật ký**: mỗi lần dò bài tự lưu tên bài, điểm, nhận xét và lưu ý cần nhớ, nhóm theo ngày, xóa được từng mục hoặc toàn bộ. Dữ liệu nằm trong trình duyệt của bạn.
- **Sao lưu** (tab Cài đặt): xuất và nhập file JSON gồm nhật ký, thư viện bài, mẹo nhớ. File không chứa khóa API.
- **Cài đặt**: chọn Claude (Anthropic) hoặc Gemini (Google), nhập khóa API và chọn mô hình.

## Đăng lên GitHub Pages

1. Tạo repo, đẩy `index.html` và `README.md` lên nhánh `main`.
2. Vào **Settings > Pages**, chọn nguồn là nhánh `main`, thư mục `/ (root)`.
3. Mở địa chỉ `https://<tên-bạn>.github.io/<tên-repo>/`, vào tab **Cài đặt** và nhập khóa.

## Về khóa API

- Mã nguồn **không chứa khóa**. Mỗi người dùng tự nhập khóa của mình, khóa nằm trong trình duyệt của họ và gửi thẳng tới nhà cung cấp bạn chọn (Anthropic hoặc Google).
- Không ghi khóa vào mã rồi đẩy lên GitHub. Khóa lộ có thể bị dùng trái phép và tính tiền vào tài khoản bạn.
- Nên đặt hạn mức chi tiêu cho khóa trong Anthropic Console.
- Nếu muốn mở web cho nhiều người dùng chung khóa của bạn, cần một máy chủ trung gian (Cloudflare Workers, Vercel…) giữ khóa và gọi API thay trình duyệt. Trang này hiện chưa có phần đó.

## Ghi chú

- Ghi âm dùng Web Speech API (`vi-VN`), chạy tốt nhất trên Chrome và Safari; cần HTTPS (GitHub Pages có sẵn).
- Mô hình: Claude (`claude-sonnet-5-5`, `claude-haiku-5-5`, `claude-opus-5-5`) hoặc Gemini (`gemini-3.5-flash`). Đổi trong tab Cài đặt.
- Khóa Gemini lấy miễn phí tại https://aistudio.google.com/apikey. Mỗi nhà cung cấp lưu khóa riêng.

## Biểu tượng và cài lên màn hình chính

- `favicon.ico`, `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` và `manifest.webmanifest` là biểu tượng của trang. Hãy đẩy cả các file này lên cùng `index.html` (favicon trong `index.html` đã được nhúng sẵn nên vẫn hiện nếu bạn chỉ đẩy một file).
- Trên điện thoại, chọn "Thêm vào màn hình chính" để mở như một ứng dụng. Trang chưa hỗ trợ chạy khi mất mạng.
