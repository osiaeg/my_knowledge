## Создание виртуального окружения python
python3 -m venv env
. env/bin/activate

## Установка python-пакет с помощью pip из исходной дериктории
pip install .

## Установка python-пакета build для сборки tarball из проекта
pip install build
python -m build

## Проверка содержимого tarball после сборки
tar tvf dist/pion-0.0.1.tar.gz

## Установка модуля для сборки deb-пакета
pip install stdeb 

## Сборка deb-пакета из tarball
cd dist; py2dsc-deb pion-0.0.1.tar.gz; cd ..

## Установка прошла успешно
