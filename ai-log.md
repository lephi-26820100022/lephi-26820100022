---
title: Nhật ký dùng AI
---

# Nhật ký dùng AI — cả học phần

> **Bài 6 · Xoá dòng này khi nộp.**
> Dùng AI là bình thường và được khuyến khích. Giấu mới là vấn đề.
> Trang này chính là một phần sản phẩm của bài cuối.

| Bài | Công cụ | Vai | Tôi nhờ nó làm gì | Tôi đã sửa lại gì |
|---|---|---|---|---|
| 1 | ChatGPT / Gemini… | Sinh bản nháp + Đối tác phản biện |..Phân tích 3 tin tuyển dụng thực tế và trích xuất thành Bảng năng lực ASK cho Kỹ sư Phần mềm / Game Dev.… |.Xóa bỏ toàn bộ thông tin AI tự bịa (đòi hỏi 3 năm kinh nghiệm Microservices, chứng chỉ AWS, thành thạo 5 ngôn ngữ) để bám sát 100% văn bản gốc..… |
| 2 | …Claude / ChatGPT | Đối tác phản biện | …Đặt câu hỏi phản biện về quyết định chọn hướng đi Unity Game Developer thay vì học dàn trải nhiều ngành. | Tự điều chỉnh lộ trình cá nhân, tập trung đào sâu C#, OOP và Giải thuật thay vì học hời hợt nhiều công cụ cùng lúc.… |
| 3 | …ChatGPT | Sinh bản nháp | Dựng khung Markdown chuẩn cho Cẩm nang giải quyết vấn đề nhóm và gợi ý mẫu biên bản họp.… | …Loại bỏ các số liệu ước lượng do AI tự tạo, thay thế bằng 100% số liệu thực tế nhóm đã tự theo dõi và thu thập trong 7 ngày. |
| 4 | Claude / Gemini… | Người kèm cặp | …Đóng vai Nhà tuyển dụng Game Dev hỏi ngược lại để đánh giá Dấu chân số và hồ sơ GitHub/Itch.io. | Tự rà soát tài khoản cá nhân, ẩn bài đăng cũ thời THPT và lập kế hoạch đưa sản phẩm Game 2D demo thực tế lên Itch.io.… |
| 5 | ChatGPT… | Đối tác phản biện | Trả lời 5 câu hỏi kiểm thử kiến thức lập trình C#, Unity Engine, Git và Thuật toán mà bản thân đã biết chắc đáp án.… | …Vạch lá tìm sâu, chỉ ra 2 câu AI trả về thông tin sai bản chất (FixedUpdate phụ thuộc FPS và struct luôn nằm trên Stack) dù giọng văn rất tự tin. |
| 6 | …Gemini / ChatGPT | Hỗ trợ tổng hợp… | Tổng hợp lịch sử tương tác AI của cả 6 bài học phần thành bảng nhật ký thống nhất.… | Đối chiếu lại toàn bộ minh chứng lịch sử (commit, screenshot), tự tay hoàn thiện các bài học đúc kết và đảm bảo tính trung thực 100%.… |

## Ba lần nó nói sai mà tôi bắt được

1. …Bịa đặt yêu cầu tuyển dụng (Bài 1): AI tự động thêm tiêu chuẩn "bắt buộc 3 năm kinh nghiệm thiết kế kiến trúc Microservices và chứng chỉ AWS" vào vị trí tuyển dụng Junior/Intern Software Engineer.

Kiểm chứng: Mở file ảnh chụp màn hình tin tuyển dụng gốc của FPT Software và VNG, thực tế nhà tuyển dụng chỉ yêu cầu vững OOP, C# / Java cơ bản và có đồ án thực tế.

2. …Khẳng định sai về cơ chế vòng lặp trong Unity Engine (Bài 5): AI khẳng định "Hàm FixedUpdate() phụ thuộc trực tiếp vào FPS của máy tính, máy lag thì FixedUpdate() chạy chậm lại tương ứng".
 
 Kiểm chứng: Đọc Unity Documentation (Order of Execution for Event Functions), FixedUpdate() chạy theo chu kỳ thời gian cố định (Fixed Timestep, mặc định $0.02\text{s}$), hoàn toàn độc lập với tốc độ dựng hình (FPS) của máy tính.

3. Tuyệt đối hóa kiến thức quản lý bộ nhớ C# (Bài 5): AI khẳng định "Kiểu dữ liệu struct trong C# là Value Type nên LUÔN LUÔN được lưu trên Stack".

Kiểm chứng: Tra cứu tài liệu Microsoft C# Docs, nếu một struct khai báo làm trường (field) bên trong một class, nó sẽ được lưu trên Heap cùng với đối tượng chứa nó chứ không nằm trên Stack.…

## Điều tôi học được về cách làm việc với nó
Coi AI là "Tập sự nhanh nhẹn nhưng hay bốc phét": AI rất giỏi trong việc dựng khung, gợi ý cú pháp Markdown, tóm tắt thông tin và viết code mẫu. Tuy nhiên, nó không thể thay thế năng lực tư duy, kiểm thử và chịu trách nhiệm cho sản phẩm cuối cùng.

Giọng văn tự tin không đồng nghĩa với câu trả lời đúng: AI luôn đưa ra đáp án với một thái độ rất trôi chảy và quyết đoán, dù thông tin đó hoàn toàn sai lệch. Tuyệt đối không dùng sự "nghe có vẻ hợp lý" để đánh giá độ chính xác của dữ liệu.

Quy trình làm việc chuẩn: Hỏi (cung cấp bối cảnh + giao vai rõ ràng) $\rightarrow$ Hoài (luôn nghi ngờ, soi lỗi hallucination) $\rightarrow$ Học (đối chiếu tài liệu gốc Docs/thực nghiệm code) $\rightarrow$ Hành (tự tay sửa và làm chủ sản phẩm).
…
