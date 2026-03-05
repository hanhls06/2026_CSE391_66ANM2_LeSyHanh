```md
# PHIẾU ÔN TẬP – KIỂM TRA KIẾN THỨC CẦN ĐẠT  
## Chương 5: Những kiến thức nền tảng về JavaScript (5.1 → 5.4)

**Họ và tên:** _Lê Sỹ Hạnh___________________________  
**Mã sinh viên:** __2451271110_______________________  
**Lớp:** ____66ANM2_____________________________  
**Thời gian làm:** ___30_ phút  
**Hình thức:** Cá nhân  
**Yêu cầu:** Trả lời ngắn gọn, đúng ý; với câu code hãy viết đúng cú pháp.

---

## A. Mục tiêu kiến thức cần đạt

Sau khi hoàn thành Chương 5, sinh viên cần:

- Mô tả được JavaScript là gì, chạy ở đâu, vai trò trong web (HTML/CSS/JS). [web:37]  
- Hiểu cú pháp cơ bản, khai báo biến `var/let/const`, kiểu dữ liệu thường gặp, toán tử, ép kiểu cơ bản. [web:57][web:58][web:42]  
- Viết được câu lệnh điều kiện, vòng lặp; định nghĩa và gọi hàm, nắm được tham số/giá trị trả về. [web:47][web:63]  
- Nhận biết khái niệm OOP trong JS: object, property, method; hiểu class ở mức cơ bản và cơ chế prototype ở mức nhận biết. [web:48][web:61]

---

## B. PHẦN 5.1 – GIỚI THIỆU VỀ JAVASCRIPT

### B1. Câu hỏi ngắn
1) JavaScript là gì? (Viết 1–2 câu) [web:37]  
 -JavaScript là ngôn ngữ lập trình dùng để tạo tính tương tác và xử lý logic cho trang web.
 -Nó thường được sử dụng cùng với HTML và CSS để xây dựng website.2) JavaScript có thể chạy ở đâu? Nêu ít nhất 2 môi trường. 
3) Phân biệt vai trò của HTML – CSS – JavaScript trong trang web (mỗi cái 1 ý). [web:37]  
- HTML: Tạo cấu trúc và nội dung của trang web (tiêu đề, đoạn văn, hình ảnh, liên kết…).
- CSS: Dùng để thiết kế giao diện và định dạng trang web (màu sắc, bố cục, font chữ…).
- JavaScript: Tạo tính tương tác và xử lý logic cho trang web (nhấn nút, kiểm tra dữ liệu, thay đổi nội dung động…).

### B2. Đúng/Sai (ghi Đ hoặc S)
4) JavaScript chỉ chạy được trong trình duyệt. _S__ [web:37]  
5) JavaScript dùng để xử lý tương tác và hành vi của trang web. __Đ_ [web:37]

---

## C. PHẦN 5.2 – CÚ PHÁP JAVASCRIPT & CÁC KIỂU DỮ LIỆU

### C1. Khai báo biến: var/let/const
6) Điền vào chỗ trống:  
- `let` có phạm vi (scope) theo __block______ (function/block). [web:57]  
- `var` có phạm vi (scope) theo ____function____ (function/block). [web:57]  
- `const` ___không_____ (có/không) cho phép gán lại (reassign) biến. [web:57]

7) Cho đoạn code, hãy dự đoán và giải thích ngắn:

```js
const arr =;
arr.push(4);
arr =;[^1]
```

- Dòng nào chạy được? Dòng nào lỗi? Vì sao? [web:57]
-Dòng chạy được: arr.push(4);
 Dòng lỗi: arr = [1,2];
-Giải thích:
const không cho phép gán lại biến, nhưng vẫn có thể thay đổi nội dung bên trong object/array. Vì vậy push() vẫn chạy được, còn gán lại arr sẽ gây lỗi.

### C2. Kiểu dữ liệu (Data Types)

8) JavaScript có các kiểu dữ liệu cơ bản (primitive) và kiểu Object. Hãy liệt kê ít nhất 5 kiểu dữ liệu. [web:58][web:42]

Một số kiểu dữ liệu trong JavaScript:

-Number

-String

-Boolean

-Null

-Undefined

-Object

9) Cho các biểu thức sau, hãy ghi kết quả của `typeof`:
```js
typeof 10
typeof "10"
typeof true
typeof null
typeof { a: 1 }
```

- Kết quả: typeof 10 → "number"

           typeof "10" → "string"

           typeof true → "boolean"

           typeof null → "object"

           typeof { a: 1 } → "object"[web:58][web:42]

> Gợi ý: Có một “điểm đặc biệt” với `null`. Em ghi chú lại nếu thấy khác thường. [web:42]

### C3. Toán tử \& ép kiểu cơ bản

10) Dự đoán kết quả:
```js
"5" + 1
"5" - 1
```

- Kết quả: "5" + 1 → "51"

           "5" - 1 → 4     [web:42]

11) Giải thích ngắn sự khác nhau giữa `==` và `===` (1–2 câu).
- == so sánh giá trị và có ép kiểu.

- === so sánh cả giá trị và kiểu dữ liệu, không ép kiểu

---

## D. PHẦN 5.3 – CẤU TRÚC ĐIỀU KHIỂN \& HÀM

### D1. Điều kiện if/else

12) Viết đoạn code: nếu `score >= 5` in `"Pass"`, ngược lại in `"Fail"`. [web:47][web:63]
```js
// TODO:
```
let score = 6;

if (score >= 5) {
    console.log("Pass");
} else {
    console.log("Fail");
}

13) Câu hỏi: Trong chuỗi `if ... else if ... else`, khi một điều kiện đúng thì các nhánh còn lại có được kiểm tra nữa không? Giải thích ngắn. [web:65]
-Trong chuỗi if ... else if ... else, khi một điều kiện đúng thì các nhánh còn lại sẽ không được kiểm tra nữa. Chương trình sẽ thực hiện nhánh đúng đầu tiên rồi bỏ qua các nhánh sau.

### D2. Vòng lặp

14) Viết vòng lặp `for` in ra các số từ 1 đến 5. [web:47]
```js
// TODO:
for (let i = 1; i <= 5; i++) {
    console.log(i);
}
```

15) Viết vòng lặp `while` để cộng dồn tổng từ 1 đến n (n cho trước). [web:47]
```js
let n = 5;
let i = 1;
let sum = 0;

while (i <= n) {
    sum += i;
    i++;
}

console.log(sum);
// Input:
let n = 5;

// TODO:
```


### D3. Hàm (function)

16) Hoàn thiện hàm `sum(a, b)` trả về tổng 2 số: [web:47]
```js
function sum(a, b) {
  return a + b;
}
  // TODO:
}
```

17) Phân biệt:

- **Parameter (tham số)** là gì?
- **Argument (đối số)** là gì?
(Trả lời ngắn + ví dụ 1 dòng)
-Parameter (tham số): biến được khai báo trong định nghĩa hàm.
-Argument (đối số): giá trị thực được truyền vào khi gọi hàm.18)
Ví dụ:
sum(3, 5);

a, b → parameter

3, 5 → argument
 Viết hàm `isEven(n)` trả về `true` nếu n chẵn, `false` nếu n lẻ.
function isEven(n) {
  if (n % 2 === 0) {
    return true;
  } else {
    return false;
  }
}

```js
// TODO:
```


---

## E. PHẦN 5.4 – LẬP TRÌNH HƯỚNG ĐỐI TƯỢNG (OOP) VỚI JAVASCRIPT

### E1. Object cơ bản

19) Tạo một object `student` có các property: `name`, `id`, `gpa` và method `introduce()` in ra câu giới thiệu. [web:61]
```js
let student = {
  name: "An",
  id: "SV01",
  gpa: 3.5,
  introduce: function() {
    console.log("Hello, my name is " + this.name);
  }
};
// TODO:
```

20) Cho object:
```js
const student = {
  name: "An",
  gpa: 3.2
};
```

- Truy cập `name` theo 2 cách khác nhau (dot notation và bracket notation). [web:61]

```js
// Cách 1: student.name
  
// Cách 2: student["name"]
```


### E2. Class (mức cơ bản)

21) Hoàn thiện class `Person` có:

- constructor nhận `name`, `age`
- method `greet()` in `"Hello, I'm <name>"` [web:61]

```js
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }

  greet() {
    console.log("Hello, I'm " + this.name);
  }
}

const p1 = new Person("Linh", 20);
p1.greet();  // TODO:
}

const p1 = new Person("Linh", 20);
p1.greet();
```

22) (Câu hỏi) `constructor` trong class dùng để làm gì? (1 câu) [web:61]
- constructor là hàm đặc biệt trong class dùng để khởi tạo giá trị ban đầu cho object khi object được tạo ra.### E3. Prototype (mức nhận biết)

23) Prototype trong JavaScript liên quan đến cơ chế “kế thừa/tra cứu thuộc tính” giữa các object. Em hãy mô tả --prototype bằng lời của em (2–3 câu). [web:48]
-Prototype là cơ chế giúp các object trong JavaScript kế thừa và dùng lại thuộc tính hoặc phương thức từ object khác.
-Khi một object không có thuộc tính nào đó, JavaScript sẽ tra cứu thuộc tính đó trong prototype của nó.
24) Quan sát đoạn ví dụ (không cần thuộc lòng):
```js
const personPrototype = {
  greet() { console.log("hello!"); }
};

const carl = Object.create(personPrototype);
carl.greet();
```

- `Object.create(personPrototype)` làm gì? (1 câu) [web:48]
Object.create(personPrototype) tạo một object mới và đặt personPrototype làm prototype của object đó.
---

## F. TỰ ĐÁNH GIÁ (Self-Reflection)

1) Em tự chấm mức hiểu của mình (khoanh tròn):

- 5.1 Giới thiệu JS: Khá rõ

-5.2 Cú pháp & kiểu DL: Khá rõ

-5.3 Điều khiển & hàm: Khá rõ

-5.4 OOP JS: Tạm ổn
2) Ba điều em còn chưa chắc hoặc muốn hỏi thêm:
1. Sự khác nhau giữa var, let, const trong các trường hợp thực tế.

2.Cách prototype hoạt động trong JavaScript khi kế thừa giữa các object.

3.Khi nào nên dùng class và khi nào nên dùng object thường trong JavaScript.
---


