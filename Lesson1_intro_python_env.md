<style>
@keyframes gradientAnimation {
  0% {background-position: 0% 50%;}
  50% {background-position: 100% 50%;}
  100% {background-position: 0% 50%;}
}
.main-title {
  display: block;
  text-align: center;
  font-weight: bold;
  font-size: 2.5em;
  padding: 20px;
  margin: 20px 0;
  color: white;
  background: linear-gradient(45deg, #4A00E0, #8E2DE2, #4A00E0);
  background-size: 200% 200%;
  animation: gradientAnimation 10s ease infinite;
  border-radius: 10px;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
.section-header {
  position: relative;
  color: #1a237e;
  font-size: 1.5em;
  font-weight: bold;
  margin: 40px 0 20px 0;
  padding-bottom: 10px;
  letter-spacing: 1px;
  text-transform: uppercase;
  border-bottom: 2px solid #e0e0e0;
}
.section-header::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 80px;
  height: 2px;
  background: linear-gradient(90deg, #3f51b5, #2196f3);
}
.section-header .section-icon {
  display: inline-block;
  margin-right: 10px;
  font-size: 1.2em;
  vertical-align: middle;
}
.section-header .section-number {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 30px;
  height: 30px;
  background: linear-gradient(135deg, #3f51b5, #2196f3);
  color: white;
  border-radius: 50%;
  font-size: 0.7em;
  margin-right: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.2);
}
.subsection-header {
  color: #283593;
  font-size: 1.3em;
  font-weight: bold;
  margin: 30px 0 15px 0;
  padding-left: 15px;
  border-left: 4px solid #3f51b5;
}
.tip-box {
  position: relative;
  margin: 25px 0;
  padding: 20px 20px 20px 70px;
  border-radius: 10px;
  background: linear-gradient(135deg, rgba(76, 175, 80, 0.1), rgba(76, 175, 80, 0.05));
  border-left: 5px solid #4caf50;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}
.tip-box::before {
  content: "💡";
  position: absolute;
  left: 20px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 2em;
  color: #4caf50;
  background: rgba(255, 255, 255, 0.7);
  width: 40px;
  height: 40px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}
</style>

<div class="main-title">🐍 Lesson 1: Giới thiệu Python & Môi trường Làm Việc</div>



<div class="section-header">
  <span class="section-number">1</span>
  <span class="section-icon">💻</span> Cài đặt Python và Môi trường Làm Việc
</div>

<div class="tip-box">
  <strong>Lý thuyết:</strong> Python là ngôn ngữ lập trình phổ biến, dễ học, mạnh mẽ cho phân tích dữ liệu, AI, web, automation.<br>
  <strong>IDE/Editor</strong> như VSCode giúp viết, chạy, debug code hiệu quả, hỗ trợ nhiều extension.<br>
  <strong>Extension</strong> giúp tăng năng suất, hỗ trợ code Python, Jupyter, kiểm tra lỗi, chạy notebook.<br>
  <strong>Google Colab</strong> là môi trường cloud miễn phí, không cần cài đặt, phù hợp thử nghiệm nhanh.
</div>

<div class="tip-box">
  <strong>Python 3.13:</strong> Tải tại <a href="https://www.python.org/downloads/">python.org</a> và cài đặt theo hướng dẫn.
</div>

- **VSCode:** Tải tại <a href="https://code.visualstudio.com/">code.visualstudio.com</a>
- **Extension nên cài:**
  - Python (Microsoft)
  - Jupyter
  - Pylance
  - Code Runner
  - Jupyter Keymap, Jupyter Notebook Renderers
- **Google Colab:** Truy cập <a href="https://colab.research.google.com/">colab.research.google.com</a> để code Python online, không cần cài đặt.



<div class="section-header">
  <span class="section-number">2</span>
  <span class="section-icon">🔤</span> Cú pháp Python cơ bản
</div>

<div class="tip-box">
  <strong>Lý thuyết:</strong> 
  <ul>
    <li><strong>Biến</strong> dùng để lưu trữ giá trị, có thể thay đổi trong quá trình chạy chương trình.</li>
    <li><strong>Kiểu dữ liệu cơ bản</strong>: số nguyên (int), số thực (float), chuỗi (str), logic (bool).</li>
    <li><strong>Cấu trúc dữ liệu</strong>: list (danh sách), tuple (bộ giá trị không đổi), dict (từ điển key-value).</li>
    <li><strong>Vòng lặp</strong> giúp lặp lại thao tác nhiều lần (for, while).</li>
    <li><strong>Câu lệnh điều kiện</strong> kiểm tra điều kiện đúng/sai để quyết định luồng chạy.</li>
    <li><strong>Hàm</strong> giúp đóng gói đoạn code thực hiện một chức năng, có thể tái sử dụng.</li>
  </ul>
</div>

<div class="subsection-header">🔤 Biến và kiểu dữ liệu</div>

```python
# Khai báo biến
x = 10
name = "Alice"
pi = 3.14
is_active = True

# Kiểu dữ liệu
print(type(x))        # <class 'int'>
print(type(name))     # <class 'str'>
print(type(pi))       # <class 'float'>
print(type(is_active))# <class 'bool'>
```

<div class="subsection-header">📚 Cấu trúc dữ liệu: list, tuple, dict</div>

```python
# List
lst = [1, 2, 3]
# Tuple
tpl = (1, 2, 3)
# Dict
dct = {"a": 1, "b": 2}

print(lst[0], tpl[1], dct["a"])
```

<div class="subsection-header">🔁 Vòng lặp và điều kiện</div>

```python
# Vòng lặp for
for i in range(5):
    print(i)

# Vòng lặp while
n = 0
while n < 3:
    print(n)
    n += 1

# Câu lệnh điều kiện
x = 7
if x > 5:
    print("Lớn hơn 5")
else:
    print("Không lớn hơn 5")
```

<div class="subsection-header">🔧 Hàm trong Python</div>

```python
def greet(name):
    return f"Hello, {name}!"

print(greet("Bob"))
```


<div class="section-header">
  <span class="section-number">3</span>
  <span class="section-icon">📝</span> Bài tập thực hành
</div>

<div class="tip-box">
  <strong>Lý thuyết:</strong> Bài tập giúp củng cố kiến thức về biến, kiểu dữ liệu, cấu trúc dữ liệu, hàm, vòng lặp, điều kiện.<br>
  Thực hành là cách tốt nhất để ghi nhớ cú pháp và tư duy lập trình Python.
</div>
<ul style="margin: 0 0 20px 20px; color: #283593; font-size: 1.1em;">
  <li>Khai báo 3 biến với 3 kiểu dữ liệu khác nhau và in ra màn hình.</li>
  <li>Tạo list gồm 5 số, tính tổng các phần tử.</li>
  <li>Viết hàm kiểm tra số chẵn/lẻ.</li>
  <li>Viết vòng lặp in ra các số từ 1 đến 10 chia hết cho 3.</li>
</ul>


<div class="section-header">
  <span class="section-number">4</span>
  <span class="section-icon">✅</span> Đáp án mẫu
</div>

<div class="tip-box">
  <strong>Giải thích đáp án:</strong><br>
  <ul>
    <li><strong>Khai báo biến</strong>: Gán giá trị cho biến với các kiểu khác nhau.</li>
    <li><strong>Tính tổng list</strong>: Sử dụng hàm <code>sum()</code> để tính tổng các phần tử trong list.</li>
    <li><strong>Hàm kiểm tra chẵn/lẻ</strong>: Sử dụng toán tử chia dư <code>%</code> để xác định số chẵn/lẻ.</li>
    <li><strong>Vòng lặp chia hết cho 3</strong>: Duyệt từ 1 đến 10, kiểm tra điều kiện chia hết cho 3.</li>
  </ul>
</div>

```python
# 1. Khai báo biến
x = 5
name = "John"
flag = False
print(x, name, flag)

# 2. Tổng list
lst = [1, 2, 3, 4, 5]
print(sum(lst))

# 3. Hàm kiểm tra chẵn/lẻ
def is_even(n):
    return n % 2 == 0
print(is_even(4), is_even(5))

# 4. Vòng lặp chia hết cho 3
for i in range(1, 11):
    if i % 3 == 0:
        print(i)
```
<div class="section-header">
  <span class="section-number">5</span>
  <span class="section-icon">🎯</span> Tổng kết bài học
</div>

<div class="tip-box">
  <strong>Tóm tắt:</strong> Bạn đã làm quen với Python, môi trường làm việc, cú pháp cơ bản, cấu trúc dữ liệu, hàm, vòng lặp và điều kiện. Đây là nền tảng quan trọng để học các chủ đề phân tích dữ liệu nâng cao hơn.
</div>