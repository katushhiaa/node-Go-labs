# Node.js REST API (Express)

Порт за замовчуванням: `3000`

## Встановлення залежностей
```bash
npm install
```

Перевірка ендпойнтів (PowerShell)
1. Health Check

```bash 
Invoke-RestMethod -Uri "http://localhost:3000/health" -Method Get
```
2. Отримати всі книги (GET /books)

```bash 
Invoke-RestMethod -Uri "http://localhost:3000/books" -Method Get
```
3. Отримати книгу за ID (GET /books/:id)

```bash 
Invoke-RestMethod -Uri "http://localhost:3000/books/1" -Method Get
```
4. Створити нову книгу (POST /books)

```bash
Invoke-RestMethod -Uri "http://localhost:3000/books" -Method Post -ContentType "application/json" -Body '{"title": "Dune", "author": "Frank Herbert"}'
```

5. Оновити книгу (PUT /books/:id)

```bash
Invoke-RestMethod -Uri "http://localhost:3000/books/1" -Method Put -ContentType "application/json" -Body '{"title": "1984 (Updated)", "author": "George Orwell"}'
```

6. Видалити книгу (DELETE /books/:id)

```bash
Invoke-RestMethod -Uri "http://localhost:3000/books/1" -Method Delete 
```
7. Перевірка 404 Not Found

```bash
Invoke-RestMethod -Uri "http://localhost:3000/books/999" -Method Get
```
