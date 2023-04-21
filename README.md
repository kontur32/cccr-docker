# cccr-docker
docker compose для CCCR

Что необходимо:
1. доступ к терминалу (на винде 10 WSL/Ubuntu)
1. установленный docker

Как запустить:
1. Запустите докер и войдите в терминал
1. Клонируте репозиторий
1. Установите права для чтения и записи на папку с данными [cccr-docker/data](https://github.com/kontur32/cccr-docker/tree/main/data) (и все вложенные) для пользователя, правами которого обладает docker, и запишите путь к этой папке (он потребуется далее)
1. Перейдите в папку [cccr-docker/docker](https://github.com/kontur32/cccr-docker/tree/main/docker)
1. Запустите сборку образов командой `docker-compose build`
1. Запустите контейнеры командой `DATA_DIR=полный_путь_к_паке_с_данными docker-compose up -d`
    - можно проверить что запустилось командой `docker-compose ps`
1. Откройте интерфейс [SPARQL по адресу](http://localhost:3030/)

Загрузить RDF-файл:
1. Перейти на [страницу загрузки данных в датасе](http://localhost:3030/#/dataset/ds/upload)
1. Нажмите `select file` и выберите файл для загрузки, например, [этот](https://github.com/kontur32/cccr-docker/blob/main/data/example/reestr-klassov-shkoli.rdf)
1. Нажмите `upload now`
1. Перейдите в [окно запросов](http://localhost:3030/#/dataset/ds/query) и запустите запрос (черный треугольник в правом верхнем углу окна запроса)
