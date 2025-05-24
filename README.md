# 💬 Phân tích cảm xúc từ dữ liệu Twitter (Sentiment Analysis)

Dự án áp dụng các kỹ thuật học máy và xử lý ngôn ngữ tự nhiên (NLP) để **phân loại cảm xúc** của người dùng từ dữ liệu mạng xã hội Twitter, phân loại thành: **Tích cực**, **Tiêu cực**, **Trung lập/Không liên quan**.

## 🎯 Mục tiêu
- Xây dựng mô hình phân tích cảm xúc văn bản để hỗ trợ doanh nghiệp hiểu cảm nhận khách hàng.
- Đánh giá và so sánh hiệu suất giữa các mô hình học máy trên bài toán phân loại nhiều lớp.

## 📊 Dữ liệu
- **Nguồn**: [Twitter Entity Sentiment Analysis – Kaggle]
- Bao gồm ~70.000 tweet huấn luyện và ~1.000 tweet kiểm tra.
- Mỗi bản ghi gồm: `tweet_id`, `topic`, `sentiment`, `tweet`.

## 🧹 Tiền xử lý
- Làm sạch dữ liệu: loại bỏ dòng null, mã hóa nhãn.
- Chuyển văn bản thành vector qua pipeline:  
  `CountVectorizer` → `TfidfTransformer`.

## 🛠️ Mô hình đã thử nghiệm
| Mô hình                | Accuracy | Ưu điểm nổi bật               |
|------------------------|----------|-------------------------------|
| Naive Bayes            | 87.4%    | Đơn giản, chạy nhanh         |
| Logistic Regression    | 92.8%    | Ổn định, dễ huấn luyện        |
| Decision Tree          | 92.3%    | Trực quan, dễ giải thích      |
| Random Forest          | 95.6%    | Chính xác, ít overfitting     |
| SVM (Linear)           | 93.9%    | Phân loại tốt dữ liệu tuyến tính |
| SVM (RBF Kernel)       | 97.6%    | Mạnh mẽ, xử lý phi tuyến tốt  |
| K-Nearest Neighbors    | **97.7%**| Chính xác cao nhất, đơn giản  |

👉 **Kết luận**: KNN là mô hình phù hợp nhất vì cho độ chính xác cao, hiệu quả với dữ liệu không tuyến tính, chi phí triển khai vừa phải.

## 🔧 Kỹ thuật
- `Python`, `Scikit-learn`, `Pandas`, `Matplotlib`, `Tfidf`, `SVM`, `KNN`, `Naive Bayes`
- Huấn luyện và kiểm tra mô hình bằng `Google Colab`


*Dự án môn Học máy – Trường Đại học Khoa học Tự nhiên, ĐHQGHN (2025).*

