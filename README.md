<div align="center">
  <img width="50" src="https://i.postimg.cc/h4dzTwG8/javascript.png">

### **JavaScript Interview Questions and Answers**

</div>
<br>

1. #### **What is the difference between == and === operators?**

   "==" operatoruna bərabərlik operatoru deyilir. Dəyişənlərin data tiplərini nəzərə almadan iki dəyişəni müqayisə etmək üçün istifadə edilir və boolean dəyər (true və ya false) qaytarır. Əgər dəyişənlərin dəyəri eynidirsə true qaytarır, deyilsə false qaytarır. <br>
   "===" operatoruna isə qatı bərabərlik operatoru deyilir və "==" operatorundan fərqli olaraq iki dəyişənin həm dəyərini müqayisə edir, həm də data tiplərini yoxlayır. Əgər hər ikisi də eynidirsə true qaytarır, deyilsə false qaytarır. <br>

   _Bir neçə nümunəyə baxaq:_

   ```js
   "you" == "you"; // true
   "you" === "you"; // true
   "your" === "you"; // false
   5 == "5"; // true
   5 === "5"; // false
   5 == 5; // true
   5 === 5; // true
   0 == false; // true
   0 === false; // false
   1 == true; // true
   1 === true; // false
   null == null; // true
   null === null; // true
   null == undefined; // true
   null === undefined; // false
   NaN === NaN; // false
   ```

<br>

2. #### **What is null value?**

   Null dəyərin yoxluğunu ifadə edən JavaScriptə xas primitiv data növüdür və typeof operatorundan istifadə edəndə object qaytarır. <br>

   _Nümunə:_

   ```js
   let test = null;
   alert(test); // null
   alert(typeof test); // object
   ```

<br>

3. #### **What is undefined property?**

   Undefined dəyişənin olduğunu, lakin dəyər təyin edilmədiyini bildirən primitiv data növüdür və typeof operatorundan istifadə edəndə undefined qaytarır. <br>

   _Nümunə:_

   ```js
   let test;
   alert(test); // undefined
   alert(typeof test); // undefined
   ```

<br>

4. #### **What is isNaN?**

   JavaScriptdə isNaN() metodu dəyərin ədəd olub-olmamasını yoxlayır və boolean dəyər (true və ya false) qaytarır. Əgər dəyər NaN (**N**ot-**a**-**N**umber) olarsa (yəni ədəd olmazsa), bu zaman true qaytarır, əks halda false qaytarır. <br>

   _Nümunə:_

   ```js
   isNaN(20); // false
   isNaN("20"); // false
   isNaN("20.55"); // false
   isNaN("20,55"); // true
   isNaN("text"); // true
   isNaN(""); // false
   isNaN(" "); // false
   isNaN(null); // false
   isNaN(undefined); // true
   isNaN(NaN); // true
   isNaN(true); // false
   isNaN({}); // true
   isNaN(new Date()); // false
   ```

<br>

5. #### **What is the typeof operator?**

   JavaScriptdə typeof operatorundan dəyişənlərin data tipini tapmaq üçün istifadə olunur. <br>

   _Nümunə:_

   ```js
   // numbers
   typeof 55; // 'number'
   typeof 55.12; // 'number'
   typeof Infinity; // 'number'
   typeof NaN; // 'number'
   typeof Number("5"); // 'number'
   typeof Number("paper"); // 'number'

   typeof 55n; // 'bigint'

   // strings
   typeof ""; // 'string'
   typeof "3"; // 'string'
   typeof "text"; // 'string'
   typeof `string text`; // 'string'
   typeof typeof 5; // 'string'

   // booleans
   typeof true; // 'boolean'
   typeof false; // 'boolean'

   // undefined
   typeof undefined; // 'undefined'

   // objects
   typeof null; // 'object'
   typeof { name: "Samir" }; // 'object'
   typeof [5, 55, 12]; // 'object'
   typeof new Date(); // 'object'

   // function
   typeof function () {}; // 'function'
   ```

<br>

6. ### **Who created JavaScript?**
   JavaScript ilk dəfə **1995**-ci ildə **Brendan Eich** tərəfindən **Netscape Navigator 2.0** ilə birlikdə buraxılmışdır. İlk olaraq **Mocha** adı verildi, daha sonra **LiveScript** və ən sonda isə **JavaScript** adını aldı.

<br>

7. ### **What are primitive data types?**

   JavaScriptdə primitiv data növləri metodları və xüsusiyyətləri (properties) olmayan datadır. 7 primitiv data növü var. <br>

- number
- bigint
- undefined
- null
- string
- symbol
- boolean

<br>

8. ### **What is NaN property?**

   NaN "**N**ot-**a**-**N**umber" (ədəd olmayan) dəyərləri təmsil edən qlobal xüsusiyyətdir. NaN xüsusiyyətindən daxil edilmiş nömrələrin etibarlı olub-olmamasını yoxlamaq üçün istifadə edilə bilər. <br>

   _Nümunə:_

   ```js
   parseInt("text"); // NaN
   Number(undefined); // NaN
   Math.sqrt(-1); // NaN
   5 + NaN; // NaN
   0 * Infinity; // NaN
   undefined + undefined; // NaN
   "text" / 5; // NaN
   "text" * 5; // NaN
   "text" - 5; // NaN
   ```

   <br>

9. ### **What are the bitwise operators available in JavaScript?**

   Bitwise operatorları aşağıdakılardır:

   | Operator |             Name             |  Example   |
   | :------: | :--------------------------: | :--------: |
   |    &     |         Bitwise AND          |   a & b    |
   |  &#124;  |          Bitwise OR          | a &#124; b |
   |    ^     |         Bitwise XOR          |   a ^ b    |
   |    ~     |         Bitwise NOT          |    ~ a     |
   |    <<    |          Left shift          |   a << b   |
   |    >>    | Sign-propagating right shift |   a >> b   |
   |   >>>    |    Zero-fill right shift     |  a >>> b   |

<br>

10. ### **What is the use of setTimeout?**

    JavaScriptdə setTimeout() metodundan funksiyanı çağırmaq və müəyyən edilmiş vaxtdan sonra yalnız bir dəfə yerinə yetirmək üçün istifadə olunur. Əgər icranı təkrarlamaq lazımdırsa, bu zaman setInterval() metodundan istifadə etmək lazımdır.

    _Nümunə:_

    ```js
    function sayHello() {
      alert("Hello!");
    }

    setTimeout(sayHello, 5000);
    ```

    Bu o deməkdir ki, sayHello() metodu 5 saniyədən (5000 millisaniyə) sonra işə düşəcək, yəni bir dəfə 5 saniyədən sonra ekranda "Hello!" yazısı görünəcək.

<br>

11. ### **What is the use of setInterval?**

    JavaScriptdə setInterval() metodundan funksiyanı çağırmaq və müəyyən edilmiş vaxt ərzində davamlı şəkildə yerinə yetirmək üçün istifadə olunur. SetInterval() metodu setTimeout() metodu ilə eyni yazılışa sahibdir, lakin ondan tək fərqi müəyyən edilmiş vaxt ərzində yalnız bir dəfə yox, davamlı şəkildə işləyir. Bu metod clearInterval() metodu çağırılana qədər və ya pəncərə (windows) bağlanana qədər davam edir.

    _Nümunə:_

    ```js
    function sayHello() {
      alert("Hello!");
    }

    setInterval(sayHello, 5000);
    ```

    Bu o deməkdir ki, sayHello() metodu hər 5 saniyədən (5000 millisaniyə) bir işə düşəcək, yəni hər 5 saniyədən bir ekranda "Hello!" yazısı görünəcək.
