# Требования к проекту

# Содержание
1 [Введение](#intro)   
2 [Требования пользователя](#user_requirements)  
2.1 [Программные интерфейсы](#software_interfaces)  
2.2 [Интерфейс пользователя](#user_interface)  
2.3 [Характеристики пользователей](#user_specifications)  
2.4 [Предположения и зависимости](#assumptions_and_dependencies)  
3 [Системные требования](#system_requirements)  
3.1 [Функциональные требования](#functional_requirements)  
3.2 [Нефункциональные требования](#non-functional_requirements)  
3.2.1 [Атрибуты качества](#quality_attributes)  
3.2.2 [Требования к безопасности](#security_requirements)  

<a name="intro"/>

# 1 Введение

Web-приложение YnAirline. YnAirline – это система автоматизации процессов внутри  авиакомпании. Авиакомпания имеет список рейсов. Диспетчер формирует летную Бригаду (пилоты, штурман, радист, стюардессы) на Рейс. Администратор управляет списком рейсов. Приложение является кроссплатформенным, так как выполнено в виде веб-сервиса.

<a name="user_requirements"/>

# 2 Требования пользователя

<a name="software_interfaces"/>

## 2.1 Программные интерфейсы

Приложение использует язык программирования Java. Приложение создано с использованием Java EE. Так же приложение использует Tomcat 9.0.64. Используемая база данных в приложении это - MySQL.

<a name="user_interface"/>

## 2.2 Интерфейс пользователя

## Окно для входа в аккаунт сотрудника авиакомпании.

![New Wireframe 1](https://user-images.githubusercontent.com/45950020/192600383-23be4f31-d0fd-4d45-8e5f-86614f1e42ac.png)

Рисунок 1. Окно входа

## Окно сотрудника

При нажатии на кнопку "List of flights" выводятся ближайшие рейсы, в которых учавствует сотрудник.

![New Wireframe 2](https://user-images.githubusercontent.com/45950020/192599908-0d8a0527-1279-4044-8863-be5c87e55ed9.png)

Рисунок 2. Рабочее пространство сотрудника

![image](https://user-images.githubusercontent.com/45950020/180441995-d14f6dc0-8de4-4e94-ad5c-941f8f57f5d0.png)

Рисунок 3. Начальная страница при открытии сайта.

При авторизации как администратор, открывается страница с множеством кнопок и списком ближайших рейсов. Красным выделяются рейсы на которые ещё не сформирована лётная бригада, зелёным - если бригада сформирована.

![image](https://user-images.githubusercontent.com/45950020/180442324-df8db15a-2625-42bf-bb37-892aff9d6fdf.png)

Рисунок 4. Страница при входе в аккаунт <b>Администратора</b>

При нажатии на кнопку "Новый рейс", открывается страница с формой для создания нового рейса, рисунок 5.

![image](https://user-images.githubusercontent.com/45950020/199573970-2920d7da-c43c-4fd2-ad7b-372738ac5c73.png)

Рисунок 5. Страница создания нового рейса

При нажатии на кнопку "Новый пользователь", открывается страница с формой для создания аккаунта для нового сотрудника, рисунок 6.

![image](https://user-images.githubusercontent.com/45950020/199574429-fa391af1-717b-4a6a-90a2-d8679a02d02f.png)

Рисунок 6. Страница создания нового пользователя

При нажатии на кнопку "Список пользователей", открывается страница со списком пользователей, рисунок 7. При наведении на пользователя, изменяется заливка строки, а при нажатии открывается страница с подробной информацией о пользователе, рисунок 8.

![image](https://user-images.githubusercontent.com/45950020/199577757-a39e1135-cde1-4a01-98de-82dba6290987.png)

Рисунок 7. Страница со списком пользователей

![image](https://user-images.githubusercontent.com/45950020/199578022-6659dfd4-e327-4267-90a6-0e9ededdce48.png)

Рисунок 8. Страница с подробной информацией о пользователе.

При авторизации как диспетчер. Открывается страница с ближайшими рейсами, где красным цветом выделяются рейсы, на которых бригада не сформирована, а зелёным, на которые сфармирована, рисунок 9.

![image](https://user-images.githubusercontent.com/45950020/199581299-8bef5138-10be-4ff9-bed3-4edd0869d222.png)

Рисунок 9. Страница при входе как диспетчер

При нажатии рейс, открывается страница, где можно составить бригаду на рейс, если кто-то из членов экипажа уже добавлен - они должны быть видны, если никого нет, то сообщение: "Команда пуста". Так же есть различные кнопки для добавления сотрудников на рейс, рисунок 10.

![image](https://user-images.githubusercontent.com/45950020/199581664-fb2c970e-fcb4-496a-8a69-959fed7454df.png)


Рисунок 10. Страница с информацией о рейсе

<a name="user_specifications"/>

## 2.3 Характеристики пользователей

Пользователи приложения – сотрудники авиакомпании. Это люди всех возрастных категорий которые обладают минимальной технической грамотностью. Которые обладают средним образованим.
Администратор и диспетчер – люди которые являются уверенными пользователями ПК. 

Роли пользователей:
- Администратор:
Создаёт пользователей, редактирует информацию о пользователях, создаёт новые рейсы, редактирует созданные рейсы.

- Диспетчер:
Формирует лётную бригаду на рейс, добавляет/удаляет пользователей с рейса.

- Пилоты и различный стафф:
Просмотр ближайших рейсов, где их добавил диспетчер.


<a name="assumptions_and_dependencies"/>

## 2.4 Предположения и зависимости

Для работы приложения требуется устройство с доступом в Интернет и браузером (Safari/Chrome). Рекомендуемый размер экрана более 13.3 диагональю. Не рекомендуется использовать на сматрфоне, возможна работа на планшете. 


<a name="system_requirements"/>

# 3 Системные требования

Приложение требует установленного Tomcat 9.0.64 и базы данных MySQL на сервере компании. Для обеспечения качественной работы приложения, требуется системы хранения данных для среднего и крупного бизнеса. 

<a name="functional_requirements"/>

## 3.1 Функциональные требования

1. Вход в аккаунт
2. Просмотр ближайших рейсов
3. Просмотр отправленных рейсов
4. Создание рейсов
5. Редактирование рейсов
6. Создание аккаунта для сотрудника
7. Редактирование информации о сотруднике
8. Создание бригады на рейс
9. Редактирование бригады на рейс

При создании пользователя в поле логина вводить латиницу и формат email. В поле пароль вводятся любые символы от 3 до 10 символов. В поле ФИО должно быть минимум два пробела. Пол можно выбрать между мужчина/женщина. Должность можно выбрать из следующих: Пилот/Штурман/Радист/Диспетчер/Стюардесса. Возраст должно быть числом  от 18 до 150. Телефон в формате +375(XX)XXX-XX-XX. Место жительства должно быть на кириллице.

<a name="non-functional_requirements"/>

## 3.2 Нефункциональные требования

<a name="quality_attributes"/>

## 3.2.1 АТРИБУТЫ КАЧЕСТВА

Атрибуты, важные для пользователей:  
1. Переносимость данных. Все данные должны легко переноситься между системами и разными версиями приложения.  
2. Удобство и простота использования. Интерфейс должен быть интуитивно понятен и не вызывать трудностей при работе с ним.  
3. Приложение не должно требовать дополнительных библиотек(кроме системных) и предустановленных программ, влияющих на работоспособность приложения.

Атрибуты, важные для разработчиков:  
1. Лёгкость в эксплуатации. Вложенность вызываемых функций не должна превышать 7 уровней.  
2. Лёгкость в эксплуатации. Для каждого программного модуля непустые комментарии в соотношении к исходному коду должны составлять как минимум 0,1.  
3. Тестируемость. Максимальная цикломатическая сложность модуля (количество логических ответвлений в модуле исходного кода) не должна превышать 43.

<a name="security_requirements"/>

## 3.2.2 Требования к безопасности

Пользовательская база приложения распологается на сервере. Авиакомпания несёт ответственность за сохранность персональных данных.

Загрузка и отображение основного окна программы не должны превышать 1 секунд.





