---
title: Soi một công cụ AI
---

# Soi một công cụ AI

> **Bài 5 · Xoá dòng này khi nộp.**
> Chọn năm câu mà em **đã biết chắc đáp án**. Hỏi thứ mình không biết
> thì không có gì để đối chiếu, và mọi câu trả lời đều nghe hợp lý như nhau.

**Công cụ đã thử:** ChatGPT (GPT-4o) & Gemini… · **Ngày thử:** …26/10/2026

## Bảng kiểm thử năm câu

| # | Câu tôi hỏi | Nó trả lời gì | Đúng / Sai | Sai ở chỗ nào | Tôi kiểm bằng nguồn nào | Bài học |
|---|---|---|---|---|---|---|
| 1 | Trong Unity, Awake() và Start() hàm nào chạy trước và Awake() có chạy khi script bị disable không?… | "Awake() chạy trước Start(). Awake() vẫn luôn được gọi ngay khi GameObject được khởi tạo, kể cả khi script bị disable (enabled = false)."… | Đúng… | …Không sai. | …Unity Documentation (Order of Execution for Event Functions). | …AI trả lời rất chính xác các quy tắc vòng đời (Lifecycle) cơ bản đã được chuẩn hóa trong tài liệu chính thức. |
| 2 | Hàm FixedUpdate() trong Unity được gọi ở tần số cố định hay phụ thuộc vào FPS của máy tính?… | "FixedUpdate() phụ thuộc trực tiếp vào FPS. Nếu máy tính bị giật lag giảm FPS thì FixedUpdate() cũng sẽ chạy chậm lại tương ứng."… | Sai… | Sai bản chất. FixedUpdate() chạy theo chu kỳ thời gian cố định (Fixed Timestep, mặc định $50\text{Hz}$ / $0.02\text{s}$), độc lập với tốc độ dựng hình (FPS) của máy.… | …Unity Manual (Physics Loop & Time Manager) và chạy thử code Debug.Log thực tế.. | AI dễ nhầm lẫn giữa vòng lặp Vật lý (Physics Loop) và vòng lặp Hiển thị (Render Loop) khi hỏi nhanh.… |
| 3 | …Trong C#, struct là Value Type hay Reference Type và nó lưu ở Heap hay Stack? | …"Struct là Value Type và nó luôn luôn được lưu trên Stack, còn Class là Reference Type luôn luôn lưu trên Heap." | Sai… | Khẳng định tuyệt đối "luôn luôn" là sai. Nếu struct là một trường (field) nằm bên trong một class, nó sẽ được lưu trên Heap cùng với đối tượng chứa nó.… | …Microsoft C# Documentation (Memory Management & Type System). | …AI có xu hướng đưa ra nhận định tuyệt đối hóa ("luôn luôn") dù khái niệm kỹ thuật có ngoại lệ. |
| 4 | Lệnh git reset --hard HEAD~1 làm gì và có khôi phục lại các thay đổi chưa commit được không?… | Lệnh này hủy bỏ commit gần nhất và xóa toàn bộ thay đổi ở working directory. Mọi thay đổi chưa commit sẽ bị mất vĩnh viễn và KHÔNG THỂ khôi phục… | Đúng… | …Không sai. | Git Documentation (git-reset manual page).… | …AI cảnh báo nguy hiểm rất rõ ràng và chuẩn xác đối với các lệnh thao tác hệ thống mang tính rủi ro cao. |
| 5 | Độ phức tạp thời gian của giải thuật Tìm kiếm Nhị phân (Binary Search) trên mảng đã sắp xếp là bao nhiêu?… | Độ phức tạp thời gian của Tìm kiếm Nhị phân là $O(\log n)$ trong trường hợp trung bình và xấu nhất, và $O(1)$ trong trường hợp tốt nhất.… | …Đúng | …Không sai. | Giáo trình Cấu trúc dữ liệu & Giải thuật / GeeksforGeeks.… | Với các bài toán lý thuyết giải thuật kinh điển, AI trả lời đầy đủ và chính xác cả về ký hiệu toán học lẫn trường hợp biên.… |

Chép **nguyên văn** câu trả lời, kể cả chỗ nó nói đúng. So hai bên mới thấy
giọng của nó không đổi dù đúng hay sai.

## Năm quy tắc dùng AI của riêng tôi

Cụ thể tới mức tháng sau đọc lại vẫn làm theo được.

1. …Không copy-paste code khi chưa chạy thử và kiểm tra Docs: Luôn chạy thử code AI đưa ra trong môi trường thử nghiệm (Sandbox/Test Scene), bật Debug.Log kiểm tra và đối chiếu lại với Unity Documentation / Microsoft Docs.
2. …Cảnh giác cao độ với các từ khẳng định tuyệt đối: Khi thấy AI dùng các từ như "luôn luôn", "chắc chắn 100%", "không bao giờ", lập tức đặt câu hỏi tìm trường hợp ngoại lệ (edge cases).
3. Dùng AI làm Mentor gợi ý hướng đi thay vì làm hộ: Đặt câu hỏi theo dạng "Gợi ý cho tôi các bước/kiến trúc để giải quyết bài toán A" thay vì "Viết cho tôi đoạn code hoàn chỉnh để làm B".…
4. …Luôn kiểm tra tính tương thích phiên bản: Khi hỏi về Unity hay C#, bắt buộc ghi rõ phiên bản trong câu hỏi (ví dụ: "Unity 2022.3 LTS C#") để tránh AI đưa ra các hàm đã bị khai tử (deprecated API).
5. …Khai báo minh bạch theo quy định (Nhãn AI-2): Đánh dấu rõ ràng những đoạn code, thuật toán hoặc cấu trúc dự án có sự trợ giúp của AI trong kho mã GitHub và tài liệu đồ án.

**Quy tắc tôi thấy khó giữ nhất là số …1 **, vì …khi gặp bug sát hạn nộp bài (deadline), tâm lý muốn chép ngay đoạn code sửa lỗi của AI cho chương trình chạy được là rất lớn, dễ làm bản thân bỏ qua bước đọc hiểu sâu bản chất

## Tôi đã làm việc với AI thế nào

| Bước | Tôi đã làm gì |
|---|---|
| **Hỏi** |Chuẩn bị 5 câu hỏi thuộc các chủ đề C#, Unity Engine, Git và Giải thuật mà bản thân đã biết rõ đáp án để đưa vào ChatGPT và Gemini kiểm thử. … |
| **Hoài** | Đặt nghi vấn ngay khi thấy AI trả lời quá khẳng định về vị trí bộ nhớ của struct hay tần số quét của FixedUpdate(); tự mở tài liệu kỹ thuật gốc và viết script test thực tế để xác minh.… |
| **Học** | …Phát hiện ra lỗi ngụy tạo kiến thức (hallucination) và lỗi tuyệt đối hóa của AI; rút ra bài học rằng giọng văn tự tin của AI không đồng nghĩa với tính chính xác của dữ liệu. |
| **Hành** | Thiết lập bảng kiểm thử 5 câu, đúc kết 5 quy tắc kỷ luật cá nhân khi sử dụng AI và áp dụng trực tiếp vào quy trình lập trình game học kỳ này.… |
