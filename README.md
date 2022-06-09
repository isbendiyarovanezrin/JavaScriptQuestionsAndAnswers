<div align="center">
  <img width="50" src="https://i.postimg.cc/h4dzTwG8/javascript.png">

### JavaScript Interview Questions and Answers

#### “The strength of JavaScript is that you can do anything. The weakness is that you will.”

<p align="end"><em>━ Reg Braithwaite</em></p>
</div>

#

1. ### What is the difference between == and === operators?

   "==" operatoruna bərabərlik operatoru deyilir. Dəyişənlərin data tiplərini nəzərə almadan iki dəyişəni müqayisə etmək üçün istifadə edilir və boolean dəyər (true və ya false) qaytarır. Əgər dəyişənlərin dəyəri eynidirsə true qaytarır, deyilsə false qaytarır. <br />
   "===" operatoruna isə qatı bərabərlik operatoru deyilir və "==" operatorundan fərqli olaraq iki dəyişənin həm dəyərini müqayisə edir, həm də data tiplərini yoxlayır. Əgər hər ikisi də eynidirsə true qaytarır, deyilsə false qaytarır.

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

<br />

2. ### What is null value?

   Null dəyərin yoxluğunu ifadə edən JavaScriptə xas primitiv data növüdür və typeof operatorundan istifadə edəndə object qaytarır.

   _Nümunə:_

   ```js
   let test = null;
   alert(test); // null
   alert(typeof test); // object
   ```

<br />

3. ### What is undefined property?

   Undefined dəyişənin olduğunu, lakin dəyər təyin edilmədiyini bildirən primitiv data növüdür və typeof operatorundan istifadə edəndə undefined qaytarır.

   _Nümunə:_

   ```js
   let test;
   alert(test); // undefined
   alert(typeof test); // undefined
   ```

<br />

4. ### What is isNaN?

   JavaScriptdə isNaN() metodu dəyərin ədəd olub-olmamasını yoxlayır və boolean dəyər (true və ya false) qaytarır. Əgər dəyər NaN (**N**ot-**a**-**N**umber) olarsa (yəni ədəd olmazsa), bu zaman true qaytarır, əks halda false qaytarır.

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

<br />

5. ### **What is the typeof operator?**

   JavaScriptdə typeof operatorundan dəyişənlərin data tipini tapmaq üçün istifadə olunur.

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
   typeof "5"; // 'string'
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

<br />

6. ### Who created JavaScript?

   JavaScript ilk dəfə **1995**-ci ildə **Brendan Eich** tərəfindən **Netscape Navigator 2.0** ilə birlikdə buraxılmışdır. İlk olaraq **Mocha** adı verildi, daha sonra **LiveScript** və ən sonda isə **JavaScript** adını aldı.

<br />

7. ### What are primitive data types?

   JavaScriptdə primitiv data növləri metodları və xüsusiyyətləri (properties) olmayan datadır. 7 primitiv data növü var.

- number
- bigint
- undefined
- null
- string
- symbol
- boolean

<br />

8. ### What is NaN property?

   NaN "**N**ot-**a**-**N**umber" (ədəd olmayan) dəyərləri təmsil edən qlobal xüsusiyyətdir. NaN xüsusiyyətindən daxil edilmiş nömrələrin etibarlı olub-olmamasını yoxlamaq üçün istifadə edilə bilər.

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

   <br />

9. ### What are the bitwise operators available in JavaScript?

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

<br />

10. ### What is the use of setTimeout?

    JavaScriptdə setTimeout() metodundan funksiyanı çağırmaq və müəyyən edilmiş vaxtdan sonra yalnız bir dəfə yerinə yetirmək üçün istifadə olunur. Əgər icranı təkrarlamaq lazımdırsa, bu zaman setInterval() metodundan istifadə etmək lazımdır.

    _Nümunə:_

    ```js
    function sayHello() {
      alert("Hello!");
    }

    setTimeout(sayHello, 5000);
    ```

    Bu o deməkdir ki, sayHello() metodu 5 saniyədən (5000 millisaniyə) sonra işə düşəcək, yəni bir dəfə 5 saniyədən sonra ekranda "Hello!" yazısı görünəcək.

<br />

11. ### What is the use of setInterval?

    JavaScriptdə setInterval() metodundan funksiyanı çağırmaq və müəyyən edilmiş vaxt ərzində davamlı şəkildə yerinə yetirmək üçün istifadə olunur. SetInterval() metodu setTimeout() metodu ilə eyni yazılışa sahibdir, lakin ondan tək fərqi müəyyən edilmiş vaxt ərzində yalnız bir dəfə yox, davamlı şəkildə işləyir. Bu metod clearInterval() metodu çağırılana qədər və ya pəncərə (windows) bağlanana qədər davam edir.

    _Nümunə:_

    ```js
    function sayHello() {
      alert("Hello!");
    }

    setInterval(sayHello, 5000);
    ```

    Bu o deməkdir ki, sayHello() metodu hər 5 saniyədən (5000 millisaniyə) bir işə düşəcək, yəni hər 5 saniyədən bir ekranda "Hello!" yazısı görünəcək.

<br />

12. ### What would be the result of 1+2+'3'?
    Cavab 33-dür, çünki ilk iki dəyər ədəddir və ona görə də birinci 1 və 2 toplanacaq (3+'3'). Ondan sonrakı dəyər isə string'dir və string olduğu üçün də dəyərlər birləşəcək və cavab 33 olacaq.

<br />

13. ### What is the difference between internal and external JavaScript?

    Internal (daxili) JavaScript HTML-də `<script></script>` teqinin içində yazılır. External (xarici) JavaScriptdə isə JavaScript kodları ayrıca ".js" uzantılı faylın içində yazılır və HTML-də bu kod ilə çağırılır `<script src="filename.js"></script>`.

<br />

14. ### What paradigm is JavaScript?

    JavaScript **funksional (functional)**, **obyekt yönümlü (object-oriented)**, **prosessual/imperativ (procedural/imperative)** və **prototip (prototypal)** proqramlaşdırmanı dəstəkləyən **çoxparadiqmalı (multi-paradigm)** dildir.

<br />

15. ### What is JSON?

    JSON (**J**ava**S**cript **O**bject **N**otation) dataları (çox böyük olmayan) depolamaq və dəyişdirmək üçün istifadə olunan JavaScript obyekt məntiqinə əsaslanan mətn əsaslı formatdır. Məsələn, JSON-dan istifadə edərək serverdən alınan JSON-ları JavaScript obyektinə çevirə bilərsiniz və ya hər hansısa bir JavaScript obyektini JSON-a çevirib serverə göndərə bilərsiniz. Fayl genişləməsi **".json"**-dur. JSON-da verilənlər açar (key) və dəyərlərdən (value) ibarət olur.

    _Nümunə:_

    ```json
    { "ad": "Vüsalə", "soyad": "İsbəndiyarova" }
    ```

<br />

16. ### What are the syntax rules of JSON?
    JSON-un aşağıdakı sintaksis qaydaları var:

- Verilənlər açar (key) və dəyər (value) cütlərindən ibarət olur. Sol tərəfdəki məlumatlar açarı, sağ tərəfdəki məlumatlar isə dəyəri təmsil edir (hər ikisi qoşa dırnaq içində yazılır) və bir-birlərindən ":" (iki nöqtə) işarəsi ilə ayrılırlar.
- Ad/dəyər (name/value) cütləri bir-birindən vergüllə ayrılır.
- Bəzəkli mötərizələr ({}) obyektləri saxlayır.
- Kvadrat mötərizələr ([]) arrayları saxlayır.

<br />

17. ### Why do you need JSON?
    Serverlə brauzer arasında olan məlumat mübadiləsi yalnız mətn ola bilər. JSON da yalnız mətn olduğundan serverə və ya serverdən asanlıqla göndərilə bilər və bütün proqramlaşdırma dilləri tərəfindən data formatı kimi istifadə oluna bilər.

<br />

18. ### How do you parse JSON string?

    JSON-un ümumi istifadəsi serverə və ya serverdən data mübadiləsi etməkdir və serverdən məlumat qəbul edərkən data həmişə string formatında olmalıdır. **JSON.parse()** metodu ilə aşağıdakı string dəyərini JavaScript obyektinə çevirə bilərsiniz.

    _Nümunə:_

    ```js
    const str = '{"name":"Orkhan", "surname":"Shahbaz", "age":29}';
    const obj = JSON.parse(str);
    console.log(obj); // { name: 'Orkhan', surname: 'Shahbaz', age: 29 }
    ```

    Burada obyekt əvəzinə massivə çevirəcək.

    ```js
    const text = '["alma", "armud", "banan", "nar"]';
    const arr = JSON.parse(text);
    console.log(arr); // [ 'alma', 'armud', 'banan', 'nar' ]
    ```

<br />

19. ### What is the purpose JSON stringify?

    JSON-un ümumi istifadəsi serverə və ya serverdən data mübadiləsi etməkdir və serverə məlumat göndərərkən data həmişə string formatda olmalıdır. **JSON.stringify()** metodu ilə JavaScript obyektini string formatına çevirə bilərsiniz.

    _Nümunə:_

    ```js
    const obj = {
      name: "Orkhan",
      surname: "Shahbaz",
      age: 29,
    };

    const myJSON = JSON.stringify(obj);
    console.log(myJSON); // {"name":"Orkhan","surname":"Shahbaz","age":29}
    ```

    `myJSON` indi stringdir və serverə göndərilməyə hazırdır.

<br />

20. ### How do you redirect new page in JavaScript?

    JavaScript ilə başqa səhifəyə redirect etməyin bir neçə yolu var. Bunlardan ən məşhur olanları window obyektinin `location.href` xüsusiyyəti və `location.replace` metodudur.

    _Nümunə:_

    Buttona klik edəndə portfolio saytıma gedəcək.

    _Birinci yol:_

    ```html
    <button type="button" onclick="myFunction()">Go website</button>
    ```

    ```js
    function myFunction() {
      window.location.href = "https://isbendiyarovanezrin.herokuapp.com";
    }
    ```

    _İkinci yol:_

    ```html
    <button type="button" onclick="myFunction()">Go website</button>
    ```

    ```js
    function myFunction() {
      location.replace("https://isbendiyarovanezrin.herokuapp.com");
    }
    ```

<br />

21. ### How do you get the current url with JavaScript?

    JavaScriptdə cari URL adresini almaq üçün `window.location.href` xüsusiyyətindən istifadə olunur.

    _Nümunə:_

    ```js
    console.log(window.location.href); // cari URL adresini qaytarır
    ```

<br />

22. ### How do you check if a string starts with another string?

    Bunu JavaScript string `startsWith()` metodu ilə etmək olar. `StartsWith()` metodu stringin təyin edilmiş string ilə başlayıb-başlamadığını müəyyən edir və boolean (true və ya false) dəyər qaytarır. Əgər string təyin edilmiş string ilə başlayırsa true qaytarır, əks halda false qaytarır.

    _Sintaksisi bu şəkildədir:_

    ```
    string.startsWith(axtarılan string)
    string.startsWith(axtarılan string, mövqe)
    ```

    _Nümunə:_

    ```js
    const text = "Mənim anam mükəmməldir!";
    const result = text.startsWith("Mənim"); // və ya ("Mənim", 0)
    console.log(result); // true qaytaracaq
    ```

    ```js
    let text = "Mənim anam mükəmməldir!";
    let result = text.startsWith("ən", 1);
    console.log(result); // true qaytaracaq
    ```

    Bu metod böyük, kiçik hərflərə qarşı həssasdır. Başdakı "m" hərfini kiçik yazdığım üçün false qaytaracaq.

    ```js
    let text = "Mənim anam mükəmməldir!";
    let result = text.startsWith("mənim");
    console.log(result); // false qaytaracaq
    ```

<br />

23. ### What is a polyfill?

    Polyfill yazdığımız kodları dəstəkləməyən köhnə brauzerlərdə müasir funksionallığı təmin üçün istifadə edilən kod parçasıdır.

<br />

24. ### How do you define JSON arrays?

    JSON massivləri kvadrat mötərizələrin ([]) içində yazılır və JavaScript obyektlərini saxlayır. JSON-dakı massivlər JavaScriptdəki massivlər ilə demək olar ki, eynidir. JSON-da massiv dəyərləri obyekt, string, number, null, massiv və ya boolean ola bilər. JSON stringini (içində JSON massivi olan) `JSON.parse()` metodu ilə massivə çevirə bilərik.

    _Nümunə:_

    ```js
    const meyve =
      '{"meyveler":[{"ad":"alma", "növ":"sibir"}, {"ad":"armud", "növ":"lada"}]}';
    const result = JSON.parse(meyve);
    console.log(result);
    ```

    _Nəticəsi:_

    ```
    {
     meyveler: [ { ad: 'alma', 'növ': 'sibir' }, { ad: 'armud', 'növ': 'lada' } ]
    }
    ```

    Massiv indeksi 0-dan başlayır.

    ```js
    const meyve =
      '{"meyveler":[{"ad":"alma", "növ":"sibir"}, {"ad":"armud", "növ":"lada"}]}';
    const result = JSON.parse(meyve);
    console.log(result.meyveler[0]);
    ```

    _Nəticəsi:_

    ```
    { ad: 'alma', 'növ': 'sibir' }
    ```

    _Başqa bir nümunəyə baxaq:_

    ```js
    const meyve =
      '{"meyveler":[{"ad":"alma", "növ":"sibir"}, {"ad":"armud", "növ":"lada"}]}';
    const result = JSON.parse(meyve);
    console.log(result.meyveler[1].ad);
    ```

    _Nəticəsi:_

    ```
    armud
    ```

<br />

25. ### How do you generate random integers?

    `Math.random()` metodu 0 (daxil olmaqla) ilə 1 (daxil deyil) arasında təsadüfi şəkildə (random) ədədlər qaytarır. `Math.random()` metodu həmişə 1-dən aşağı ədəd qaytarır.

    _Nümunə:_

    ```js
    // 0 ilə 1 (daxil deyil) arasında random bir ədəd qaytaracaq
    console.log(Math.random());
    ```

    `Math.floor()` ilə istifadə olunan `Math.random()` metodu random **tam ədədləri** qaytarmaq üçün istifadə olunur, çünki `Math.floor()` metodu ədədi aşağı ən yaxın tam ədədə yuvarlaqlaşdırır.

    ```js
    // 0 ilə 9 (daxil olmaqla) arasında random tam ədəd qaytaracaq
    console.log(Math.floor(Math.random() * 10));
    ```

    ```js
    // 1 ilə 10 (daxil olmaqla) arasında random tam ədəd qaytaracaq
    console.log(Math.floor(Math.random() * 10) + 1);
    ```

    #### ⬆ [Yuxarıya qayıt](https://github.com/isbendiyarovanezrin/JavaScriptQuestionsAndAnswers#readme)

26. ### Can I use reserved words as identifiers?

    Xeyr, istifadə edilsə error verəcək. Dəyişən, funksiya adı kimi bu sözlərdən istifadə edilə bilməz. Məsələn: if, else, for, return, delete, default, this, switch, null, new, true, false, continue, do, const, with, try, break.

    _Nümunə:_

    ```js
    let default = "text";
    console.log(default);
    ```

    _Nəticəsi:_

    ```js
    SyntaxError: Unexpected token 'default'
    ```

<br />

27. ### How do you detect JavaScript disabled in the page?

    JavaScriptin deaktiv olub-olmadığını aşkar etmək üçün `<noscript>` teqindən istifadə olunur. Bu teq skriptləri dəstəkləməyən və ya skriptləri söndürülmüş brauzerləri olan istifadəçilərə göstəriləcək alternativ məzmunu müəyyən edir. Aşağıdakı `<noscript>` teqinin içindəki kod bloku JavaScript söndürüləndə icra olunacaq.

    _Nümunə:_

    ```html
    <script>
      // Burada JavaScript kodları yazılacaq
    </script>

    <noscript>Sizin brauzeriniz JavaScripti dəstəkləmir!</noscript>
    ```

<br />

28. ### How can you get the list of keys of any object?

    Bunun üçün `Object.keys()` və `Object.getOwnPropertyNames()` metodlarından istifadə edə bilərik. `Object.keys()` və `Object.getOwnPropertyNames()` metodları obyektin xüsusiyyət adlarından (property name) ibarət massiv qaytarır, amma ikisinin arasında kiçik fərqlər var. Onlardan biri `Object.getOwnPropertyNames()` metodu obyektin bütün xüsusiyyət adlarını qaytarır, `Object.keys()`metodu isə yalnız sadalanan (enumerable) xüsusiyyət adlarını qaytarır.

    _Nümunə:_

    `Object.keys()` metodunu yoxlayaq.

    ```js
    let user = { name: "Orkhan", surname: "Shahbaz", age: 29 };
    console.log(Object.keys(user));
    ```

    _Nəticəsi:_

    ```
    [ 'name', 'surname', 'age' ]
    ```

    `Object.getOwnPropertyNames()` metodunu yoxlayaq.

    ```js
    let user = { name: "Orkhan", surname: "Shahbaz", age: 29 };
    console.log(Object.getOwnPropertyNames(user));
    ```

    _Nəticəsi:_

    ```
    [ 'name', 'surname', 'age' ]
    ```

<br />

29. ### How do you print the contents of web page?

    Window obyektinin `print()` metodu cari pəncərənin məzmununu çap etmək üçün istifadə olunur. `Print()` metodu müxtəlif çap seçimlərini seçməyə imkan verən çap dialoq qutusunu (Print Dialog Box) açır.

    _Nümunə:_

    Bu zaman buttona klik edəndə aşağıdakı çap dialoq qutusu açılacaq.

    ```html
    <button type="button" onclick="window.print()">Səhifəni çap et</button>
    ```

    <img width="85%" src="https://i.postimg.cc/9QTT4N8Q/print.png">

<br />

30. ### How do you combine two or more arrays?

    İki və ya daha çox massivi birləşdirmək üçün `concat()` metodundan istifadə edə bilərik. `Concat()` metodu mövcud massivləri dəyişdirmir, birləşdirilmiş massivlərdən ibarət yeni massiv qaytarır.

    _Sintaksisi bu şəkildədir:_

    ```
    massiv1.concat(massiv2, massiv3, ..., massivN)
    ```

    _Nümunə:_

    ```js
    const massiv1 = ["n", "e", "z"];
    const massiv2 = ["r", "i", "n"];
    const ad = massiv1.concat(massiv2);
    console.log(ad);
    ```

    _Nəticəsi:_

    ```
    [ 'n', 'e', 'z', 'r', 'i', 'n' ]
    ```

    3 massivi də birləşdirmək olar.

    ```js
    const eded1 = [1, 2, 3];
    const eded2 = [4, 5, 6];
    const eded3 = [7, 8, 9];
    const ededler = eded1.concat(eded2, eded3);
    console.log(ededler);
    ```

    _Nəticəsi:_

    ```
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
    ```

<br />

31. ### How do you create specific number of copies of a string?

    Bunun üçün JavaScript string `repeat()` metodundan istifadə etmək lazımdır. `Repeat()` metodu stringin bizim müəyyən etdiyimiz qədər kopyasından ibarət yeni string qaytarır. Bu metod ECMAScript 2015 spesifikasiyasına əlavə edilmişdir və hələ də bütün JavaScript tətbiqlərində (implementations) mövcud olmaya bilər.

    _Sintaksisi bu şəkildədir:_

    ```
    string.repeat(eded)
    ```

    Burada "eded" mənfi olmamalıdır.

    _Nümunə:_

    ```js
    const text = "Nəzrin ";
    let copy1 = text.repeat(-1);
    let copy2 = text.repeat(0);
    let copy3 = text.repeat(1);
    let copy4 = text.repeat(5);
    let copy5 = text.repeat(2.5);
    console.log(copy1); // RangeError: Invalid count value
    console.log(copy2); // '' (boş)
    console.log(copy3); // Nəzrin
    console.log(copy4); // Nəzrin Nəzrin Nəzrin Nəzrin Nəzrin
    console.log(copy5); // Nəzrin Nəzrin (ədəd tam ədədə çevriləcək)
    ```

<br />

32. ### What is the output of below console statement with unary operator?

    ```js
    console.log(+"Hello");
    ```

    "+" **unary plus** operatorudur və operandı number növünə çevirməyə çalışır (əgər ədəd deyilsə). Nəticə **NaN** olacaq, çünki JavaScript tərcüməçisi (interpreter) operandı number növünə çevirməyə çalışacaq və çevirmə uğursuz olacaq. Ona görə də **NaN** qaytaracaq.

<br />

33. ### What happens if we add two arrays?

    Əgər biz iki massivi toplamağa çalışsaq massivlər birinci stringə çevriləcək, sonra isə birləşəcək.

    _Nümunə:_

    ```js
    console.log([] + []); // ''
    console.log([2, 5] + [5, 25]); // 2,55,25
    console.log([2, 5] + ["-ci", 25]); // 2,5-ci,25
    console.log(["Sa"] + ["mir"]); // Samir
    console.log(["Sa"] + ["mir", "Aydan"]); // Samir,Aydan
    ```

<br />

34. ### How do you empty an array?

    Massivi boşaltmağın ən tez yollarından biri massivin uzunluğunu 0-a bərabər etməkdir.

    _Nümunə:_

    ```js
    let meyveler = ["alma", "armud", "banan"];
    meyveler.length = 0;
    console.log(meyveler); // []
    ```

<br />

35. ### How do you rounding numbers to certain decimals?

    Bunu JavaScript number `toFixed()` metodu ilə edə bilərik. `toFixed()` metodu ədədi stringə çevirir və müəyyən edilmiş ədədə qədər yuvarlaqlaşdırır.

    _Nümunə:_

    ```js
    const eded = 5.22255225;
    console.log(eded.toFixed()); // 5
    console.log(eded.toFixed(0)); // 5
    console.log(eded.toFixed(2)); // 5.22
    console.log(eded.toFixed(5)); // 5.22255
    console.log(typeof eded.toFixed(5)); // string
    ```

<br />

36. ### What is the easiest way to convert an array to an object?

    Ən asan yolu spread (...) operatorundan istifadə etməkdir. Spread (...) operatorundan istifadə edərək massivi eyni data ilə obyektə çevirə bilərsiniz.

    _Nümunə:_

    ```js
    let meyve = ["alma", "armud", "banan"];
    meyveObyekt = { ...meyve };
    console.log(meyveObyekt); // { '0': 'alma', '1': 'armud', '2': 'banan' }
    ```

<br />

37. ### How do you create an array with some data?

    JavaScript massiv `fill()` metodundan istifadə edərək eyni məlumatlara malik massiv yarada bilərik. Başlanğıc və son mövqe müəyyən edilə bilər, əks halda bütün elementlər doldurulacaq.

    _Sintaksisi bu şəkildədir:_

    ```
    massiv.fill(dəyər)
    massiv.fill(dəyər, başlanğıc (defaultu 0-dır))
    massiv.fill(dəyər, başlanğıc, son (defaultu massivin uzunluğudur))
    ```

    _Nümunə:_

    ```js
    let meyve = ["alma", "armud", "banan"];
    console.log(meyve.fill("gilas")); // [ 'gilas', 'gilas', 'gilas' ]
    ```

<br />

38. ### How do you disable right click in the web page?

    Veb səhifədə sağ klik hadisəsini body elementində `oncontextmenu` atributundan false qaytarmaqla deaktiv edə bilərik.

    _Nümunə:_

    ```html
    <body oncontextmenu="return false;"></body>
    ```

<br />

39. ### How do you find operating system details?

    `window.navigator` obyekti ziyarətçinin brauzeri, əməliyyat sisteminin detalları və s. haqqında məlumatları ehtiva edir.

    _Nümunə:_

    ```js
    console.log(navigator);
    ```

<br />

40. ### How do you display data in a tabular format using console object?

    `console.table()` metodu massivləri və obyektləri konsolda cədvəl formatında göstərmək üçün istifadə olunur. Mürəkkəb massivləri və ya obyektləri vizuallaşdırmaq lazım olanda çox faydalıdır.

    _Nümunə:_

    ```js
    const meyve = [
      { ad: "alma", növ: "sibir" },
      { ad: "armud", növ: "lada" },
      { ad: "gilas", növ: "regina" },
    ];
    console.table(meyve);
    ```

    _Nəticəsi:_

    ![table](https://i.postimg.cc/3J4Hhq7L/table.png)

<br />

41. ### What is the purpose of the array slice method?

    `slice()` metodu massivdə seçilmiş elementləri yeni massiv kimi qaytarır. `slice()` metodu verilmiş başlanğıcdan verilmiş sona qədər (sonuncu ədəd daxil deyil) seçir. Əgər bitiş ədədini yazmasaq verilmiş başlanğıcdan sona qədər seçəcək. Bu metod orijinal massivi dəyişmir.

    _Sintaksisi bu şəkildədir:_

    ```
    massiv.slice()
    massiv.slice(başlanğıc)
    massiv.slice(başlanğıc, son)
    ```

    _Nümunə:_

    ```js
    const meyve = ["alma", "armud", "banan", "nar"];
    console.log(meyve.slice()); // [ 'alma', 'armud', 'banan', 'nar' ]
    console.log(meyve.slice(1)); // [ 'armud', 'banan', 'nar' ]
    console.log(meyve.slice(1, 2)); // [ 'armud' ]
    console.log(meyve.slice(1, 3)); // [ 'armud', 'banan' ]
    console.log(meyve.slice(1, 4)); // [ 'armud', 'banan', 'nar' ]
    console.log(meyve.slice(-1)); // [ 'nar' ]
    console.log(meyve.slice(-2)); // [ 'banan', 'nar' ]
    console.log(meyve.slice(1, -1)); // [ 'armud', 'banan' ]
    ```

<br />

42. ### What is the purpose of the array splice method?

    `splice()` metodu mövcud elementləri əvəz etməklə, silməklə və yaxud yerinə yeni elementlər əlavə etməklə massivin məzmununu dəyişdirir və silinmiş massivi qaytarır. Birinci arqument əlavə etmək və ya silmək üçün massiv mövqeyini, istəyə bağlı ikinci arqument isə silinəcək element sayını göstərir.

    _Sintaksisi bu şəkildədir:_

    ```
    massiv.slice(başlanğıc)
    massiv.slice(başlanğıc, silinənElementSayı, element1)
    massiv.slice(başlanğıc, silinənElementSayı, element1, element2, elementN)
    ```

    _Nümunə:_

    ```js
    const meyve = ["alma", "armud", "banan", "nar"];
    console.log(meyve.splice(1, 2)); // [ 'armud', 'banan' ]
    console.log(meyve); // [ 'alma', 'nar' ]
    ```

    ```js
    const meyve = ["alma", "armud", "banan", "nar"];
    console.log(meyve.splice(-2, 1)); // [ 'banan' ]
    console.log(meyve); // [ 'alma', 'armud', 'nar' ]
    ```

    ```js
    const meyve = ["alma", "armud", "banan", "nar"];
    meyve.splice(2, 1, "kivi");
    console.log(meyve); // [ 'alma', 'armud', 'kivi', 'nar' ]

    meyve.splice(1, 0, "gilas");
    console.log(meyve); // [ 'alma', 'gilas', 'armud', 'kivi', 'nar' ]

    meyve.splice(3, 0, "ananas", "heyva");
    console.log(meyve); // [ 'alma', 'gilas', 'armud', 'ananas', 'heyva', 'kivi', 'nar' ]
    ```

<br />

43. ### What is the difference between slice and splice?

    Aşağıdakı cədvəldə aralarındakı əsas fərqlər var.

    |                                   splice() metodu                                   |                                     slice() metodu                                     |
    | :---------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------: |
    |                             Orijinal massivi dəyişdirir                             |                              Orijinal massivi dəyişdirmir                              |
    | Mövcud elementləri əvəz etmək, silmək və yaxud yerini dəyişmək üçün istifadə olunur | Verilmiş başlanğıcdan verilmiş sona qədər olan elementləri seçmək üçün istifadə olunur |
    |                            Silinmiş elementləri qaytarır                            |                     Seçilmiş elementləri yeni massiv kimi qaytarır                     |
    |            Nəticənin hər hansı dəyişənə təyin edilməsinə ehtiyac yoxdur             |                           Nəticə dəyişənə təyin edilməlidir                            |
    |                            n sayda arqument götürə bilər                            |                                   2 arqument götürür                                   |

<br />

44. ### What is a first class function?

    JavaScript dili birinci dərəcəli funksiyalara (first class function) malikdir. Funksiyaların dəyişən olaraq qəbul edilə bilməsi halına birinci dərəcəli funksiyalar deyilir. Birinci dərəcəli funksiyalar başqa funksiyalara arqument kimi ötürülə bilər, başqa funksiya tərəfindən qaytarıla bilər və dəyişənə dəyər kimi təyin edilə bilər.

    _Nümunə:_

    ```js
    const myFunc = function () {
      console.log(55);
    };
    myFunc(); // 55
    ```

    ```js
    const myFunc = (num) => () => {
      console.log(num + 25);
    };
    myFunc(55)(); // 80
    ```

<br />

45. ### What is the purpose of the delete operator?

    `delete` operatoru obyektdən xüsusiyyəti (və onun dəyərini) silir.

    _Nümunə:_

    ```js
    const obj = {
      name: "Orkhan",
      surname: "Shahbaz",
    };

    delete obj.surname;
    console.log(obj); // { name: 'Orkhan' }
    console.log(obj.surname); // undefined
    ```

<br />

46. ### How do you access history in JavaScript?

    JavaScriptdə `window.history` obyekti brauzer tarixçəsini saxlayır və "window" prefiksi olmadan da yazıla bilir. `Window.history` obyektinin `history.back` və `history.forward` metodlarından istifadə edərək tarixçədə əvvəlki və sonrakı URL-ləri yükləmək olar.

    _Nümunə:_

    Buttona klik edəndə sonrakı səhifəyə gedəcək.

    ```html
    <input type="button" value="Forward" onclick="goForward()" />
    ```

    ```js
    function goForward() {
      history.forward();
    }
    ```

<br />

47. ### What is the purpose of isFinite function?

    `isFinite()` metodu verilən dəyərin sonlu ədəd olub-olmamasını yoxlayır və boolean (true və ya false) dəyər qaytarır. Əgər dəyər Infinity, -Infinity və NaN (**N**ot-**a**-**N**umber) olarsa false, qalan hallarda true qaytarır.

    _Nümunə:_

    ```js
    console.log(isFinite(Infinity)); // false
    console.log(isFinite(-Infinity)); // false
    console.log(isFinite(NaN)); // false
    console.log(isFinite(undefined)); // false
    console.log(isFinite(0)); // true
    console.log(isFinite(52)); // true
    ```

<br />

48. ### How do you sort elements in an array?

    JavaScriptdə `sort()` metodu massivdəki elementləri sıralayır və sıralanmış massivi qaytarır.

    _Nümunə:_

    Bu zaman elementlər əlifba sırasına görə sıralanacaq.

    ```js
    const meyveler = ["alma", "gilas", "banan", "armud", "kivi"];
    meyveler.sort();
    console.log(meyveler); // [ 'alma', 'armud', 'banan', 'gilas', 'kivi' ]
    ```

    Bu zaman ədədlər kiçikdən böyüyə doğru (artan sıra ilə) sıralanacaq.

    ```js
    const ededler = [1, 25, 52, 50, 21, 10];
    ededler.sort();
    console.log(ededler); // [ 1, 10, 21, 25, 50, 52 ]
    ```

<br />

49. ### How do you define multiline strings?

    "&#92;" simvolundan istifadə edərək çoxsətirli stringləri təyin etmək olar. Bu zaman hər sətrin sonuna "&#92;" simvolunu yazmaq lazımdır. Əgər "&#92;" simvolundan sonra boşluq qoyulsa görünüşdə heç bir dəyişiklik olmayacaq, amma belə bir `SyntaxError: Invalid or unexpected token` error verəcək.

    _Nümunə:_

    ```js
    let text =
      "Bura \
    heç nə \
    yazmayacam.";

    console.log(text); // Bura heç nə yazmayacam.
    ```

<br />

50. ### Can we define properties for functions?

    Bəli, funksiyalara xüsusiyyətlər təyin etmək olar, çünki JavaScriptdə funksiyalar birinci dərəcəli obyektlərdir (first-class objects). Funksiyalar ilə obyektləri bir-birindən fərqləndirən cəhət funksiyaların çağırıla bilən olmasıdır. Funksiyalara çağırıla bilən obyektlər də demək olar.

    _Nümunə:_

    ```js
    let myFunc = function () {
      myFunc.surname = "Objects";
    };

    myFunc();

    console.log(myFunc.surname); // Objects
    ```

    #### ⬆ [Yuxarıya qayıt](https://github.com/isbendiyarovanezrin/JavaScriptQuestionsAndAnswers#readme)

    ### Sualları [bu](https://github.com/sudheerj/javascript-interview-questions "Click me! 🙃") repodan götürmüşəm.
