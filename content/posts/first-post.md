---
title: "Ứng dụng LQR trong Điều khiển cân bằng"
date: 2023-11-23
draft: false
tags: ["Control Theory", "Python", "LQR"]
math: true
---

Chào mừng đến với blog của tôi. Đây là ví dụ về cách viết bài kỹ thuật.

## 1. Mô hình toán học
Phương trình trạng thái của hệ thống (State-space):

$\dot{x} = Ax + Bu$

Trong đó hàm mục tiêu $J$ cần tối thiểu hóa là:

$J = \int_{0}^{\infty} (x^T Q x + u^T R u) dt$

## 2. Giải thuật (Python)
Dưới đây là code Python để giải phương trình Riccati:

```python
import numpy as np
import scipy.linalg as la

def lqr(A, B, Q, R):
    """Giải phương trình đại số Riccati"""
    X = np.matrix(la.solve_continuous_are(A, B, Q, R))
    # Tính toán gain matrix K
    K = np.matrix(la.inv(R) * (B.T * X))
    eigVals, eigVecs = la.eig(A - B * K)
    return K, X, eigVals

A = np.array([[0, 1], [0, -1]])
B = np.array([[0], [1]])
# ... code tiếp theo