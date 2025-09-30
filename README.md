# the-blueprint-nlp

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ghostfr1end/the-blueprint-nlp/blob/main/notebooks/TheBlueprint_project_clean_1.ipynb)

NLP-анализ Telegram-канала **The Blueprint** за март–май 2025: эмбеддинги + векторный поиск (FAISS), n-граммы, таймлайны событий/трендов.

## Быстро посмотреть
- 📓 Основной ноутбук: `notebooks/TheBlueprint_project_clean.ipynb` (кнопка Colab выше).
- ⚡ TL;DR:
     Весенняя повестка канала следует календарю индустрии; мода – брендоцентрична, рубрика о культуре завязана на новостях и ивентах, сфера красоты и здоровья фокусируется на бьюти-советах, образе жизни и зависит от сезона. Метод дал быстрые и полезные срезы; для «идеала» нужны более мелкие чанки, детальнее запросы и лёгкая пост-фильтрация.
- 🖼 Превью результатов:
  - Таймлайн упоминаний (ивенты/бренды/микротренды):  
    ![timeline](assets/timeline.png)
  - Топ биграмм по рубрикам (бар-чарты):  
    ![bars](assets/bigrams.png)

## Стек
`sentence-transformers (paraphrase-multilingual-mpnet-base-v2)`, `FAISS`, `pandas`, `numpy`, `scikit-learn (TfidfVectorizer)`, `matplotlib`.

## Как запустить
**В Colab:** нажмите на бейдж выше и следуйте ячейкам (загрузите `data/result.json` при запросе).  
**Локально:**
```bash
git clone https://github.com/ghostfr1end/the-blueprint-nlp.git
cd the-blueprint-nlp
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook notebooks/TheBlueprint_project_clean.ipynb
