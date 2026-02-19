# c2
Браузерный калькулятор

## Деплой на Vercel

### Через Vercel CLI

1. Установите Vercel CLI (один раз):
   ```powershell
   npm i -g vercel
   ```

2. В корне проекта выполните:
   ```powershell
   vercel
   ```
   Следуйте подсказкам (логин при первом запуске, имя проекта). Для продакшн-деплоя:
   ```powershell
   vercel --prod
   ```

### Через веб-интерфейс (GitHub/GitLab/Bitbucket)

1. Зайдите на [vercel.com](https://vercel.com) и войдите через Git-провайдер.
2. **Add New** → **Project** и импортируйте репозиторий этого проекта.
3. **Framework Preset** выберите **Other** (без сборки). Root Directory оставьте пустым.
4. Нажмите **Deploy**. Калькулятор будет открываться по корневому URL (`/`).

### Что настроено

- Папка **`public/`** — статика (Vercel для «Other» отдаёт файлы из неё). Внутри: `index.html`, `calculator.html`.
- **`vercel.json`** — указан `outputDirectory: "public"`, чтобы Vercel отдавал страницы из этой папки.
