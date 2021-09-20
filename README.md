# Ứng dụng mô hình Hidden Markov cho bài toán nhận diện chữ số
## Thông tin nhóm
|**Thành viên**|**MSSV**|
|:- | --- |
|Vũ Đăng Hoàng Long|18120203|
|Nguyễn Huỳnh Đại Lợi|18120198|
|Huỳnh Long Nam|18120212|
|Phạm Nhật Minh|18120209|
|Nguyễn Bảo Long|18120201|
  
---
# Tổng quan bài toán

Đối với con người, âm thanh chính là phương thức giao tiếp hiệu quả và thông dụng nhất. Cũng chính vì thế mà nhận diện giọng nói là một chủ đề hữu ích, có nhiều ứng dụng. Dễ dàng thấy được tính ứng dụng này khi mà hiện nay các trợ lý ảo trở nên rất phổ biến, hay các ứng dụng nhập liệu bằng giọng nói,…

Bài toán nhận diện giọng nói nói chung là bài toán tìm cách giúp cho máy tính có thể hiểu được con người và giọng nói, từ đó có các phản hồi hợp lý. Trong đồ án này, với mục đích chính là tìm hiểu về cách ứng dụng mô hình Hidden Markov, bài toán chính nhóm chọn thực hiện là nhận diện chữ số từ âm thanh cô lập (isolated digit recognition). Đây là bài toán theo nhóm đánh giá là không quá phức tạp, là nền tảng cho các toán lớn hơn như nhận diện chữ từ giọng nói hay chuyển từ giọng đọc thành văn bản.

**Input**: một đoạn âm thanh ngắn chứa giọng đọc một số bất kỳ từ 0 tới 9.

**Output**: cho biết số từ âm thanh này.

**Dữ liệu sử dụng**:
-	[FSDD (Free Spoken Digit Dataset)](https://github.com/Jakobovski/free-spoken-digit-dataset): đây là dữ liệu tiếng anh, gồm 3000 mẫu giọng đọc từ 6 người, mỗi người sẽ đọc mỗi số từ 0-9 50 lần (50x10x6 = 3000).
-	[Speech Commands](https://www.wolfram.com/language/12/machine-learning-for-audio/classify-spoken-digits.html?product=mathematica): đây là dữ liệu của Google bao gồm giọng đọc các số và một số lệnh đơn (left, right,…). Phiên bản nhóm sử dụng do Wolfram cung cấp, tách ra dữ liệu giọng đọc số ra từ dữ liệu gốc. Dữ liệu này có 10000 mẫu cho tập huấn luyện và 1000 mẫu cho tập test, được đọc bởi 997 người.

---
# Môi trường cài đặt, sử dụng
Đồ án này được thực hiện trên môi trường Google Colab nhằm giúp dễ dàng chia sẻ và sử dụng.

---
# Tổ chức github
## Folders
- experiment/ : chứa notebook thực hiện các thí nghiệm.<br>
- pre_trained/ : chứa các model đã train từ các thí nghiệm.<br>
- sample_audio/ : chứa audio mẫu dùng để khám phá.<br>
## Files
- `demo.ipynb`: notebook chính dùng để demo.<br>
- `Report.pdf`: file báo cáo đồ án chính thức của nhóm.<br>

---
# Tham khảo
[1]. D. Jurafsky, J.H. Martin (2020). Speech and Language Processing (3rd ed. draf). Truy cập tại: https://web.stanford.edu/~jurafsky/slp3/

[2]. L. R. Rabiner, J. G. Wilpon and F. K. Soong, "High performance connected digit recognition using hidden Markov models," in IEEE Transactions on Acoustics, Speech, and Signal Processing, vol. 37, no. 8, pp. 1214-1225, Aug. 1989, doi: 10.1109/29.31269.

[3]. J. Picone, "Continuous speech recognition using hidden Markov models," in IEEE ASSP Magazine, vol. 7, no. 3, pp. 26-41, July 1990, doi: 10.1109/53.54527. Truy cập tại: https://www.isip.piconepress.com/publications/journals_refereed/1990/ieee_asspm/hmms/paper_v00.pdf 

[4]. N.L.Huy (2019). Sơ lược về Mel Frequency Cepstral Coefficients (MFCCs) trên Viblo. Truy cập tại: https://viblo.asia/p/so-luoc-ve-mel-frequency-cepstral-coefficients-mfccs-1VgZv1m2KAw 

[5]. Haytham Fayek (2016), Speech Processing for Machine Learning: Filter banks, Mel-Frequency Cepstral Coefficients (MFCCs) and What's In-Between, online blog. Truy cập tại: https://haythamfayek.com/2016/04/21/speech-processing-for-machine-learning.html#fnref:1

[6]. J. Hui (2019), Speech Recognition — GMM, HMM on Medium. Truy cập tại: https://jonathan-hui.medium.com/speech-recognition-gmm-hmm-8bb5eff8b196 
