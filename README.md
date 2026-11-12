# 🛍️ Dự án Phân tích Dữ liệu H&M: Giải pháp Data & Machine Learning Toàn diện

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![DuckDB](https://img.shields.io/badge/DuckDB-Fast%20SQL-yellow?style=for-the-badge&logo=duckdb&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Wrangling-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Statsmodels](https://img.shields.io/badge/Statsmodels-Time%20Series-green?style=for-the-badge)

---

## 📖 Tổng quan Dự án (Project Overview)

Chào mừng đến với kho lưu trữ **Phân tích Dữ liệu H&M**! Đây là **Dự án Danh mục Phân tích Dữ liệu Toàn diện định hướng Kinh doanh (Business-Driven End-to-End Data Analytics Portfolio Project)** được thiết kế để mô phỏng môi trường Bán lẻ & Thương mại Điện tử thực tế.

Sử dụng tập dữ liệu khổng lồ về các giao dịch, sản phẩm và siêu dữ liệu của khách hàng H&M, dự án này thể hiện một vòng đời dữ liệu hoàn chỉnh: bắt đầu từ quá trình **Xử lý dữ liệu SQL (Data Wrangling)**, chuyển sang **Phân tích Khám phá Dữ liệu (EDA)** và kết thúc bằng **các mô hình Học máy (Machine Learning)** có tính ứng dụng cao. Mục tiêu tối thượng là thu hẹp khoảng cách giữa dữ liệu thô và chiến lược kinh doanh của Ban lãnh đạo.

---

## 🎯 Các Trụ cột Kinh doanh Cốt lõi (Core Business Pillars)

Những nỗ lực phân tích và mô hình hóa của dự án hoàn toàn bám sát vào việc giải quyết 3 thách thức lớn của ngành bán lẻ:

1. **Giữ chân Khách hàng & Rời bỏ (Trụ cột 1):** Phân khúc tệp khách hàng để xác định nhóm VIP và nhóm có nguy cơ rời bỏ, hỗ trợ triển khai các chiến dịch marketing mục tiêu.
2. **Cá nhân hóa & Gợi ý sản phẩm (Trụ cột 2):** Xây dựng hệ thống gợi ý chuyên biệt cho khách hàng giá trị cao nhằm tăng Giá trị đơn hàng trung bình (AOV) và Tỷ lệ chuyển đổi.
3. **Dự báo Nhu cầu Tồn kho (Trụ cột 3):** Dự báo khối lượng bán hàng trong tương lai cho các danh mục bán chạy nhất để ngăn ngừa tình trạng hết hàng và giảm thiểu lượng tồn kho quá mức.

---

## 📂 Cấu trúc Kho lưu trữ (Repository Structure)

Kho lưu trữ được tổ chức tuân theo các tiêu chuẩn tốt nhất của Data Engineering và Data Science:

```text
hm-fashion-analytics/
├── data/               # Dữ liệu thô, dữ liệu trung gian và dữ liệu đã xử lý (Parquet/CSV)
├── docs/               # Tài liệu Markdown, từ điển dữ liệu và Báo cáo Kinh doanh cuối cùng
├── models/             # Các mô hình ML và Scaler đã lưu (pkl)
├── notebooks/          # Jupyter Notebooks phân tích (01_data_understanding & 03_ml_2_recommendation)
├── reports/            # Hình ảnh, biểu đồ và báo cáo tóm tắt
├── src/                # Mã nguồn Python xử lý toàn bộ Data Pipeline & Mô hình phân tích:
│   ├── data/           # Module làm sạch và chuẩn hóa dữ liệu thô
│   ├── features/       # Module kỹ thuật trích xuất đặc trưng Khách hàng & Sản phẩm
│   ├── sql/            # Module truy vấn & phân tích SQL DuckDB (RFM, Cá nhân hóa, Dự báo tồn kho)
│   └── visualization/  # Module trực quan hóa dữ liệu EDA
├── tests/              # Unit test để kiểm tra tính toàn vẹn của dữ liệu
├── venv/               # Môi trường ảo Python (Virtual Environment)
├── PROJECT_CONTEXT.md  # Yêu cầu dự án chi tiết ban đầu
└── README.md           # Bạn đang xem tệp này!
```

---

## 🚀 Thông tin chuyên sâu & Mô hình Học Máy (Key Insights & ML Models)

### 💡 Thông tin Kinh doanh (Business Insights - EDA)
- **Nhân khẩu học:** Thế hệ Gen Z và Millennials (độ tuổi 21-30) là nhóm mang lại nguồn doanh thu chủ đạo nhất.
- **Sản phẩm chủ lực (Cash Cows):** Danh mục **"Garment Upper body"** (Quần áo phần trên) thống trị doanh số ở mọi phân khúc.
- **Hiệu suất Kênh bán:** Kênh **Online** vượt trội hoàn toàn so với doanh số Offline, xu hướng này càng được minh chứng rõ rệt và củng cố bền vững trong đại dịch COVID-19.

### 🧠 Các giải pháp Học Máy (Machine Learning Implementations)
1. **Phân khúc khách hàng (K-Means Clustering):** 
   - Áp dụng phân tích RFM (Recency, Frequency, Monetary).
   - Xác định 5 cụm chiến lược: *Champions (VIP), Loyal (Trung thành), Promising (Tiềm năng), At Risk (Nguy cơ rời bỏ), Lost (Đã mất)*.
2. **Hệ thống Gợi ý 2 lớp (2-Stage Recommender Engine):**
   - **Giai đoạn 1 (Popularity Baseline):** Giải quyết vấn đề "cold-start" (người dùng mới) bằng cách gợi ý các sản phẩm đang thịnh hành.
   - **Giai đoạn 2 (Item-based Collaborative Filtering):** Sử dụng TruncatedSVD và Cosine Similarity để tìm quy luật mua kèm (co-purchasing), tập trung vào các nhóm khách hàng giá trị cao.
3. **Dự báo Chuỗi thời gian (Holt-Winters):**
   - Xây dựng mô hình Làm trơn Hàm mũ (Exponential Smoothing) tích hợp xu hướng (trend) và tính mùa vụ (seasonality).
   - Dự báo nhu cầu hàng tuần cho danh mục bán chạy nhất "Garment Upper body".

---

## 🛠️ Công nghệ sử dụng (Tech Stack)

- **Xử lý Dữ liệu & SQL:** DuckDB, Pandas, Numpy, PyArrow (Parquet)
- **Machine Learning & Thống kê:** Scikit-Learn, Statsmodels, SciPy
- **Trực quan hóa Dữ liệu:** Matplotlib, Seaborn
- **Môi trường lập trình:** Python 3.8+, Jupyter Notebook, VS Code

---

## 📥 Tải Dữ liệu (Data Acquisition)

Do tập dữ liệu gốc rất lớn, các file dữ liệu thô không được lưu trữ trực tiếp trên GitHub này. Để chạy được dự án, bạn cần tải dữ liệu trực tiếp từ Kaggle:

1. Truy cập cuộc thi trên Kaggle: [H&M Personalized Fashion Recommendations](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/data)
2. Đăng nhập/Đăng ký tài khoản Kaggle và chọn **Download All**.
3. Giải nén file vừa tải về.
4. Di chuyển 3 file dữ liệu chính (`articles.csv`, `customers.csv`, `transactions_train.csv`) vào thư mục `data/` của dự án này theo cấu trúc sau:

```text
H-M_fashion_analytics/
├── data/
│   ├── articles.csv
│   ├── customers.csv
│   └── transactions_train.csv
...
```

---

## 💡 Hướng dẫn chạy dự án (How to Run)

Thực hiện theo các bước sau để sao chép môi trường và chạy các Notebook trên máy tính của bạn:

**1. Clone kho lưu trữ (Clone the repository)**
```bash
git clone https://github.com/your-username/hm-fashion-analytics.git
cd hm-fashion-analytics
```

**2. Thiết lập Môi trường ảo (Set up Virtual Environment)**
```bash
python -m venv venv

# Trên Windows:
.\venv\Scripts\activate
# Trên Mac/Linux:
source venv/bin/activate
```

**3. Cài đặt Thư viện phụ thuộc (Install Dependencies)**
```bash
pip install pandas numpy scikit-learn statsmodels matplotlib seaborn duckdb pyarrow jupyter
```

**4. Thực thi Dự án (Execution)**

Bạn có thể lựa chọn 1 trong 2 cách sau để chạy dự án tùy theo nhu cầu:

#### 🔹 Cách 1: Chạy tự động toàn bộ Data Pipeline qua các script trong `src/` (Khuyến nghị)
Toàn bộ luồng xử lý dữ liệu từ làm sạch, trích xuất đặc trưng đến các mô hình phân tích SQL đã được mô-đun hóa trong thư mục `src/`. Bạn chỉ cần thực thi tuần tự các lệnh sau:

```bash
# Bước 4.1: Làm sạch và chuẩn hóa dữ liệu thô (Data Cleaning)
python src/data/clean_customers.py
python src/data/clean_articles.py
python src/data/clean_transactions.py

# Bước 4.2: Xây dựng bảng đặc trưng Khách hàng & Sản phẩm (Feature Engineering)
python src/features/build_customer_features.py
python src/features/build_product_features.py

# Bước 4.3: Thực thi các mô hình phân tích SQL chuyên sâu theo 3 trụ cột kinh doanh
python src/sql/analyze_retention_rfm.py                # Trụ cột 1: Phân khúc RFM & Rủi ro Churn
python src/sql/analyze_personalization_preferences.py   # Trụ cột 2: Cá nhân hóa & Sở thích danh mục
python src/sql/analyze_inventory_demand.py             # Trụ cột 3: Dự báo & Quản trị tồn kho

# Bước 4.4: Tạo trực quan hóa dữ liệu EDA & Xuất biểu đồ báo cáo
python src/visualization/run_eda.py
python src/visualization/run_advanced_eda.py
```

#### 🔹 Cách 2: Khám phá trực quan qua các Jupyter Notebook hiện có
Nếu bạn muốn theo dõi trực quan từng bước phân tích khám phá hoặc huấn luyện mô hình gợi ý, hãy khởi chạy Jupyter:

```bash
jupyter notebook
```

Khám phá 2 notebook phân tích chính trong thư mục `notebooks/`:
* `notebooks/01_data_understanding.ipynb`: Khám phá dữ liệu ban đầu, cấu trúc schema, kiểm tra tính toàn vẹn và tỷ lệ khuyết thiếu (Data Profiling & EDA).
* `notebooks/03_ml_2_recommendation.ipynb`: Nghiên cứu, huấn luyện và đánh giá hệ thống gợi ý sản phẩm 2 giai đoạn (Popularity Baseline kết hợp TruncatedSVD Collaborative Filtering).

> 💡 **Lưu ý:** Phần lớn code tiền xử lý dữ liệu, tính toán đặc trưng và phân tích thống kê SQL đã được chuyển đổi thành các module hoàn chỉnh trong thư mục `src/data/`, `src/features/` và `src/sql/`. Do đó, người dùng không cần chạy tuần tự 4 notebook (01 -> 02 -> 03 -> 04) như cấu trúc phác thảo ban đầu mà chỉ cần chạy các script trong `src/` hoặc mở 2 notebook phân tích chính hiện có.

---
*Xây dựng với niềm đam mê quản trị ra quyết định dựa trên dữ liệu.* 🚀
