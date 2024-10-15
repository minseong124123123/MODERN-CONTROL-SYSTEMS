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

![이미지 설명](https://github.com/minseong124123123/modern-contreol-systems/blob/405f79abac5993ce8b14e41386df7e4c4308d5c9/P2.26.png)



$$
\begin{bmatrix}
\frac{s^2 + 12s + 44}{s^3 + 12s^2 + 44s - 48} & \frac{-(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{-1}{s^3 + 12s^2 + 44s - 48} \\
\frac{-48}{s^3 + 12s^2 + 44s - 48} & \frac{s(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s}{s^3 + 12s^2 + 44s - 48} \\
\frac{-(48s)}{s^3 + 12s^2 + 44s - 48} & \frac{-4(11s - 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s^2}{s^3 + 12s^2 + 44s - 48}
\end{bmatrix}
$$

```
syms s; 

A = [s, 1, 0; 
     0, s, -1; 
     48, 44, s+12];

A_inv = inv(A);

disp('The inverse of matrix A is:');
disp(A_inv);
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
