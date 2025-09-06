# Phát hiện gian lận thẻ tín dụng (credit card fraud detection)

## Mô tả dự án
Xây dựng và huấn luyện mạng nơ-ron AutoEncoder để phát hiện gian lận thẻ tín dụng.

## Bộ dữ liệu
Dự án sử dụng bộ dữ liệu "Credit Card Fraud Detection" nổi tiếng từ Kaggle.
* Nguồn: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud



## Ý tưởng
* Huấn luyện một autoencoder chỉ với các giao dịch bình thường (không gian lận). khi đó, sai số của mô hình khi tái tạo các mẫu giao dịch bình thường sẽ rất thấp. 

* Tuy nhiên, khi chúng ta đưa vào mẫu giao dịch gian lận, sai số khi tái tạo sẽ rất cao vì mô hình chưa bao giờ thấy mẫu dữ liệu này

* Việc của chúng ta là chỉ cần đặt ra một ngưỡng (threshold), bất kỳ giao dịch nào có sai số vượt ngưỡng đã cho sẽ bị gắn cờ là "bất thường" hoặc "gian lận".
