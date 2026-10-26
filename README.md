# Sắc Độ — Giáo trình Lightroom tương tác

16 chương học trực tiếp trên web: giải thích cơ chế, bản đồ công cụ, ví dụ có lập luận, phòng thực hành theo chủ đề, bài tập tự kiểm và sổ tay cá nhân. Không cần mở PDF để học.

## GitHub Pages

Settings → Pages → Deploy from a branch → main → / (root) → Save.

Website: https://duykhanh2401.github.io/lightroom/

Mỗi chương có đường dẫn riêng, ví dụ `#/lesson/3`. Không cần build hoặc backend; dùng đường dẫn tương đối để chạy ở thư mục con của repository.

## Nội dung và chức năng

- 64 phần giải thích chuyên sâu, 16 ca thực hành có từng bước lập luận.
- 16 phòng thực hành theo chủ đề: lưu mốc, ngữ cảnh màu, Exposure, WB, Curve, HSL, Grading, trộn kênh, mask elip, độ nét, crop, dải màu da, match, preset, xuất JPEG và đồ án.
- So ảnh gốc và ảnh chỉnh; histogram RGB tính từ pixel preview.
- Nạp JPEG PNG WebP tại trình duyệt, giới hạn 25 MB. File không được gửi tới máy chủ.
- Ghi chú, lý giải, tự kiểm và tiến độ lưu trong localStorage; xuất sổ tay Markdown để sao lưu.
- Preset trong lab là dữ liệu riêng của mô hình, không phải XMP Lightroom.
- Tạo JPEG thật với kích thước và quality lựa chọn; tính pixel in từ cm và PPI.

## Giới hạn cần hiểu

Các phép xử lý là mô hình giáo dục giản lược trên JPEG sRGB, không phải thuật toán Adobe, trình chỉnh sửa RAW hoặc mô phỏng chính xác các thanh Lightroom. Mask trong lab là elip hình học; chọn da và HSL chỉ chọn theo phạm vi màu, không nhận diện người hay vật thể. Lab crop không mô phỏng Upright, lens correction hoặc Generative Remove. Không có chuyển ICC máy in hoặc xuất HDR trong lab.

Ảnh thực hành `assets/practice-portrait.jpg` được tạo bằng AI cho giáo trình này; không phải ảnh một người thật được cung cấp làm tham chiếu. Nguồn ảnh được thu nhỏ còn tối đa 640 x 480 khi xử lý preview để giữ hiệu năng. Lab xuất JPEG sử dụng ảnh đầu vào ở kích thước yêu cầu; nội suy lớn hơn nguồn không thêm chi tiết thực. Font có fallback hệ thống.

Các file PDF cũ trong `docs/` được giữ như bản lưu của phiên bản trước; giao diện học mới không liên kết hay phụ thuộc chúng. Tài liệu ngoài giữ quyền của tác giả tương ứng, giáo trình liên kết tới nguồn gốc.

## Kiểm tra

Đã kiểm tra cú pháp JavaScript, cấu trúc đầy đủ 16 chương, đường dẫn nội bộ, trạng thái trung tính không đổi pixel, +1 EV trong mô hình tuyến tính, phạm vi mask, làm mượt vùng đồng nhất và dữ liệu nguồn bất biến. Kiểm tra trình duyệt gồm các nhóm xử lý ảnh, nạp ảnh, lưu ghi chú sau reload, áp preset, match đích và mã hóa JPEG. Không có dependency hoặc bước build.
