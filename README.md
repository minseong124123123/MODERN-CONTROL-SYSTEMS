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

---

### p3.12

(a)

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/7cd98979128163db65ca1f616cd258e8d82d0b24/P3.12(a).png)

(b)

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/755b279d1094ab4e97b59f8092929391a083eaa9/P3.12(b).png)

역행렬과 역라플라스를 매트랩으로 하면

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

역행렬 한 행렬:

$$
\begin{bmatrix}
\frac{s^2 + 12s + 44}{s^3 + 12s^2 + 44s - 48} & \frac{-(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{-1}{s^3 + 12s^2 + 44s - 48} \\
\frac{-48}{s^3 + 12s^2 + 44s - 48} & \frac{s(s + 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s}{s^3 + 12s^2 + 44s - 48} \\
\frac{-(48s)}{s^3 + 12s^2 + 44s - 48} & \frac{-4(11s - 12)}{s^3 + 12s^2 + 44s - 48} & \frac{s^2}{s^3 + 12s^2 + 44s - 48}
\end{bmatrix}
$$

역라플라스

$$
\ Φ(t) =  
\begin{bmatrix}
3e^{-2t} - 3e^{-4t} + e^{-6t} & \frac{5e^{-2t}}{4} - 2e^{-4t} + \frac{3e^{-6t}}{4} & \frac{e^{-2t}}{8} - \frac{e^{-4t}}{4} + \frac{e^{-6t}}{8} \\
12e^{-4t} - 6e^{-2t} - 6e^{-6t} & 8e^{-4t} - \frac{5e^{-2t}}{2} - \frac{9e^{-6t}}{2} & e^{-4t} - \frac{e^{-2t}}{4} - \frac{3e^{-6t}}{4} \\
12e^{-2t} - 48e^{-4t} + 36e^{-6t} & 5e^{-2t} - 32e^{-4t} + 27e^{-6t} & \frac{e^{-2t}}{2} - 4e^{-4t} + \frac{9e^{-6t}}{2}
\end{bmatrix}
$$   

---

### p3.17

![이미지 설명](https://github.com/minseong124123123/modern-control-systems-3/blob/d260490f4e16e59d206724be8ebc7e97d764f754/p3.17.png)

매트랩으로 진행하면
```
syms s;


A = [(s - 3)*(s - 10)/(s^3 - 14*s^2 + 37*s + 20), (s - 11)/(s^3 - 14*s^2 + 37*s + 20), -(s - 3)/(s^3 - 14*s^2 + 37*s + 20);
     4*(s - 10)/(s^3 - 14*s^2 + 37*s + 20), (s^2 - 11*s + 8)/(s^3 - 14*s^2 + 37*s + 20), -4/(s^3 - 14*s^2 + 37*s + 20);
    -2*(s - 5)/(s^3 - 14*s^2 + 37*s + 20), (s - 3)/(s^3 - 14*s^2 + 37*s + 20), -(-s^2 + 4*s + 1)/(s^3 - 14*s^2 + 37*s + 20)];

row_vector = [1, 0, 0];

column_vector = [0; 0; 4];

result_1 = row_vector * A;

final_result = result_1 * column_vector;

disp('결과:');
disp(simplify(final_result));

```

## 최종 결과

$$
-\frac{4(s - 3)}{s^3 - 14s^2 + 37s + 20}
$$


