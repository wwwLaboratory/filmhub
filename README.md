# Filmhub

Filmhub - це сервіс для перегляду фільмів, який по функціоналу віддалено нагадує hdrezka.

## Features

Реалізовані наступні функції для звичайного користувача:

- Реєстрація
- Авторизація
- Перегляд фільму
- Коментування фільму
- Оцінка фільму
- Список рекомендацій
- Вибір випадкового фільма

Також реалізовані панелі для адміністрування і модерування сервісу, а саме:

- Можливість додавання фільму у каталог
- Можливість видалення фільму з каталогу
- Можливість модерування коментарів, їхнє підтвердження або видалення
- Можливість надавати роль адміністратора/модератора

## Usage

Сервіс знаходиться на безкоштовному хостингу heroku. Протестувати можна [тут](https://filmhubb.herokuapp.com).  
Або ж сервіс можна запустити локально, для цього потрібно виконати наступне:

1.  Завантажити проект.
2.  Перевірити чи встановлені nodejs, npm та postgresql, якщо ні - встановити.
3.  Виконати в термiналi

```
cd db
chmod +x ./setup
./setup
npm i
npm start
```

4. Сервiс стане доступний за адресою localhost:8000

### Dockerize

1. Build

```
sudo docker build -f Dockerfile . -t filmhub:latest
```

2. Test

```
sudo docker run --rm -it filmhub:latest npm run test
```

3. Run

```
sudo docker run -p 8000:8000 -p 8001:8001 -p 8002:8002 --rm -it filmhub:latest
```

## Authors

[Гуськов Данило](https://github.com/imnetcat)

[Поліщук Степан](https://github.com/Professor108)

[Маїк Богдан](https://github.com/Storkki)

[Олійник Юлія](https://github.com/Yulia02)

## License

Copyright (c) 2020 WWWLaboratory

This software is [MIT licensed](./LICENSE).
