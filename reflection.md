Individual reflection — Nguyễn Công Thành(2A202600142)

## 1. Role
Eval metrics + ROI + Demo slides. Phụ trách xây dựng bộ tiêu chí đánh giá (Eval Metrics) và phân tích ROI/Kill Criteria cho dự án  AI In-Car Control Agent (Smart Cabin).

## 2. Đóng góp cụ thể
    - Định nghĩa 3 metrics chính: Intent Accuracy, Task Success Rate, Intervention Rate – kèm ngưỡng đạt (>95%, >98%, <2%).

    - Thiết kế 3 kịch bản ROI (Conservative, Realistic, Optimistic) và Kill Criteria gắn với chi phí cloud <2 USD/xe/tháng và tỷ lệ lỗi an toàn <0.1% sau 6 tháng beta.

    - Phân biệt rõ Precision (Intent Accuracy) và Recall (Task Success Rate) trong bối cảnh AI điều khiển xe.

3. SPEC mạnh/yếu
    -Mạnh nhất: Nhóm nghĩ ra được hệ thống chat bot giúp hỗ trợ điều khiển và tra cứu thông tin cho tài xế thông qua giọng nói và văn bản thật kết hợp giữa AI Automation và Agumentation.

    - Yếu nhất: Hệ thống chỉ mạng tính chất giả lập, thao tác điều khiển xe thông qua các tool mà aggent thực hiện chỉ là mô phỏng thay đổi số liệu vào chưa đưa vào thực tế sử dụng được.

4. Đóng góp khác
    - Tham gia vào 1 phần code xây dựng và lên ý tưởng.

5. Điều học được
    - Cách thiết kế 1 sản phẩm, cách làm việc nhóm hiệu quả, phản biện giữa các thành viên.

6. Nếu làm lại
    - Thiết kế rõ phạm vi hệ thống cần đặt được, xây dựng trợ lý Personalized AI Assistant hoàn chỉnh luôn lắng nghe câu lệnh mà không phải sử dụng nút bấm trên màn hình để nhập lệnh nói, thiết kế Rule và cấu trúc chương trình rõ ràng hơn.

7. AI giúp gì / AI sai gì
Giúp: Dùng Deepseek để sinh các kịch bản ROI – nó gợi ý thêm “tiết kiệm năng lượng pin nhờ AI tối ưu điều hòa” mà tôi chưa nghĩ ra. Dùng ChatGPT để kiểm tra tính nhất quán giữa Kill Criteria và các threshold (ví dụ: nếu Intervention Rate >5% thì roll-back – điều này khớp với kill criteria về safety error rate).

Sai/mislead: Ban đầu Claude đề xuất dùng F1-score làm metric chính. Nhưng trong bối cảnh điều khiển xe, F1-score che mất sự khác biệt giữa precision và recall. Nếu nghe theo, nhóm có thể chấp nhận 2% bỏ sót lệnh “phanh” vì F1 vẫn cao. Đó là sai lầm nguy hiểm. Bài học: Không dùng metric tổng hợp cho safety-critical AI. Phải tách riêng precision và recall với ngưỡng khác nhau.