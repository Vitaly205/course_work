# Мобильное приложение для управления банковскими счетами  

## Описание проекта  
Это мобильное приложение, разработанное на языке C# с использованием объектно-ориентированного программирования (ООП). Оно предназначено для управления банковскими счетами и предоставляет пользователям удобный интерфейс для выполнения повседневных банковских операций. Технологии:C#,.NET MAUI,SQLite

### Студент  
**Имя**: Сильчук Виталий Викторович
**Группа**: 353504 

### Диаграмма классов  
Ниже представлена диаграмма классов, иллюстрирующая архитектуру приложения:
*Примечание*: Диаграмма будет уточнена на следующих этапах разработки.  

### Список функций приложения  
1. **Регистрация и вход пользователя**  
   - *Описание*: Пользователь может создать новый аккаунт или войти в существующий.  
   - *Входные данные*: Имя, email, пароль (для регистрации); email и пароль (для входа).  
   - *Выходные данные*: Сообщение о успешной регистрации или входе.  

2. **Просмотр баланса счета**  
   - *Описание*: Пользователь может увидеть текущий баланс выбранного счета.  
   - *Входные данные*: Выбор счета из списка.  
   - *Выходные данные*: Текущий баланс счета.  

3. **Совершение переводов**  
   - *Описание*: Пользователь может перевести деньги между своими счетами или на другой счет.  
   - *Входные данные*: Номер счета отправителя, номер счета получателя, сумма перевода.  
   - *Выходные данные*: Подтверждение перевода или сообщение об ошибке (например, "Недостаточно средств").  

4. **Просмотр истории транзакций**  
   - *Описание*: Пользователь может просмотреть список всех операций по выбранному счету.  
   - *Входные данные*: Выбор счета.  
   - *Выходные данные*: Список транзакций с указанием даты, суммы и типа (например, "перевод", "пополнение").  

5. **Обновление личных данных**  
   - *Описание*: Пользователь может изменить свои контактные данные.  
   - *Входные данные*: Новые данные (например, email или телефон).  
   - *Выходные данные*: Подтверждение обновления данных.
6. **Создание финансовых целей**
   - *Описание*: Пользователь может установить финансовую цель (например, накопить на отпуск) и отслеживать прогресс.
   - *Входные данные*: Название цели, целевая сумма, срок достижения, счет для накоплений.
   - *Выходные данные*: Подтверждение создания цели, процент выполнения (визуализация прогресса).
7. **Калькулятор кредитов и вкладов**
   - *Описание*: Пользователь может рассчитать условия кредита или доходность вклада прямо в приложении.
   - *Входные данные*: Сумма, процентная ставка, срок.
   - *Выходные данные*: Расчет ежемесячного платежа (для кредита) или итоговой суммы (для вклада).



### Описание моделей данных  
1. **User**  
   - `Id` (string): Уникальный идентификатор пользователя.  
   - `Name` (string): Имя пользователя.  
   - `Email` (string): Адрес электронной почты.  
   - `PasswordHash` (string): Зашифрованный пароль для входа.  

2. **Account**  
   - `AccountNumber` (string): Уникальный номер счета.  
   - `Balance` (decimal): Текущий баланс счета.  
   - `AccountType` (string): Тип счета (например, "сберегательный", "текущий").  

3. **Transaction**  
   - `TransactionId` (string): Уникальный идентификатор транзакции.  
   - `Date` (DateTime): Дата и время выполнения транзакции.  
   - `Amount` (decimal): Сумма транзакции.  
   - `Type` (string): Тип транзакции (например, "перевод", "снятие").  
