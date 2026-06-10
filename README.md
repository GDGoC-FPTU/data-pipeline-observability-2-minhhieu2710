[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112821&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** student2A202600550@vinuni.edu.vn
**Name:** Nguyen Van A

---

## Mo ta

Dự án này xây dựng một ETL Pipeline tự động để xử lý dữ liệu sản phẩm. Pipeline thực hiện trích xuất dữ liệu từ file JSON, kiểm tra tính hợp lệ của dữ liệu (giá > 0, category không rỗng), áp dụng giảm giá 10%, chuẩn hóa định dạng văn bản và lưu trữ kết quả ra file CSV phục vụ cho việc phân tích hoặc làm đầu vào cho AI Agent.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python generate_garbage.py
python solution.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
