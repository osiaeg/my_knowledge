Исходный код можно найти [здесь](https://github.com/radxa-repo/bsp)
Официальная документация для сборки ядра *zero3w* [здесь](https://docs.radxa.com/en/zero/zero3/low-level-dev/kernel)

Пример сборки ядра:
```bash
bsp linux rk356x radxa-zero3 -r 999
```

### Radxa image builder
Исходный код можно найти [здесь](https://github.com/radxa-repo/rbuild)

Пример сборки образа с новым ядром
```bash
rbuild -k /path/to/kerner/linux-image.deb --compress radxa-zero3 cli
```
