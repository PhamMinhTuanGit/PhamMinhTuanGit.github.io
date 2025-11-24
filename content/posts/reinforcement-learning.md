---
title: "Các kiến thức cơ bản về Reinforcement Learning - Phần 1"
date: 2025-11-24
draft: false
tags: ["Reinforcement Learning"]
math: true
---
# Lời nói đầu
Xin chào các bạn đã đến vứi blog của mình. Mình là Minh Tuấn, và đây là chiếc blog nưi mình chia sẻ những gì mình đã học, mong rằng nó sẽ giúp ích cho mọi người. Nào, bây giờ chúng ta hãy đến với nội dung của ngày hôm nay nhé. 
# Khái niệm Học tăng cường (Reinforcement Learning)
Theo [Wikipedia](https://vi.wikipedia.org/wiki/H%E1%BB%8Dc_t%C4%83ng_c%C6%B0%E1%BB%9Dng), học tăng cường có thể hiểu như sau:
> **Trong ngành khoa học máy tính, học tăng cường (tiếng Anh: reinforcement learning) là một lĩnh vực con của học máy, nghiên cứu cách thức một agent trong một môi trường nên chọn thực hiện các hành động nào để cực đại hóa một khoản thưởng (reward) nào đó về lâu dài. Các thuật toán học tăng cường cố gắng tìm một chiến lược ánh xạ các trạng thái của thế giới tới các hành động mà agent nên chọn trong các trạng thái đó.**

Và từ định nghĩa trên, các bạn có thể nhận ra rằng Học tăng cường có 3 hành phần cơ bản đó là: 
1. $S$ - Tập các trạng thái của môi trường
2. $A$ - Tập các cách hành động của tác nhân (agent)
3. $R$ - Tập các "điểm thưởng" (reward)

