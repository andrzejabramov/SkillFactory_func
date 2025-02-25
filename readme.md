 # Task1
 Условие: QA-инженеры часто сталкиваются с задачей тестирования функций, связанных с обработкой паролей. Для этого им нужно убедиться, что пароль, введённый пользователем, соответствует определённым требованиям.
Напишите функцию check_password, которая принимает пароль в виде строки и проверяет, что:

длина пароля не менее 8 символов;
в пароле есть хотя бы одна заглавная буква;
в пароле есть хотя бы одна строчная буква;
в пароле есть хотя бы одна цифра.
Функция должна выводить сообщение, если пароль не соответствует какому-либо из этих условий. Сообщения, которые должна выводить функция, вы можете увидеть в примере работы.

Пример работы:

Если не соблюдены все условия:


check_password("_")
#### Пароль должен быть не менее 8 символов
#### Пароль должен содержать хотя бы одну заглавную букву
#### Пароль должен содержать хотя бы одну строчную букву
#### Пароль должен содержать хотя бы одну цифру
Если не соблюдена часть условий:


check_password("password")
#### Пароль должен содержать хотя бы одну заглавную букву
#### Пароль должен содержать хотя бы одну цифру
Условия соблюдены:


check_password("Password1")

----------------------------
# Task2

Условие: При тестировании программного обеспечения QA-инженерам часто нужно проводить тесты, где они должны проверить, что число попадает в определённый диапазон.
Для такого тестирования вам необходимо реализовать функцию test_range, которая принимает число и две границы диапазона, а затем выводит сообщение, если число не попадает в диапазон.
Порядок аргументов: число, начало диапазона, конец диапазона. Диапазон включает начало и конец (>= и <=).

Пример работы:

Допущена ошибка:


test_range(15, 1, 10)
#### Число 15 не попадает в диапазон между 1 и 10
Ошибки нет:


test_range(5, 1, 10)

---------------------------------
# Task3

Условие: При тестировании веб-приложений QA-инженерам часто требуется проверять коды ответа HTTP.
Напишите функцию is_success_code(), которая принимает код ответа HTTP и возвращает True, если это код успешного ответа (в диапазоне 200-299), и False в противном случае. Передаваемое значение имеет имя code!
Пример работы:


print(is_success_code(200))
print(is_success_code(404))
#### True
#### False

---------------------------------------------
# Task4

Условие: QA-инженеры часто сталкиваются с необходимостью проверять валидность email-адресов в различных формах регистрации.
Напишите функцию is_valid_email(), которая принимает email в виде строки и возвращает True, если email:

содержит символ "@";
содержит хотя бы одну точку после символа "@";
не содержит пробелов.
В противном случае функция должна возвращать False.

Пример работы:


print(is_valid_email("user@example.com"))
print(is_valid_email("user at example dot com"))

#### True
#### False

----------------------------
# Task5

Условие: Во время автоматизированного тестирования часто требуется проверить, возвращает ли функция ожидаемый результат.
Напишите функцию test_function(), которая принимает:
1. другую функцию, которая принимает один аргумент — имя функции,
2. аргумент для этой функции,
3. ожидаемый результат.
Функция test_function() должна возвращать True, если функция возвращает ожидаемый результат, и False в противном случае.

Пример работы:


#### Пример функции для тестирования
def square(n):
   return n ** 2

print(test_function(square, 4, 16))  # Передаем имя функции
print(test_function(square, 5, 20))

#### True
#### False

-----------------------------
# Task6

Условие: В этом задании вам предстоит усовершенствовать функцию проверки пароля, добавив в неё значения по умолчанию, которыми будет определяться необходимость проверки того или иного параметра пароля.
Напишите функцию is_valid_password(), которая принимает пароль в виде строки и проверяет его на соответствие следующим критериям:

длина не менее 8 символов;
есть хотя бы одна заглавная буква;
есть хотя бы одна строчная буква;
есть хотя бы одна цифра.
Функция должна иметь параметры по умолчанию, определяющие требования к паролю, чтобы можно было настроить проверку в соответствии с потребностями безопасности: min_length=8, require_upper=True, require_lower=True, require_digit=True.

Пример работы:


print(is_valid_password("Password123"))
#### True
print(is_valid_password("password"))
#### False
print(is_valid_password("Password123", min_length=12))
#### False

----------------------------
# Task7

Условие: Реализуйте функцию generate_test_data(), которая генерирует список из n случайных чисел в заданном диапазоне. Параметры функции должны включать количество генерируемых чисел, минимальное и максимальное значения диапазона. Также все они должны иметь значения по умолчанию: n=5, min_value=1, max_value=10.

Примечание: вам понадобится импортировать встроенный модуль random.

Пример работы:


print(generate_test_data())
#### [6, 6, 5, 10, 10]

print(generate_test_data(n=3, min_value=-5, max_value=5))
#### [3, 4, 3]

-------------------------------
# Task8

Условие: В этом задании вам необходимо реализовать функцию format_date(), которая принимает дату в формате "гггг-мм-дд" и возвращает её в заданном формате. Функция должна иметь параметр по умолчанию для формата вывода равный "dmy". Все возможные форматы вы увидите в примере работы.

Пример работы:


print(format_date("2023-07-01"))
#### 01072023
print(format_date("2023-07-01", format="dmy"))
#### 01072023
print(format_date("2023-07-01", format="mdy"))
#### 07012023
print(format_date("2023-07-01", format="ymd"))
#### 20230701

-----------------------------
# Task9

Условие: В этом задании вам необходимо реализовать функцию compare_lists(), которая принимает два списка и возвращает список элементов, которые есть в первом списке, но отсутствуют во втором. Функция должна иметь параметр по умолчанию ignore_case=False, который позволяет игнорировать регистр при сравнении строк.

Пример работы:


print(compare_lists(["apple", "banana", "cherry"], ["Banana", "cherry", "date"]))
#### ["apple", "banana"]
print(compare_lists(["apple", "banana", "cherry"], ["Banana", "cherry", "date"], ignore_case=True))
#### ["apple"]

------------------------------
# Task10

Условие: Вы проводите автоматическое тестирование времени ответа сервера. Вам необходимо написать функцию calculate_average(*args), которая принимает список времени ответа и возвращает среднее значение.

Пример использования:


print(calculate_average(1.2, 0.9, 1.3, 1.1, 1.7))
#### 1.24

-------------------------------
# Task11

Условие: Вы работаете над автоматизированным тестированием веб-сайта, где данные пользователя передаются в формате JSON. Вам нужно написать функцию sort_data(**kwargs), которая будет принимать данные пользователя и возвращать их, отсортированные по ключам.

Пример работы:


print(sort_data(name='Alex', age=30, city='New York'))
#### [('age', 30), ('city', 'New York'), ('name', 'Alex')]

---------------------------------
# Task12

Условие: Ваши разработчики внедряют новый алгоритм сортировки пользователей на сайте. Он учитывает множество параметров, но для начальной проверки вы решили сфокусироваться только на именах пользователей. Пользователи отображаются в списке, и вы должны проверить, корректно ли работает сортировка по последнему символу в имени пользователя. Создание подобной функции поможет вам генерировать тестовые данные для проверки этого алгоритм.

Вам необходимо реализовать функцию sort_strings_by_last_char, использующую лямбда-функцию, которая будет сортировать список строк по последнему символу в каждой строке.

Пример работы:


strings = ["apple", "banana", "cherry", "date", "elderberry"]
print(sort_strings_by_last_char(strings))
#### ['banana', 'apple', 'date', 'elderberry', 'cherry']

------------------------------
# Task13

Условие: Ваша команда добавляет новую функцию рейтинга пользователей в ваше приложение. Это включает применение некоторой математической функции к набору данных для каждого пользователя, чтобы вычислить его рейтинг.

Ваша задача: протестировать эту функцию на различных наборах данных и убедиться, что она работает правильно. Для этого вы создаете функцию, которая позволяет применять различные функции к набору данных.

Создайте функцию apply_function, которая будет принимать список чисел и функцию, преобразующую числа. Ваша функция должна применять преобразующую функцию (которая будет представлена как лямбда-функция) к каждому числу в списке и возвращать обновленный список.

Пример работы:


numbers = [1, 2, 3, 4, 5]
print(apply_function(numbers, lambda x: x**2))
#### [1, 4, 9, 16, 25]

--------------------------------
# Task14

Условие: Вам нужно обработать данные о продажах, которые представлены в виде списка списков. Каждый внутренний список представляет собой запись о продаже и содержит следующую информацию: ["название товара", количество, цена за единицу].

Напишите функцию, которая принимает такой список списков, и ключевые аргументы, которые определяют, какую статистику нужно вернуть: общий доход или количество проданных единиц каждого товара.

Пример работы:


sales_data = [["яблоки", 10, 20], ["груши", 5, 30], ["яблоки", 7, 20]]
print(sales_stats(sales_data, revenue=True))
#### (490, None)
print(sales_stats(sales_data, quantity=True))
#### (None, {'яблоки': 17, 'груши': 5})
При этом ваша функция должна отрабатывать корректно, если ей были переданы сторонние ключевые аргументы:


print(sales_stats(sales_data, customers=True))
#### (None, None)
Ваша задача:только реализовать функцию sales_stats, вызывать её не нужно.

----------------------------
# Task15

Условие: Напишите функцию create_report, которая автоматически создает отчеты. Отчет представляет собой строку, которая содержит информацию о среднем доходе и общем количестве проданных единиц товара за определенный период. Функция должна принимать на вход данные о продажах (в том же формате, что и в задаче выше) и функцию, которую нужно использовать для обработки этих данных (функция из предыдущей задачи).

Пример работы:


sales_data = [["яблоки", 20, 20], ["груши", 5, 30], ["яблоки", 7, 20]]
print(create_report(sales_data, sales_stats))
#### Средний доход за данный период составил 230.0.
#### Количество проданных единиц каждого товара:
#### яблоки: 27
#### груши: 5

----------------------------------------
# Task16

Условие: У вас есть данные об активности пользователей в формате словаря, где ключ — идентификатор пользователя, а значение — количество его активностей.

Напишите функцию sort_users_by_activity, которая будет возвращать список пользователей, отсортированных по уровню активности в порядке убывания. Функция sorted должна использоваться с аргументом key и лямбда-функцией.

Пример работы:


user_activity = {"user1": 10, "user2": 5, "user3": 20, "user4": 15, "user5": 10}
print(sort_users_by_activity(user_activity))
#### ['user3', 'user4', 'user1', 'user5', 'user2']

-----------------------------
















