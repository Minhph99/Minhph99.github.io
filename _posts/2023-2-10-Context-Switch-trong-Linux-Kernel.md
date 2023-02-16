---
layout: post
title: Context switch trong trong Linux Kernel.
gh-repo: 
gh-badge: [star, fork, follow]
tags: [kernel, embedded, context switch]
---

Như bài viết trước, chúng ta đã tìm hiểu về các loại context trong Linux Kernel bao gồm: ```process context``` và ```interrupt context```. Trong bài nay, chúng ta sẽ tìm hiểu về thế nào là context switch trong Linux Kernel và cơ chế hoạt động của nó.

### 1. Context switch là gì ?
Để kiểm soát việc thực hiện các tiến trình, kernel phải có khả năng tạm dừng việc thực hiện tiến trình đang chạy trên CPU và tiếp tục thực hiện một số tiến trình khác đã bị đình chỉ trước đó. Hoạt động này có thể gọi là ```process switch, task switch hoặc context switch```. Các phần tiếp theo mô tả các yếu tố của quá trình chuyển đổi này trong Linux.