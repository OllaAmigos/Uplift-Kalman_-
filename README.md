# Uplift-моделирование с фильтром Калмана

Этот проект демонстрирует использование uplift-моделирования и фильтра Калмана на основе датасета `sklift.datasets.fetch_x5`. Подробнее о датасете в [официальной документации](https://www.uplift-modeling.com/en/latest/api/datasets/fetch_x5.html).

---

## Бизнес-задача

### Сценарий
- Два города: **богатый город (Y)** и **бедный город (X)**.
- Проведение промо-кампании возможно только в богатом городе
- Мы пробуем использовать результаты кампании в богатом городе для прогноза результатов в бедном городе

### Цели
- Спрогнозировать результаты рекламной кампании в бедном городе (X)

### Задачи
1. Подготовить и предобработать необходимые данные.
2. Восстановить скрытые характеристики покупателей в бедном городе (X)
3. Разработать uplift-модель для богатого города (Y)
4. Применить и оценить uplift-модель для бедного города (X)

---

## Техническая постановка задачи

### Дано:
- Данные о потребителях из богатого города (Y)
- Данные имеют панельную структуру, включая:
  - Идентификаторы транзакций
  - Временные метки
  - Суммы покупок
  - Состав корзин

### Задачи:
1. Обучить модель пространственного состояния.
2. Восстановить скрытые состояния с помощью **фильтра Калмана**.
3. Оценить uplift-модель для бедного города (X)

---

## Методология

### Подготовка данных
- Моделирование новых фичей
- Очистка и предобработка панельных данных
- Обеспечение согласованности данных и устранение аномалий


### Фильтр Калмана
- Использование фильтра Калмана для восстановления скрытых состояний, представляющих характеристики покупателей

### Uplift-моделирование
- Обучение uplift-модели на данных из богатого города
- Оценка производительности модели и её обобщение для прогноза в бедном городе

---

## Благодарности
- Библиотека `sklift` за поддержку uplift-моделирования.
- Третьяк Никита, Хубежова Диана, Андросова Ольга - за усердную работу по ночам
