# COVID-19 Radiography Segmentation

## 📋 Описание

Этот проект направлен на решение задачи сегментации медицинских изображений рентгенографии с использованием модели **U-Net++**. Мы используем датасет COVID-19 Radiography Dataset для разработки и тестирования модели, а также применяем современные методы аугментации данных для улучшения качества модели.

## Особенности:
1. **Данные**: Используется открытый датасет COVID-19 Radiography Dataset.
2. **Сегментация**: Задача заключается в выделении областей на изображениях с аномалиями.
3. **Модель**: Используется архитектура **U-Net++**, подходящая для задач сегментации изображений.
4. **Аугментация**: Применяется библиотека `Albumentations` для улучшения данных.
5. **Реализация**: Полный пайплайн, включая загрузку данных, предобработку, генерацию данных, обучение модели и визуализацию результатов.

## 🛠️ Зависимости

- Python 3.8+
- TensorFlow/Keras
- NumPy
- Pandas
- Albumentations
- Matplotlib
- Opendatasets

Установите зависимости через pip:
```bash
pip install tensorflow keras albumentations opendatasets numpy pandas matplotlib
```

## 📂 Данные

## Загрузка:
Датасет доступен на Kaggle. Для загрузки выполните:

```python
import opendatasets as od
od.download("https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database/")
```

## Структура

- **Изображения**: `COVID-19_Radiography_Dataset/Normal/images/`
- **Маски**: `COVID-19_Radiography_Dataset/Normal/masks/`


## 📊 Производительность

- **Batch Size**: `32` (оптимальное значение после тестирования).
- **Метрики**: 
  - `Accuracy`
  - `IoU` (Intersection over Union)

## Аугментация:
- Случайные повороты на 90°.
- Отражения.
- Случайный снег.

