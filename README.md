# Dự đoán giá xe ô tô bằng Machine Learning

**Sinh viên thực hiện:** Lương Thị Linh  
**Mã số sinh viên:** 22028202  
**Môn học**: Khoa học dữ liệu - INT 3416 2

---

##  Mục Tiêu Đề Tài

Xây dựng mô hình học máy để dự đoán giá bán của xe ô tô dựa trên các đặc trưng kỹ thuật và thông số kỹ thuật. Mục tiêu là tạo ra mô hình có khả năng dự đoán giá với sai số thấp nhất, hỗ trợ người dùng hoặc doanh nghiệp trong việc định giá xe.

---

##  Dữ Liệu Đầu Vào

Bộ dữ liệu bao gồm **26 thuộc tính** được chia thành:

###  Numerical Features (16):
| Tên thuộc tính     | Mô tả |
|-------------------|-------|
| `car_ID` | ID xe |
| `symboling` | Đánh giá rủi ro (Acturian scale: -3 đến +3) |
| `wheelbase` | Chiều dài cơ sở (inch) |
| `carlength` | Chiều dài xe (inch) |
| `carwidth` | Chiều rộng xe (inch) |
| `carheight` | Chiều cao xe (inch) |
| `curbweight` | Trọng lượng không tải (pounds) |
| `enginesize` | Dung tích động cơ (in³) |
| `boreratio` | Tỷ lệ đường kính hành trình xy-lanh |
| `stroke` | Hành trình piston |
| `compressionratio` | Tỷ số nén |
| `horsepower` | Công suất (mã lực) |
| `peakrpm` | Vòng quay tối đa (rpm) |
| `citympg` | Tiêu hao nhiên liệu nội đô (dặm/gallon) |
| `highwaympg` | Tiêu hao nhiên liệu đường trường (dặm/gallon) |
| `price` | **Mục tiêu cần dự đoán** – Giá bán (USD) |

### Categorical Features (10):
| Tên thuộc tính     | Mô tả |
|-------------------|-------|
| `fueltype` | Loại nhiên liệu (gas/diesel) |
| `aspiration` | Kiểu hút khí (standard/turbo) |
| `doornumber` | Số cửa (two/four) |
| `carbody` | Kiểu thân xe |
| `drivewheel` | Kiểu dẫn động |
| `enginelocation` | Vị trí động cơ |
| `enginetype` | Loại động cơ |
| `cylindernumber` | Số xy-lanh |
| `fuelsystem` | Hệ thống nhiên liệu |

---

##  Công Nghệ Sử Dụng

- **Ngôn ngữ**: Python
- **Môi trường phát triển**: Jupyter Notebook  
- **Thư viện**:
  - `pandas`, `numpy`: xử lý và phân tích dữ liệu
  - `matplotlib`, `seaborn`: trực quan hóa
  - `scikit-learn`: xây dựng và đánh giá mô hình
---

## Quy Trình Thực Hiện

1. **Tiền xử lý dữ liệu**
2. **Trực quan hóa và phân tích (EDA)**
3. **Xây dựng và huấn luyện mô hình**
4. **Đánh giá mô hình**
---

##  Kết Quả Đánh Giá Mô Hình

| Mô hình              | MAE           | RMSE          | R² Score |
|----------------------|---------------|---------------|----------|
| Linear Regression    | 2,123.85 USD  | 2,750.38 USD  | 0.858    |
| Decision Tree        | 1,156.29 USD  | 1,671.64 USD  | 0.948    |
| Random Forest        | 1,034.29 USD  | 1,407.66 USD  | **0.963** |

**Random Forest là mô hình tốt nhất** với sai số thấp và độ chính xác cao.

---
