# Vietnamese News Classification

Dự án phân loại tin tức tiếng Việt tự động sử dụng các thuật toán học máy. Đây là Bài tập lớn môn Khai phá dữ liệu (CO3029) tại Trường Đại học Bách Khoa - ĐHQG TP.HCM.

## Sinh viên thực hiện
* Võ Công Đăng Khôi
* Nguyễn Thị Cẩm Vân
* Nguyễn Sĩ Hoàng Khang 

## Dữ liệu (Dataset)
* Nguồn: [Vietnamese Online News Dataset](https://www.kaggle.com/datasets/haitranquangofficial/vietnamese-online-news-dataset) từ Kaggle.
* Quy mô: 172,132 bản ghi thô, sau khi tiền xử lý còn 51,880 bản ghi chất lượng.
* Danh sách 7 chủ đề: Thế giới, Thể thao, Pháp luật, Thời sự, Kinh doanh, Giải trí, Sức khỏe.

## Quy trình xử lý
1. Tiền xử lý: Loại bỏ các bài viết trùng lặp, xử lý dữ liệu thiếu, lọc bài viết quá ngắn và thực hiện tách từ (Tokenization).
2. Biểu diễn dữ liệu: Chuyển đổi văn bản sang dạng vector bằng phương pháp TF-IDF.
3. Trực quan hóa: Sử dụng các kỹ thuật giảm chiều dữ liệu PCA, t-SNE và UMAP để phân tích các cụm chủ đề.

## Kết quả mô hình
Dự án so sánh hiệu năng của 3 mô hình chính:

| Mô hình | Accuracy | Đặc điểm |
| :--- | :--- | :--- |
| Naive Bayes | 89.31% | Đơn giản, tốc độ huấn luyện và dự đoán rất nhanh. |
| SVM (Linear) | 93.96% | Đạt độ chính xác cao nhất, hoạt động ổn định trên dữ liệu văn bản. |
| ANN | 93.07% | Khả năng học các quan hệ phi tuyến và đặc trưng ngữ nghĩa tốt. |

## Hướng phát triển
* Tích hợp các mô hình ngôn ngữ tiền huấn luyện như PhoBERT hoặc FastText.
* Thử nghiệm các kiến trúc Deep Learning chuyên sâu như TextCNN, LSTM hoặc BiLSTM.
* Xây dựng API hoặc giao diện Web để ứng dụng phân loại trong thực tế.
## Hướng dẫn sử dụng

### 1. Yêu cầu hệ thống
Dự án được thực hiện trên ngôn ngữ **Python 3.x** với các thư viện chính:
* `pandas`, `numpy` (Xử lý dữ liệu)
* `scikit-learn` (Huấn luyện mô hình NB, SVM)
* `tensorflow`/`keras` (Huấn luyện mô hình ANN)
* `vnpcore` hoặc `pyvi` (Tách từ tiếng Việt)
* `matplotlib`, `seaborn`, `umap-learn` (Trực quan hóa)

### 2. Cài đặt môi trường
Mở terminal tại thư mục dự án và chạy lệnh sau để cài đặt các thư viện cần thiết:
```bash
pip install pandas numpy scikit-learn tensorflow matplotlib seaborn umap-learn pyvi
```

Chi tiết cấu trúc thuật toán và đánh giá xem tại file báo cáo đính kèm trong repository.
