---
layout: default
title: Метод Auth.Confirm
permalink: auth/confirm/
comments: true
---
# Метод Auth.Confirm
Завершает регистрацию нового пользователя, начатую методом auth.signup, по коду, полученному через SMS.

Страница документации ВКонтакте [auth.confirm](https://vk.com/dev/auth.confirm).

## Синтаксис
``` csharp
public AuthConfirmResult Confirm(AuthConfirmParams @params)
```

## Параметры
Класс **`AuthConfirmParams`** содержит следующие свойства:

+ **ClientId** - Идентификатор Вашего приложения. целое число, обязательный параметр
+ **ClientSecret** - Секретный ключ приложения, доступный в резделе редактирования приложения. строка, обязательный параметр
+ **Phone** - Номер телефона регистрируемого пользователя. Номер телефона может быть проверен заранее методом auth.checkPhone. строка, обязательный параметр
+ **Code** - Код, отправленный пользователю по SMS. строка, обязательный параметр
+ **Password** - Пароль пользователя, который будет использоваться при входе. (Следует передавать только если он не был передан на предыдущем шаге auth.signup) Не меньше 6 символов. строка
+ **TestMode** - 1 — тестовый режим, при котором не будет зарегистрирован новый пользователь, но при этом номер не будет проверяться на использованность. 0 — (по умолчанию) рабочий. флаг, может принимать значения 1 или 0
+ **Intro** - Битовая маска отвечающая за прохождение обучения использованию приложения. положительное число

## Результат
В случае успешного завершения авторизации таким способом будет возвращён объект, содержащий поля success = 1 и uid = идентификатор зарегистрированного пользователя.

## Пример
``` csharp
// Пример кода
```

## Версия Вконтакте API v.5.44
Дата обновления: 28.01.2016 14:06:14