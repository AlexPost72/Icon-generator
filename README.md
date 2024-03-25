# Icon-generator
# Генератор Иконок с Использованием Модели Диффузии

Этот проект предназначен для создания уникальных иконок с помощью модели диффузии. Модель обучается на существующем наборе данных иконок и способна генерировать новые изображения, имитируя стиль исходных данных.

## Установка зависимостей

Для работы с проектом необходимо установить следующие пакеты:

```shell
python3 -m pip install diffusers==0.21.* numpy torch torchvision matplotlib PIL accelerate datasets huggingface_hub tqdm
```

# Структура проекта
Проект включает следующие ключевые компоненты:

1) Подготовка данных: Преобразование исходных изображений иконок к квадратному формату и нормализация данных.
2) Модель диффузии: Использование UNet2DModel и DDPMScheduler для генерации иконок.
3) Обучение модели: Настройка параметров обучения через класс TrainingConfig и выполнение обучения модели.
4) Генерация иконок: Создание новых иконок на основе обученной модели.

# Подготовка данных
* Перед обучением модели необходимо подготовить исходные данные, преобразовав изображения к квадратному формату с помощью функции expand2square. Это обеспечивает единообразие входных данных для модели.

# Обучение модели
* Конфигурация обучения задаётся через TrainingConfig, включая размер изображения, количество шагов инференции и другие параметры. В процессе обучения модели генерируются логи и сохраняются результаты.

# Генерация иконок
* После обучения можно использовать модель для генерации новых иконок. Процесс обратной диффузии преобразует начальный шум в изображения, стилизованные под обучающий набор данных.

# Ссылка на датасет:
[Icons50 Dataset on Kaggle](https://www.kaggle.com/datasets/danhendrycks/icons50/code)

# Ссылка на юпитер ноутбук:
[ipynb]()

