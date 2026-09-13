
### 3. `lab1/go/COMMANDS.md`

# Go REST API (net/http)

Порт за замовчуванням: `8080`

## Ініціалізація модуля (якщо завантажено з нуля)
```bash
go mod tidy

```

## Запуск сервера

```bash
go run main.go

```

## Перевірка ендпойнтів (PowerShell)

### 1. Health Check

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/health" -Method Get

```

### 2. Отримати всі книги (GET /books)

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books" -Method Get

```

### 3. Отримати книгу за ID (GET /books/{id})

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books/1" -Method Get

```

### 4. Створити нову книгу (POST /books)

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books" -Method Post -ContentType "application/json" -Body '{"title": "Dune", "author": "Frank Herbert"}'

```

### 5. Оновити книгу (PUT /books/{id})

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books/1" -Method Put -ContentType "application/json" -Body '{"title": "1984 (Updated)", "author": "George Orwell"}'

```

### 6. Видалити книгу (DELETE /books/{id})

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books/1" -Method Delete

```

### 7. Перевірка 404 Not Found

```powershell
Invoke-RestMethod -Uri "http://localhost:8080/books/999" -Method Get

```


