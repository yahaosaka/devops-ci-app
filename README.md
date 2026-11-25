# devops-ci-app

Практическая работа № 10. Цепочка проверок lint → test → image.
Для Pull Request образ собирается и проверяется. Публикация в
ghcr.io/yahaosaka/devops-ci-app выполняется после push в main.

    python -m pip install -r app/requirements.txt -r requirements-dev.txt
    python -m pylint app --score=no
    python -m pytest -q

В GitHub создайте правило protect-main с обязательными проверками
lint, test и image. Для загрузки учебного образа без токена откройте
чтение пакета GHCR. Развёртывание привязывается к полному SHA коммита.
