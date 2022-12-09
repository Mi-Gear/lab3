Лабораторная работа №5
"JS"

Лабораторная работа №3. «Основы языка JavaScript».

Задачи:

1. Что выведет код ниже?
alert( null || 2 || undefined );1

2.Что выведет код ниже?
alert( alert(1) || 2 || alert(3) );

3. Что выведет код ниже?
alert( 1 && null && 2 );

4. Что выведет alert (И)?
alert( alert(1) && alert(2) );

5. Что выведет этот код?
alert( null || 2 && 3 || 4 );

6. Напишите условие if для проверки, что переменная age находится в диапазоне между 14 и 90 включительно. «Включительно» означает, что значение переменной age может быть равно 14 или 90.

7.Напишите условие if для проверки, что значение переменной age НЕ находится в диапазоне 14 и 90 включительно. Напишите два варианта: первый с использованием оператора НЕ !, второй – без этого оператора.

8. Какие из перечисленных ниже alert выполнятся?
Какие конкретно значения будут результатами выражений в условиях if(...)?

if (-1 || 0) alert( 'first' );
if (-1 && 0) alert( 'second' );
if (null || -1 && 1) alert( 'third' );

9. Проверка логина
важность: 3
Напишите код, который будет спрашивать логин с помощью prompt.

Если посетитель вводит «Админ», то prompt запрашивает пароль, если ничего не введено или нажата клавиша Esc – показать «Отменено», в противном случае отобразить «Я вас не знаю».

Пароль проверять так:

Если введён пароль «Я главный», то выводить «Здравствуйте!»,
Иначе – «Неверный пароль»,
При отмене – «Отменено».
Блок-схема:
 

Для решения используйте вложенные блоки if. Обращайте внимание на стиль и читаемость кода.

Подсказка: передача пустого ввода в приглашение prompt возвращает пустую строку ''. Нажатие клавиши Esc во время запроса возвращает null.

10. Какое последнее значение выведет этот код? Почему?
let i = 3;
while (i) {
  alert( i-- );
}

11. Для каждого цикла запишите, какие значения он выведет. Потом сравните с ответом.

Оба цикла выводят alert с одинаковыми значениями или нет?

Префиксный вариант ++i:

let i = 0;
while (++i < 5) alert( i );

Постфиксный вариант i++

let i = 0;
while (i++ < 5) alert( i );

12. Для каждого цикла запишите, какие значения он выведет. Потом сравните с ответом. Оба цикла выведут alert с одинаковыми значениями или нет?

Постфиксная форма:
for (let i = 0; i < 5; i++) alert( i );

Префиксная форма:
for (let i = 0; i < 5; ++i) alert( i );

13. При помощи цикла for выведите чётные числа от 2 до 10.

14. Перепишите код, заменив цикл for на while, без изменения поведения цикла.
for (let i = 0; i < 3; i++) {
  alert( `number ${i}!` );
}

15. Напишите цикл, который предлагает prompt ввести число, большее 100. Если посетитель ввёл другое число – попросить ввести ещё раз, и так далее. Цикл должен спрашивать число пока либо посетитель не введёт число, большее 100, либо не нажмёт кнопку Отмена (ESC). Предполагается, что посетитель вводит только числа. Предусматривать обработку нечисловых строк в этой задаче необязательно.

16. Натуральное число, большее 1, называется простым, если оно ни на что не делится, кроме себя и 1. Другими словами, n > 1 – простое, если при его делении на любое число кроме 1 и n есть остаток. Например, 5 — это простое число, оно не может быть разделено без остатка на 2, 3 и 4. Напишите код, который выводит все простые числа из интервала от 2 до n. Для n = 10 результат должен быть 2,3,5,7.

17. Напишите if..else, соответствующий следующему switch:
switch (browser) {
  case 'Edge':
    alert( "You've got the Edge!" );
    break;
  case 'Chrome':
  case 'Firefox':
  case 'Safari':
  case 'Opera':
    alert( 'Okay we support these browsers too' );
    break;

  default:
    alert( 'We hope that this page looks ok!' );
}

18. Перепишите код с использованием одной конструкции switch:
 const number = +prompt('Введите число между 0 и 3', '');

if (number === 0) {
  alert('Вы ввели число 0');
}

if (number === 1) {
  alert('Вы ввели число 1');
}

if (number === 2 || number === 3) {
  alert('Вы ввели число 2, а может и 3');
}

19. Следующая функция возвращает true, если параметр age больше 18. В ином случае она запрашивает подтверждение через confirm и возвращает его результат:

function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    // ...
    return confirm('Родители разрешили?');
  }
}
Будет ли эта функция работать как-то иначе, если убрать else?

function checkAge(age) {
  if (age > 18) {
    return true;
  }
  // ...
  return confirm('Родители разрешили?');
}
Есть ли хоть одно отличие в поведении этого варианта?

20. Следующая функция возвращает true, если параметр age больше 18. В ином случае она задаёт вопрос confirm и возвращает его результат.

function checkAge(age) {
  if (age > 18) {
    return true;
  } else {
    return confirm('Родители разрешили?');
  }
}
Перепишите функцию, чтобы она делала то же самое, но без if, в одну строку.

Сделайте два варианта функции checkAge:

Используя оператор ?
Используя оператор ||

21. Напишите функцию min(a,b), которая возвращает меньшее из чисел a и b.

Пример вызовов:
min(2, 5) == 2
min(3, -1) == -1
min(1, 1) == 1

22. Напишите функцию pow(x,n), которая возвращает x в степени n. Иначе говоря, умножает x на себя n раз и возвращает результат.
pow(3, 2) = 3 * 3 = 9
pow(3, 3) = 3 * 3 * 3 = 27
pow(1, 100) = 1 * 1 * ...* 1 = 1
Создайте страницу, которая запрашивает x и n, а затем выводит результат pow(x,n).

23. 7 kyu https://www.codewars.com/kata/highest-and-lowest
24. 7 kyu https://www.codewars.com/kata/disemvowel-trolls
25. 7 kyu https://www.codewars.com/kata/isograms
26. 7 kyu https://www.codewars.com/kata/digits-explosion
27. 6 kyu https://www.codewars.com/kata/handshake-problem
28. 6 kyu https://www.codewars.com/kata/duplicate-encoder
29. 6 kyu https://www.codewars.com/kata/n-th-fibonacci
30. 6 kyu https://www.codewars.com/kata/multiples-of-3-or-5

Ход работы:
```html
<!DOCTYPE html>
<html lang="en">
<script>
    //1
    alert(null || 2 || undefined);
    //2
    alert(alert(1) || 2 || alert(3));
    //3
    alert(1 && null && 2);
    //4
    alert(alert(1) && alert(2));
    //5
    alert(null || 2 && 3 || 4)
        //6
    function inc(age) {
        if (age >= 14 && age <= 90)
            return true;
        return false
    }
    //7
    function exc(age) {
        if (age > 14 && age < 90)
            return true;
        return false
    }
    //8
    if (-1 || 0) alert('first')
    if (-1 && 0) alert('second')
    if (null || -1 && 1) alert('third')
        //9
    function login() {
        if (prompt("Login", "user") == "Админ") {
            switch (prompt("Password")) {
                case "Я главный":
                    alert("Здравствуйте!")
                    break;
                case null:
                    alert("Отменено")
                    break;
                default:
                    alert('Неверный пароль')
                    break;
            }
        } else alert("Я вас не знаю")
    }
    login()
        //10
    let i = 3
    while (i) {
        alert(i--);
    }
    //11
    i = 0;
    while (++i < 5) alert(i);
    i = 0;
    while (i++ < 5) alert(i);
    //12
    for (let j = 0; j < 5; j++) alert(j)
    for (let j = 0; j < 5; ++j) alert(j)
        //13
    for (let n = 2; n < 11;) {
        alert(n)
        n += 2
    }
    //14
    i = 0;
    while (i++ < 3) {
        alert('number ${i}!')
    }
    //15
    function _15() {
        start: i = null;
        while (i == null || i < 100) {
            i = prompt("Введите число больше 100");
        }
    }
    _15();
    //16
    function primal(n) {
        for (let i = 2; i <= n; i++)
            for (let j = 2; j <= i; j++) {
                if ((i % j == 0) && (j != i))
                    break;
                else {
                    alert(i);
                    break;
                }
            }
    }
    primal(40);
    //17
    function _17(browser) {
        if (browser == "Edge")
            alert("You've got the Edge")
        else if (browser == "Chrome" || browser == "Firefox" || browser == "Safari" || browser == "Opera")
            alert("Okay we support these browsers too");
        else alert("We hope that this page looks ok!")
    }
    _17("Opera");
    //18
    function _18() {
        n = +prompt("Введите число между 0 и 3")
        switch (n) {
            case 0:
                alert("Вы ввели число 0")
                break;
            case 1:
                alert("Вы ввели число 1")
                break;
            case 2:
            case 3:
                alert("Вы ввели число 2 или 3")
                break;
        }
    }
    _18();
    //19
    нет
    //20
    function checkAge(age) {
        i = age > 18 ? true : confirm("Родители разрешили?")
        return i;
    }
    checkAge(17)
        //21
    function min(a, b) {
        i = a < b ? a : b;
        return i;
    }
    alert(min(3, 10));
    //22
    function pow(x, n) {
        temp = x;
        for (i = 1; i < n; i++)
            x *= temp;
        return x;
    }
    pow(12, 2);
</script>
</html>
```
