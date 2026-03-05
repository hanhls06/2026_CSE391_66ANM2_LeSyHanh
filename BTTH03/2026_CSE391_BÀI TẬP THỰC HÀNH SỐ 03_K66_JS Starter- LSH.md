
## BTTH03: JS nền tảng, DOM & Sự kiện

**Đối tượng:** Sinh viên chưa học lý thuyết JavaScript

---

## 1. MỤC TIÊU HỌC TẬP

Sau buổi lab, sinh viên có thể:

- Mô tả được JavaScript là gì, chạy ở đâu, khác HTML/CSS ở điểm nào.
- Viết được các đoạn JS đơn giản với:
  - Biến, kiểu dữ liệu cơ bản (number, string, boolean),
  - Cú pháp lệnh, toán tử đơn giản,
  - Cấu trúc điều khiển if/else, vòng lặp đơn giản,
  - Hàm (function) có tham số và giá trị trả về.
- Thao tác được với DOM:
  - Lấy phần tử bằng `document.getElementById`,
  - Thay đổi nội dung văn bản, kiểu dáng (style),
  - Lắng nghe và xử lý một số sự kiện cơ bản: `click`, `input`.
- Nhận biết jQuery là một thư viện hỗ trợ thao tác DOM/sự kiện (ở mức nhận diện, chưa cần sử dụng thành thạo).

---

## 2. CẤU TRÚC THỜI GIAN BUỔI LAB
- 03 tiết thực hành.

---

## 3. HOẠT ĐỘNG 1 (45’): GIỚI THIỆU JS & CÚ PHÁP CƠ BẢN

### 3.1. Chuẩn bị file HTML & JS

Tạo file `lab-js-basic.html`:

```html
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Lab JS Cơ bản</title>
</head>
<body>
  <h1>Khám phá JavaScript</h1>
  <p id="welcome">Chưa có JavaScript...</p>
  <button id="runBtn">Nhấn để chạy JS</button>

  <script src="main.js"></script>
</body>
</html>
```

Tạo file `main.js`:

```js
console.log("Hello from JavaScript!");
```


---

### 3.2. Nhiệm vụ cho sinh viên

#### Bước 1: Mở file \& Quan sát bằng Console

1. Mở `lab-js-basic.html` trong trình duyệt (Chrome/Edge/…).
2. Mở DevTools → tab **Console**.
3. Quan sát thông báo xuất hiện.

> Câu hỏi:
> - Em thấy dòng thông báo nào trong console?
Em thấy :
Trong console xuất hiện dòng:

Hello from JavaScript!
> - Điều này cho em biết JavaScript đang làm gì khi trang web được tải?

---Điều này cho thấy file JavaScript đã được tải và thực thi khi trang web được mở, và lệnh console.log() đã in thông báo ra Console của trình duyệt.

#### Bước 2:  “JavaScript là gì?” (Tra cứu nhanh)

Sử dụng 1–2 nguồn tài liệu (vd. W3Schools, freeCodeCamp, …), tóm tắt:

> a) JavaScript chạy ở đâu? (Trình duyệt / Server / Cả hai?)
-JavaScript có thể chạy ở cả hai:

+Trình duyệt (client-side): chạy trực tiếp trên trình duyệt như Chrome, Edge để tạo tương tác trên trang web.

+Server (server-side): chạy trên máy chủ thông qua môi trường như Node.js để xử lý logic backend.

> b) HTML, CSS, JavaScript mỗi phần chịu trách nhiệm chính về điều gì?

>
> - HTML: Dùng để tạo cấu trúc và nội dung của trang web (tiêu đề, đoạn văn, hình ảnh…).
> - CSS: Dùng để thiết kế giao diện và định kiểu cho trang web (màu sắc, font chữ, bố cục…).
> - JavaScript: Dùng để tạo chức năng và tương tác cho trang web, ví dụ: xử lý sự kiện, thay đổi nội dung HTML, thay đổi CSS, phản hồi khi người dùng bấm nút hoặc nhập dữ liệu.

---

#### Bước 3: Thử nghiệm biến \& kiểu dữ liệu trong Console

Trong tab Console, gõ từng dòng sau và ghi lại kết quả:

```js
let age = 20;
const name = "An";
let isStudent = true;

typeof age;
typeof name;
typeof isStudent;

1 + 2 * 3;
"Hello " + "world";
```

> Câu hỏi:
> - Kết quả `typeof age` là gì?
➡"number"
> - Kết quả `typeof name` là gì?
➡ "string"
> - Kết quả `typeof isStudent` là gì?
➡ "boolean"
> - Em hãy tự mô tả ngắn gọn:
>   - `number` là: kiểu dữ liệu dùng để lưu các giá trị số (ví dụ: 1, 20, 3.14...)
>   - `string` là: kiểu dữ liệu dùng để lưu chuỗi ký tự hoặc văn bản (ví dụ: "Hello", "An")..
>   - `boolean` là: kiểu dữ liệu chỉ có hai giá trị đúng hoặc sai (true hoặc false).
---

#### Bước 4: Viết đoạn script tính tuổi

Mở file `main.js`, viết thêm:

```js
let name = "An";
let yearOfBirth = 2005;
let currentYear = 2026;
let age = currentYear - yearOfBirth;

console.log("Xin chào, mình là " + name + ", năm nay mình " + age + " tuổi.");
```

Sau đó:

1. Đổi giá trị `name`, `yearOfBirth` thành thông tin của chính em.
2. Reload trang \& quan sát console.

> Câu hỏi:
> - Dòng log hiển thị gì sau khi em sửa thông tin?
Nếu sửa thành:

let name = "Hanh";
let yearOfBirth = 2006;

Thì Console sẽ hiển thị:

Xin chào, mình là Hanh, năm nay mình 19 tuổi.
> - Nếu em quên dấu `;` hoặc quên dấu `+`, điều gì xảy ra? Trình duyệt báo lỗi thế nào?
  - Nếu quên dấu ;:
Thường không gây lỗi nghiêm trọng, vì JavaScript có thể tự hiểu điểm kết thúc câu lệnh.

  -Nếu quên dấu +:
JavaScript sẽ báo lỗi cú pháp (SyntaxError) trong Console, vì chuỗi và biến không được nối đúng cách nên chương trình không chạy.
---

#### Bước 5: Phản tư nhanh (Reflection)

> - Điều thú vị nhất em vừa khám phá được về console là gì?
➡ Console cho phép chạy và kiểm tra mã JavaScript trực tiếp, giúp xem kết quả ngay lập tức và dễ dàng phát hiện lỗi trong chương trình
> - Em gặp lỗi cú pháp nào? Em đã xử lý bằng cách nào (tự sửa, hỏi bạn, đọc lỗi, tìm Google, …)?
➡ Em gặp lỗi thiếu dấu + khi nối chuỗi trong lệnh console.log. Em đã đọc thông báo lỗi trong Console và sửa lại cú pháp cho đúng.
---

## 4. HOẠT ĐỘNG 2 (40’): CẤU TRÚC ĐIỀU KHIỂN \& HÀM

### 4.1. Chuẩn bị file logic (hoặc viết tiếp trong main.js)

Ví dụ đoạn mã:

```js
// TODO: Đổi giá trị score và quan sát kết quả
let score = 7.5;

// TODO: Dự đoán điều kiện if/else đang làm gì, rồi chạy thử
if (score >= 8) {
  console.log("Giỏi");
} else if (score >= 6.5) {
  console.log("Khá");
} else if (score >= 5) {
  console.log("Trung bình");
} else {
  console.log("Yếu");
}

// TODO: Viết hàm tính điểm trung bình 3 môn
function tinhDiemTrungBinh(m1, m2, m3) {
  let avg = (m1 + m2 + m3) / 3;
  return avg;
}

// Gợi ý dùng thử hàm trong console:
// tinhDiemTrungBinh(8, 7, 9);
```


---

### 4.2. Nhiệm vụ cho sinh viên

#### Bước 1: Đoán trước – chạy sau

> a) Nếu `score = 9`, em dự đoán console sẽ in: Giỏi........................
> b) Nếu `score = 6`, em dự đoán console sẽ in: Trung bình........................

Sau đó:

1. Thay `score = 9`, reload trang hoặc chạy file và kiểm tra console.
2. Thay `score = 6`, kiểm tra lại.

> So sánh dự đoán và kết quả thực tế:
> - Trường hợp `score = 9`: Dự đoán vs Thực tế: .....Giỏi - Giỏi...................
> - Trường hợp `score = 6`: Dự đoán vs Thực tế: .....Trung bình - Trung bình ...................

---

#### Bước 2: Mô tả lại if/else bằng lời

> - Khi nào chương trình in `"Giỏi"`?
➡ Khi score >= 8 thì chương trình sẽ in "Giỏi".
> - Khi nào chương trình in `"Yếu"`?
➡ Khi score >= 8 thì chương trình sẽ in "Giỏi".
> - Em hãy mô tả cấu trúc `if/else` bằng lời của em (có thể ví von “ngã rẽ” trong đời sống):

➡ Cấu trúc if/else giống như các ngã rẽ trong cuộc sống. Chương trình sẽ kiểm tra từng điều kiện; nếu điều kiện đúng thì thực hiện hành động tương ứng, nếu không thì chuyển sang điều kiện tiếp theo cho đến khi tìm được trường hợp phù hợp.
---

#### Bước 3: Làm việc với hàm

1. Mở Console, gọi hàm:
```js
tinhDiemTrungBinh(8, 7, 9);
```

> Em ghi lại giá trị hàm trả về: .....8.............................

2. Viết thêm hàm `xepLoai(avg)` trong file JS:
```js
function xepLoai(avg) {
  // TODO: Dùng if/else để:
  // avg >= 8  -> "Giỏi"
  // avg >= 6.5 -> "Khá"
  // avg >= 5  -> "Trung bình"
  // còn lại   -> "Yếu"
}
```

3. Gọi thử trong console:
```js
let avg = tinhDiemTrungBinh(8, 7, 9);
let loai = xepLoai(avg);
console.log("Điểm TB:", avg, " - Xếp loại:", loai);
```

> Câu hỏi:
> - Một hàm gồm những phần chính nào?
➡ tinhDiemTrungBinh, xepLoai
>   - Tên hàm: tinhDiemTrungBinh, xepLoai
>   - Tham số (parameters):  Các giá trị truyền vào hàm, ví dụ: m1, m2, m3 hoặc avg
>   - Thân hàm (body): Phần code bên trong { } để xử lý logic của hàm.
>   - Giá trị trả về (return): Kết quả mà hàm trả về sau khi thực hiện, ví dụ: return avg; hoặc "Giỏi".
> - Ưu điểm của việc dùng hàm thay vì lặp lại cùng một đoạn code nhiều lần là gì?
➡ Giúp tái sử dụng code nhiều lần, giảm lặp lại, dễ đọc và dễ bảo trì chương trình.
---

#### Bước 4: Mở rộng nhỏ (tuỳ chọn)

Viết hàm `kiemTraTuoi(age)`:

```js
function kiemTraTuoi(age) {
  // TODO:
  // Nếu age >= 18 -> console.log("Đủ 18 tuổi");
  // Ngược lại -> console.log("Chưa đủ 18 tuổi");
}
```

Gọi thử: `kiemTraTuoi(16);`, `kiemTraTuoi(20);`.

---

#### Bước 5: Phản tư

> - Phần nào trong if/else hoặc hàm khiến em khó hiểu nhất?
➡ Phần viết điều kiện trong if/else để phân loại kết quả ban đầu hơi khó hiểu.
> - Em đã làm gì để vượt qua (thử nhiều lần, hỏi bạn, xem lại ví dụ, tra Google, …)?
➡ Em thử thay đổi giá trị nhiều lần và chạy lại chương trình, đồng thời xem lại ví dụ và đọc thông báo trong Console để hiểu cách hoạt động của chương trình.

---

## 5. HOẠT ĐỘNG 3 (40’): THAO TÁC DOM \& SỰ KIỆN

### 5.1. Chuẩn bị HTML

Thêm vào trang (hoặc tạo file mới):

```html
<section>
  <h2>DOM & Sự kiện</h2>
  <p id="status">Chưa có tương tác...</p>

  <button id="btnHello">Chào</button>
  <button id="btnRed">Đổi màu nền thành đỏ</button>

  <div style="margin-top: 20px;">
    <label>Nhập tên: </label>
    <input id="nameInput" type="text" />
    <p id="greeting"></p>
  </div>
</section>

<script src="dom.js"></script>
```

Tạo file `dom.js`:

```js
const statusEl = document.getElementById("status");
const btnHello = document.getElementById("btnHello");

btnHello.addEventListener("click", function () {
  statusEl.textContent = "Xin chào! Đây là nội dung được thay đổi bằng JavaScript.";
});
```


---

### 5.2. Nhiệm vụ cho sinh viên

#### Bước 1: Đọc \& giải thích

> Câu hỏi:
> - `document.getElementById("status")` đang làm gì?
➡ Lệnh này dùng để lấy phần tử HTML có id là "status" trong trang web để JavaScript có thể thay đổi nội dung hoặc thuộc tính của phần tử đó
> - Sự kiện `"click"` xảy ra khi nào?
➡ Sự kiện click xảy ra khi người dùng nhấn chuột vào nút hoặc phần tử trên trang web.
> - Trong đoạn code trên, khi nhấn nút `btnHello`, điều gì thay đổi trên trang?
➡ Khi nhấn nút "Chào", nội dung của đoạn <p id="status"> sẽ được thay đổi thành:
Xin chào! Đây là nội dung được thay đổi bằng JavaScript.

---

#### Bước 2: Thử nghiệm nút đổi màu nền

Hoàn thiện code:

```js
const btnRed = document.getElementById("btnRed");

btnRed.addEventListener("click", function () {
  // TODO: Đổi màu nền trang thành đỏ
  document.body.style.backgroundColor = "red";
});
```

> Câu hỏi:
> - Em có thể đổi sang màu khác (vd. `lightblue`) không? Hãy thử.
Em có thể đổi sang màu khác.
Ví dụ: document.body.style.backgroundColor = "lightblue";
Khi nhấn nút, nền trang sẽ đổi sang màu xanh nhạt.

> - Em hãy ghi lại 1 ví dụ khác mà JavaScript có thể làm với `document.body.style`.
Một ví dụ khác mà JavaScript có thể làm với document.body.style:
➡ JavaScript có thể thay đổi kiểu chữ hoặc màu chữ của trang. Ví dụ:

document.body.style.color = "white";
---
Lệnh này sẽ đổi màu chữ trên trang thành màu trắng.

#### Bước 3: Xử lý sự kiện input – gõ tên, hiện lời chào

Hoàn thiện code:

```js
const nameInput = document.getElementById("nameInput");
const greeting = document.getElementById("greeting");

nameInput.addEventListener("input", function () {
  const value = nameInput.value;
  greeting.textContent = "Xin chào, " + value + "!";
});
```



> Câu hỏi:
> - Sự kiện `"input"` khác gì so với `"click"`?
➡ input xảy ra khi người dùng gõ, xoá hoặc thay đổi nội dung trong ô nhập liệu.
➡ click xảy ra khi người dùng nhấn chuột vào một phần tử như nút (button).
> - Khi em xoá hết nội dung ô input, dòng `greeting` hiển thị gì?
➡ Khi xoá hết nội dung, biến value sẽ rỗng nên dòng greeting sẽ hiển thị:

Xin chào, !
---

#### Bước 4: Liên hệ khái niệm DOM

> DOM (Document Object Model) là mô hình biểu diễn trang HTML dưới dạng một **cây các đối tượng** mà JavaScript có thể truy cập và thay đổi.
>
> Em hãy:
> - Tự mô tả DOM bằng lời của em:
>   ➡ DOM là mô hình biểu diễn trang HTML dưới dạng các đối tượng mà JavaScript có thể truy cập và thay đổi. Nhờ DOM, JavaScript có thể chỉnh sửa nội dung, màu sắc hoặc cấu trúc của các phần tử trên trang web.
> - Nêu 1 ví dụ “thao tác DOM” trong bài (ghi lại 1 dòng lệnh cụ thể).
Ví dụ:

document.body.style.backgroundColor = "red";
➡ Lệnh này thay đổi màu nền của trang web thành màu đỏ.
---

#### Bước 5: Ảnh kết quả

Hãy chụp các ảnh màn hình:

1. Khi vừa tải trang (chưa tương tác).
2. Sau khi nhấn “Chào”.
3. Sau khi đổi nền sang màu đỏ.
4. Khi gõ tên và nhìn thấy lời chào xuất hiện.

*(Ảnh có thể được yêu cầu nộp cùng bài hoặc dán vào báo cáo)*

---

## 6. KẾT THÚC (15’): GIỚI THIỆU JQUERY \& PHẢN TƯ

### 6.1. Nhìn nhanh jQuery (so sánh với JS thuần)

Ví dụ:

```js
// JS thuần
document.getElementById("btnHello").addEventListener("click", function () {
  alert("Hello from JS!");
});

// jQuery (giả sử đã import jQuery)
$("#btnHello").on("click", function () {
  alert("Hello from jQuery!");
});
```

> Câu hỏi:
> - Điểm giống nhau về chức năng giữa 2 đoạn code trên là gì?
Cả hai đoạn code đều gắn sự kiện click cho nút btnHello.
Khi người dùng nhấn vào nút, chương trình sẽ hiện thông báo alert trên màn hình.

> - Điểm khác nhau về cú pháp là gì (`document.getElementById` vs `$("#id")`, `addEventListener` vs `.on`)?
| JavaScript thuần                      | jQuery               |
| ------------------------------------- | -------------------- |
| `document.getElementById("btnHello")` | `$("#btnHello")`     |
| `addEventListener("click", ...)`      | `.on("click", ...)`  |
| Cú pháp dài hơn                       | Cú pháp ngắn gọn hơn |
➡️ jQuery viết ngắn và dễ đọc hơn, còn JavaScript thuần dài hơn nhưng không cần thư viện ngoài.

> - Em hãy tra cứu nhanh “What is jQuery used for?” và ghi 2 ý chính:
>   1. Đơn giản hóa việc thao tác DOM (tìm, thay đổi nội dung, CSS, phần tử HTML).

    2. Xử lý sự kiện và hiệu ứng trên trang web dễ dàng hơn (click, animation, AJAX,…).

---

### 6.2. Tự đánh giá \& định hướng

 1. Sau buổi lab, em tò mò nhất về phần nào của JavaScript/DOM?

Em tò mò nhất về cách JavaScript thao tác với DOM để thay đổi nội dung và giao diện trang web khi người dùng tương tác.

2. Em muốn tự làm thêm tính năng gì trên trang web?

Em muốn thử làm tính năng đổi theme (dark/light mode) hoặc một bộ đếm số lần nhấn nút.

3. Em đánh giá mức độ hiểu của mình về:

Biến & kiểu dữ liệu: ☑ Tạm ổn

If/else & hàm: ☑ Tạm ổn

DOM & sự kiện: ☑ Tạm ổn
---

## 7. GHI CHÚ CHO GIẢNG VIÊN (NỘI BỘ)

- Có thể cho SV làm theo cặp/nhóm 2–3 để hỗ trợ nhau thử nghiệm, đọc lỗi, tra cứu.
- Tùy thời lượng thực tế, có thể:
    - Giảm bớt phần mở rộng (hàm `kiemTraTuoi`, tuỳ biến thêm hiệu ứng).
    - Hoặc tăng thêm bài tập DOM (ẩn/hiện một khối, đếm số lần click, v.v.).
- Phiếu học tập tiếp theo có thể chi tiết hóa từng hoạt động thành form trả lời, chỗ dán ảnh, và câu hỏi mini test trắc nghiệm.

```

---```

