# File Bài tập lý thuyết lần 3

## Câu 1: Tìm một ví dụ cho mệnh đề sau “Không phải mọi công thức đều có thể biểu diễn dưới dạng câu Horn”
- Câu **Horn** là một mệnh đề tuyển (disjunction) của các literal, trong đó tối đa một literal là dương.

### 1. A &or; B
Công thức này không thể biểu diễn dưới dạng câu Horn vì nó chứa hai literal dương.

### 2. (A∨B)∧(¬A∨C)∧(¬B∨C)
- (A∨B): Mệnh đề con này chứa hai literal dương (A và B), do đó không phải là một câu Horn.
- (¬A∨C): Mệnh đề con này chứa một literal dương (C), thỏa mãn định nghĩa câu Horn.
- (¬B∨C): Tương tự như mệnh đề con thứ hai, mệnh đề này cũng thỏa mãn định nghĩa câu Horn.

#### Vì công thức (A∨B)∧(¬A∨C)∧(¬B∨C) chứa mệnh đề con (A∨B) không phải là câu Horn, nên toàn bộ công thức này không phải là một câu Horn.
---

## Câu 2: Chứng minh luật phân giải là luật suy diễn tổng quát, bao gồm luật Modus Ponens, Modus Tollens, luật bắc cầu

**Luật Phân Giải:**

* Luật phân giải được áp dụng để kết hợp hai mệnh đề con có chứa một literal đối nghịch nhau (ví dụ: $\alpha$ và $\neg \alpha$). 
* Kết quả của luật phân giải là một mệnh đề con mới (resolvent) được tạo bằng cách loại bỏ các literal đối nghịch và kết hợp các literal còn lại từ hai mệnh đề con ban đầu.

**- Modus Ponens:**
### $\frac{\alpha \rightarrow \beta \quad \alpha}{\beta}$

- Chứng minh bằng luật phân giải:
    - Biểu diễn $\alpha \rightarrow \beta$ dưới dạng $\neg \alpha \lor \beta$.
    - Áp dụng luật phân giải cho $\alpha$ và $\neg \alpha \lor \beta$ (Literal 
α và 
¬α là đối nghịch nhau, nên chúng bị loại bỏ, để lại 
β.):
      ### $\frac{\neg \alpha \lor \beta \quad \alpha}{\beta}$

Kết quả này tương ứng với Modus Ponens, 
    bởi vì từ "Nếu $\alpha$ thì $\beta$" và việc biết $\alpha$ là đúng, ta suy ra rằng $\beta$ phải đúng.

**- Modus Tollens:**
### $\frac{\alpha \rightarrow \beta \quad \neg \beta}{\neg \alpha}$

- Chứng minh bằng luật phân giải:
    - Biểu diễn $\alpha \rightarrow \beta$ dưới dạng $\neg \alpha \lor \beta$.
    - Áp dụng luật phân giải cho $\neg \beta$ và $\neg \alpha \lor \beta$:
      ### $\frac{\neg \alpha \lor \beta \quad \neg \beta}{\neg \alpha}$

Đây chính là bản chất của Modus Tollens: 
    từ "Nếu $\alpha$ thì $\beta$" và biết rằng $\beta$ là sai, chúng ta suy ra rằng $\alpha$ cũng phải sai.

**- Luật Bắc Cầu:**
Luật bắc cầu cho phép kết luận $ \alpha \rightarrow \gamma $ từ hai mệnh đề $\alpha \rightarrow \beta $ và $ \beta \rightarrow \gamma$.

### $\frac{\alpha \rightarrow \beta \quad \beta \rightarrow \gamma}{\alpha \rightarrow \gamma}$

- Chứng minh bằng luật phân giải:
    - Biểu diễn $\alpha \rightarrow \beta$ dưới dạng $\neg \alpha \lor \beta$.
    - Biểu diễn $\beta \rightarrow \gamma$ dưới dạng $\neg \beta \lor \gamma$.
    - Áp dụng luật phân giải cho $\neg \beta \lor \gamma$ và $\neg \alpha \lor \beta$:
      ### $\frac{\neg \alpha \lor \beta \quad \neg \beta \lor \gamma}{\neg \alpha \lor \gamma}$
    - Biểu diễn $\neg \alpha \lor \gamma$ dưới dạng $\alpha \rightarrow \gamma$.

Điều này thể hiện tính chất bắc cầu: Nếu "Nếu $\alpha$ thì $\beta$" và "Nếu $\beta$ thì $\gamma$" đều đúng,
 thì "Nếu $\alpha$ thì $\gamma$" cũng đúng.

### Do đó có thể kết luận rằng luật phân giải là luật suy diễn tổng quát, bao gồm luật Modus Ponens, Modus Tollens, luật bắc cầu
---
