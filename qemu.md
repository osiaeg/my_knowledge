### QEMU и chroot

Для того, чтобы была возможно редактирования образа для
архитектуры отличной от хоста, необходимо запустить 
эмулятор *qemu*. Его можно установить следующим образом:
```bash
# Для Linux основанных на Debian
sudo apt install -y git qemu-user-static
```

#### Монтирование образов

Примонтировать образ формата **.img** можно, записав его на
flash носитель, после чего примонтировать небходимые разделы
в систему. Также можно воспользоваться программой *losetup* [man losetup](https://man7.org/linux/man-pages/man8/losetup.8.html)
# TODO: добавить больше информации про *losetup*

Для выполнения команды *chroot* потребуется скопировать скрипт
с именем *qemu-(architercher)-static*, где *architercher* - это
название архитекртуры для примонтированного образа 
(например *qemu-aarch64-static* для arm-процессоров).
```bash
cp $(which qemu-aarch64-static) /path/to/mnt/rootfs/usr/bin
```

После чего можно выполнить комнаду *chroot*:
```bash
sudo chroot /mnt/radxaimg/rootfs/ qemu-aarch64-static /bin/bash
```
