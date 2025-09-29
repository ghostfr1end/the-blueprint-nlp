# Данные

Проект ожидает файл **`data/result.json`** — экспорт сообщений Telegram-канала (формат Telegram Desktop / Telethon).

- Положите файл сюда: `data/result.json` (папка уже игнорируется в git, кроме этого README).
- Данные **не коммитим** в репозиторий (см. `.gitignore`).

### Как загрузить в Colab
- Вручную: выполните ячейку с загрузкой:
  ```python
  from google.colab import files
  uploaded = files.upload()  # выберите result.json

