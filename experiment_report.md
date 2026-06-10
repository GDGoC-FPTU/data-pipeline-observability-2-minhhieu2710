# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600550
**Name:** Pham Minh Hieu
**Date:** 2024-05-20

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Trả về thông tin sản phẩm chính xác, tính toán đúng tổng giá trị. | 10 | Dữ liệu nhất quán. |
| Garbage Data (`garbage_data.csv`) | Báo lỗi hoặc đưa ra thông tin sai lệch về giá trị sản phẩm. | 2 | Dữ liệu nhiễu. |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi sử dụng Garbage Data, AI Agent thường đưa ra kết quả không chính xác hoặc thậm chí bị treo do dữ liệu không đúng định dạng. Các vấn đề như Duplicate IDs khiến Agent bị nhầm lẫn giữa các thực thể, wrong data types (như giá bằng chữ) khiến các phép tính toán học bị lỗi hoàn toàn. Outliers cực đoan bóp méo các thống kê trung bình, còn null values làm Agent mất ngữ cảnh quan trọng để xử lý. Việc có một pipeline ETL sạch là điều kiện tiên quyết vì "Rác vào thì Rác ra" (Garbage In, Garbage Out), chất lượng dữ liệu đóng vai trò quan trọng hơn cả việc tinh chỉnh prompt.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Đồng ý. Một prompt dù tinh tế đến đâu cũng không thể xử lý chính xác nếu đầu vào là dữ liệu rác, thiếu nhất quán hoặc sai định dạng kỹ thuật.
