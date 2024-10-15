# MODERN-CONTROL-SYSTEMS
homework3

## 제어공학 과제3                    
##### 2020732066 최민승

### p3.1

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/331ecd8eeced5b047ffa647d7b3e3ff9347dc8e1/P3.1.png)

---

### p3.3

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/594a6742d7ae689c66514788d456d8abf0f69ba9/P3.3.png)

---

### P3.5

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/b9d866c0032cbec9dd04dfed40658f6100db0781/P3.5.png)
$$
x(t) = \frac{2 \sin\left(\frac{t\sqrt{-b^2 + 4km}}{2m}\right) \exp\left(-\frac{bt}{2m}\right)}{\sqrt{-b^2 + 4km}}
$$

---

### p3.12

(a)

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/7cd98979128163db65ca1f616cd258e8d82d0b24/P3.12(a).png)

(b)

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/755b279d1094ab4e97b59f8092929391a083eaa9/P3.12(b).png)

역행렬을 먼저하면

$$
\begin{bmatrix}
\frac{s^2 + 12s + 44}{s^3 + 12s^2 + 44s - 48} & \frac{-(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{-1}{s^3 + 12s^2 + 44s - 48} \\
\frac{-48}{s^3 + 12s^2 + 44s - 48} & \frac{s(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s}{s^3 + 12s^2 + 44s - 48} \\
\frac{-(48s)}{s^3 + 12s^2 + 44s - 48} & \frac{-4(11s - 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s^2}{s^3 + 12s^2 + 44s - 48}
\end{bmatrix}
$$

```
syms s t;  

A = [s, 1, 0; 
     0, s, -1; 
     48, 44, s+12];

A_inv = inv(A);

disp('The inverse of matrix A is:');
disp(A_inv);

A_inv_ilaplace = ilaplace(A_inv, s, t); 

disp('The inverse Laplace transform of matrix A_inv is:');
disp(A_inv_ilaplace);

```

$$
\begin{bmatrix}
\frac{s^2 + 12s + 44}{s^3 + 12s^2 + 44s - 48} & \frac{-(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{-1}{s^3 + 12s^2 + 44s - 48} \\
\frac{-48}{s^3 + 12s^2 + 44s - 48} & \frac{s(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s}{s^3 + 12s^2 + 44s - 48} \\
\frac{-(48s)}{s^3 + 12s^2 + 44s - 48} & \frac{-4(11s - 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s^2}{s^3 + 12s^2 + 44s - 48}
\end{bmatrix}
$$


---

### p3.17

![이미지 설명](https://github.com/minseong124123123/modern-contreol-systems/blob/1d4620c873e240fd89365f4a429e9479e6e81bab/P2.37.png)
