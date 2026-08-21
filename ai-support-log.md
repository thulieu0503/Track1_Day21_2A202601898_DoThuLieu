# AI Support Log

> Ghi lại bạn đã dùng AI (ChatGPT/Claude/Kimi...) ở những bước nào khi làm deliverables.
> Trung thực là một phần của bài nộp — không ai làm một mình, quan trọng là bạn giữ
> quyền kiểm soát chất lượng.

# Quy tắc dùng AI
Được dùng AI để:

Paraphrase test inputs sau khi nhóm đã khóa dimensions và combinations.
Brainstorm assertions cho code checks và gợi ý cấu trúc judge prompt.
Tóm tắt pattern từ các case judge lệch để nhóm phân tích nhanh hơn.
Soạn nháp các phần văn bản trong report.
Không được dùng AI để:

Tự chọn dimensions, combinations hoặc coverage strategy thay nhóm.
Gắn nhãn thay con người ở Phase 2 — human baseline phải là của con người.
Quyết định verdict hoặc threshold thay nhóm.
Bịa số liệu, trace hay kết quả chạy không tồn tại.

### Đỗ Thu Liễu

**AI đã giúp tôi ở đâu?**
Sau khi xác định 5 case `quote_verbatim` còn fail, tôi dùng AI để hỗ trợ đối chiếu các case và kiểm tra corpus. Qua quá trình này, xác định được nguyên nhân chung là slide/bảng nhiều cột bị làm phẳng khi convert PDF→markdown. AI hỗ trợ triển khai `_reconstruct_multicolumn()` theo hướng sửa ở tầng corpus. Sau khi kiểm tra lại, `quote_verbatim` tăng từ 73% lên 88%.

**AI sai, hời hợt hoặc làm mất coverage ở đâu?**
AI từng được hỏi về hướng xử lý có thể làm đẹp kết quả bằng cách thay thế nhãn người. Tuy nhiên, AI từ chối vì việc này sẽ tạo dữ liệu không phản ánh đánh giá thực tế. Điều này giúp tôi giữ nguyên dữ liệu gốc thay vì tối ưu kết quả một cách không trung thực.

**Tôi đã tự sửa hoặc quyết định lại điều gì?**
Tôi quyết định thử xử lý lỗi tại `load_corpus()` thay vì dừng ở mức 73–79% và đưa vấn đề vào backlog. Tôi cũng kiểm tra tác động lên retrieval trước khi chạy evaluation đầy đủ. Dù kết quả tăng lên 88%, tôi vẫn giữ verdict **CHƯA TRIỂN KHAI** và không thay đổi ngưỡng chỉ để kết quả đạt yêu cầu.
