![Google Colab](https://img.shields.io/badge/Google%20Colab-%23F9A825.svg?style=for-the-badge&logo=googlecolab&logoColor=white)![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)![Kaggle](https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white)![Google Drive](https://img.shields.io/badge/Google%20Drive-4285F4?style=for-the-badge&logo=googledrive&logoColor=white)

## YOLOv8-vehicle-detection

Современный мир уже трудно представить без камер видеонаблюдения. Такие камеры уже оснащены детекцией автомобилей, номерных знаков и так далее. Не всегда получаются качественные изображения транспортных средств, что приводит к сложностям детекции в связи с ограниченной освещенностью. Для решения подобных задачи можно использовать модели **YOLO** от компании **Ultralytics**. Из семейства этих моделей была выбрана **8** версия. Почему? Она сочетает в себе зрелость экосистемы **Ultralytics** и современную архитектуру, эта модель обладает расширенными возможностями по сравнению с предшественниками, а именно: сегментация экземпляров, оценка позы/ключевых точек и классификация.

> Настоятельно рекомендую использовать **графический ускоритель T4** или
> мощнее!

В качества датасета будет использоваться [Cars Detection](https://www.google.com/url?q=https%3A%2F%2Fwww.kaggle.com%2Fdatasets%2Fabdallahwagih%2Fcars-detection%2Fdata). Для того, чтобы его скачать, нам потребуется зарегистрироваться на **Kaggle** и получить свой _API-ключ_ через настройки профиля.

Для достижения поставленной задачи - детекция транспортных средств в условиях ограниченной освещенности, будем использовать аугментацию изображений. В коде есть возможность добавление в итоговый датасет только аугментированных изображений, а также оригинальные + аугментированные.

Будем использовать среднюю модель `yolo8m.pt`, которая предобучена для работы с обнаружением объектов. Так как я ограничен вычислительными ресурсами, то я выбрал среднюю модель, но вы можете выбрать более сложную модель, которая будет способна выдавать результаты лучше, но она будет ресурсозатратнее.

> Более подробная информация по написанию кода, а также теоретическая
> часть и выводы представлены в самом **Google Colab Notebook**!