# cccr-docker
docker compose для CCCR

Что необходимо:
1. доступ к терминалу (на винде 10 WSL/Ubuntu)
1. установленный docker

Как запустить:
1. Запустите докер и войдите в терминал
1. Клонируте репоизиторий и перейдите в папку `cccr-docker/docker/`
1. Запустите сборку образов командой `docker-compose build`
1. Запишите путь к [папке с данными](https://github.com/kontur32/cccr-docker/tree/main/data) (он потребуется в следующем пункте)
1. Запустите контейнеры командой `DATA_DIR=полный_путь_к_паке_с_данными docker-compose up -d`
    - можно проверить что запустилось командой `docker-compose ps`
1. Откройте интерфейс [SPARQL по адресу](http://localhost:3030/)
