# ISA — Probability Distributions Presentation Template

This repository provides a simple LaTeX template for team members to create consistent and professional presentations on **Probability Distributions**.

---
## 1. **Mục tiêu của project:**

* Tạo một tài liệu LaTeX tổng hợp công thức, hàm mật độ xác suất (PDF/PMF), kỳ vọng, phương sai, và mối quan hệ giữa các phân phối.
* Dễ dàng tra cứu và so sánh các phân phối trong thống kê và học máy.

Dự án sẽ bao gồm phần trình bày chi tiết và công thức tham chiếu (distribution reference) của các phân phối xác suất phổ biến sau:

| Nhóm                   | Phân phối                                                 | Ký hiệu / Ghi chú                          |
| ---------------------- | --------------------------------------------------------- | ------------------------------------------ |
| **Phân phối rời rạc**  | - Phân phối nhị thức (Binomial Distribution)              | ( X \sim \text{Bin}(n, p) )                |
|                        | - Phân phối Poisson (Poisson Distribution)                | ( X \sim \text{Pois}(\lambda) )            |
|                        | - Phân phối nhị thức âm (Negative Binomial Distribution)  | ( X \sim \text{NegBin}(r, p) )             |
|                        | - Phân phối đa thức (Multinomial Distribution)            | ( X \sim \text{Mult}(n, \mathbf{p}) )      |
| **Phân phối liên tục** | - Phân phối đều (Uniform Distribution)                    | ( X \sim U(a, b) )                         |
|                        | - Phân phối chuẩn (Normal Distribution)                   | ( X \sim \mathcal{N}(\mu, \sigma^2) )      |
|                        | - Phân phối Gamma (Gamma Distribution)                    | ( X \sim \text{Gamma}(k, \theta) )         |
|                        | - Phân phối Gamma nghịch đảo (Inverse Gamma Distribution) | ( X \sim \text{InvGamma}(\alpha, \beta) )  |
|                        | - Phân phối Beta (Beta Distribution)                      | ( X \sim \text{Beta}(\alpha, \beta) )      |
|                        | - Phân phối location-scale t-Student                      | ( X \sim t_\nu(\mu, \sigma) )              |
|                        | - Phân phối Log-normal (Lognormal Distribution)           | ( X \sim \text{Lognormal}(\mu, \sigma^2) ) |
|                        | - Phân phối mũ (Exponential Distribution)                 | ( X \sim \text{Exp}(\lambda) )             |
|                        | - Phân phối Cauchy (Cauchy Distribution)                  | ( X \sim \text{Cauchy}(\mu, \gamma) )      |
|                        | - Phân phối Dirichlet (Dirichlet Distribution)            | ( X \sim \text{Dir}(\boldsymbol{\alpha}) ) |

## **2. Cài Đặt LaTeX Workshop Trên VSCode**

Ta sẽ cần phải cài đặt các phần sau:
1. VsCode
2. texlive-latex-recommended

### 🔧 Bước 1: Cài đặt công cụ biên dịch LaTeX
- **Windows:** Cài [MiKTeX](https://miktex.org/download)
- **macOS:** Cài [MacTeX](https://tug.org/mactex/)
- **Linux (Ubuntu/Debian):**
  ```bash
  sudo apt update
  sudo apt install texlive-latex-recommended
  ```

### 🧩 Bước 2: Cài đặt tiện ích mở rộng **LaTeX Workshop**

1. Mở VSCode → nhấn `Ctrl + Shift + X` để mở tab Extensions
2. Gõ **LaTeX Workshop**
3. Nhấn **Install**

### 📂 Bước 3: clone repo này về thư mục làm việc

1. Tạo một thư mục để làm việc, sau đó dùng git clone để clone về
2. Trong đó, tạo file `main.tex`
3. Dán đoạn mã mẫu sau để kiểm tra:

   ```latex
   \documentclass{article}
   \begin{document}
   Hello LaTeX!  
   \LaTeX\ is working perfectly.
   \end{document}
   ```
4. Nhấn **Ctrl + Alt + B** (hoặc nhấn biểu tượng “Build LaTeX project” ở thanh công cụ) để biên dịch thành file PDF.

---





