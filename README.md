# Ứng dụng Âm thanh Trực tiếp

Đây là một ứng dụng web minh họa khả năng của Google Gemini AI trong việc xử lý và phản hồi các luồng âm thanh trực tiếp. Ứng dụng thu âm thanh từ micrô của người dùng, gửi đến Gemini AI và phát lại phản hồi âm thanh được tạo ra trong thời gian thực. Ứng dụng cũng có tính năng hiển thị 3D phản ứng với đầu vào và đầu ra âm thanh.

## Tính năng

- Truyền phát âm thanh thời gian thực đến Google Gemini AI.
- Phát lại phản hồi âm thanh do AI tạo ra.
- Hiển thị 3D của luồng âm thanh.
- Giao diện người dùng đơn giản và trực quan để bắt đầu, dừng và đặt lại phiên âm thanh.

## Cách hoạt động

Ứng dụng được xây dựng dưới dạng một thành phần web bằng thư viện Lit. Khi người dùng cấp quyền truy cập micrô và bắt đầu một phiên, ứng dụng sẽ:

1.  Thu âm thanh từ micrô của người dùng bằng Web Audio API.
2.  Xử lý âm thanh thành dữ liệu PCM.
3.  Gửi dữ liệu âm thanh trong thời gian thực đến Google Gemini AI.
4.  Nhận phản hồi âm thanh từ Gemini AI.
5.  Giải mã và phát lại âm thanh đã nhận.
6.  Thư viện `three.js` được sử dụng để tạo hiển thị 3D được kết nối với đầu vào và đầu ra âm thanh, cung cấp một biểu diễn trực quan của âm thanh.

## Công nghệ sử dụng

- [Lit](https://lit.dev/) - Một thư viện đơn giản để xây dựng các thành phần web nhanh và nhẹ.
- [Google Gemini AI](https://deepmind.google/technologies/gemini/) - Mô hình AI được sử dụng để xử lý luồng âm thanh.
- [Three.js](https://threejs.org/) - Một thư viện đồ họa 3D được sử dụng để hiển thị âm thanh.
- [TypeScript](https://www.typescriptlang.org/) - Ngôn ngữ lập trình được sử dụng cho ứng dụng.
- [Vite](https://vitejs.dev/) - Công cụ xây dựng được sử dụng cho dự án.

## Cài đặt

1.  Sao chép kho lưu trữ:
    ```bash
    git clone https://github.com/your-username/live-audio.git
    ```
2.  Cài đặt các gói phụ thuộc:
    ```bash
    npm install
    ```
3.  Tạo một tệp `.env` trong thư mục gốc của dự án và thêm khóa API Gemini của bạn:
    ```
    GEMINI_API_KEY=your-api-key
    ```
4.  Khởi động máy chủ phát triển:
    ```bash
    npm run dev
    ```

## Sử dụng

1.  Mở ứng dụng trong trình duyệt của bạn.
2.  Nhấp vào nút "Bắt đầu" để bắt đầu ghi âm.
3.  Nói vào micrô của bạn.
4.  Ứng dụng sẽ gửi âm thanh của bạn đến Gemini AI và phát lại phản hồi.
5.  Nhấp vào nút "Dừng" để kết thúc ghi âm.
6.  Nhấp vào nút "Đặt lại" để xóa phiên và bắt đầu lại.
