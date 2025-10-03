# Library Management REST API

Система управління бібліотекою з повним REST API.

## 📚 Опис проекту

Це REST API для управління бібліотекою, яке підтримує:
- Управління книгами, авторами та категоріями
- Систему запозичень та резервувань
- Автентифікацію та авторизацію користувачів
- Повний CRUD для всіх ресурсів

## 🎯 Особливості

- ✅ RESTful дизайн (Richardson Level 3 - HATEOAS)
- ✅ JWT автентифікація
- ✅ Role-based access control (ADMIN, LIBRARIAN, MEMBER)
- ✅ Пагінація всіх колекцій
- ✅ Ефективне кешування з ETag
- ✅ Детальна обробка помилок
- ✅ API Versioning

## 📖 Документація

Повна документація API знаходиться у файлі [API_DESIGN.md](./API_DESIGN.md)

## 🏗️ Архітектура

### Сутності:
- **Book** - Книги бібліотеки
- **Author** - Автори книг
- **Category** - Категорії книг
- **User** - Користувачі системи
- **Loan** - Запозичення книг
- **Reservation** - Резервування книг

## 🔗 Base URL
https://api.library.example.com/v1

## 🚀 Швидкий старт

### Реєстрація користувача
```bash
curl -X POST https://api.library.example.com/v1/auth/register \
  -H "Content-Type: application/json" \
  -d '{
    "email": "user@example.com",
    "password": "SecurePass123!",
    "firstName": "Іван",
    "lastName": "Петренко",
    "dateOfBirth": "1990-05-15"
  }'