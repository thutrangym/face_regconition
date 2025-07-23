💻 Dự án Nhận Diện Khuôn Mặt bằng CNN, FaceNet và OpenCV (LBPH)
🧠 Giới thiệu
Dự án này xây dựng một hệ thống nhận diện khuôn mặt bằng 3 phương pháp chính:

CNN (mạng nơ-ron tích chập) huấn luyện từ đầu

FaceNet: tạo vector đặc trưng khuôn mặt (embedding) rồi so sánh khoảng cách

OpenCV LBPH: phương pháp truyền thống sử dụng histogram của các điểm ảnh nhị phân

Hệ thống có thể nhận diện người từ:

Video có sẵn

Nguồn webcam trực tiếp

📁 Cấu trúc thư mục

<img width="1175" height="604" alt="image" src="https://github.com/user-attachments/assets/6dc61865-6f8c-44f6-9030-039795485e5e" />

⚙️ Cách hoạt động
Trích xuất dữ liệu

Đặt video vào thư mục data/train/, mỗi người một thư mục riêng.

Tự động trích xuất ảnh khuôn mặt lưu vào dataset/train/ và dataset/val/.

Huấn luyện mô hình

CNN: huấn luyện mô hình phân loại khuôn mặt.

FaceNet: dùng mô hình đã huấn luyện sẵn để tạo vector embedding rồi tính khoảng cách cosine hoặc Euclidean.

LBPH: dùng OpenCV để huấn luyện dựa trên histogram ảnh mặt.

Nhận diện

Thực hiện trên webcam hoặc video có sẵn.

Ghi lại video có gắn nhãn nhận diện và lưu vào output/.

🧩 Thư viện cần thiết
Cài đặt qua pip:

bash
Sao chép mã
pip install -r requirements.txt
Các thư viện chính sử dụng:

opencv-python

numpy

tensorflow, keras

scikit-learn

mtcnn hoặc dlib

pickle (lưu label map)

📌 Hướng dẫn sử dụng notebook
face_recognition_face_net.ipynb: Nhận diện bằng mô hình FaceNet.

face_regconition_cnn.ipynb: Huấn luyện và test bằng CNN.

face_regconition_LBPH.ipynb: Dùng OpenCV LBPH nhận diện.

⚠️ Đảm bảo bạn đã chuẩn bị xong thư mục dataset/ và file label_map.pkl đúng định dạng.

📽️ Kết quả đầu ra
Sau khi chạy, kết quả sẽ được lưu trong thư mục output/:

output_facenet.mp4: kết quả nhận diện bằng FaceNet

output_video_cnn.mp4: kết quả nhận diện bằng CNN

webcam.mp4: nhận diện trực tiếp từ webcam
