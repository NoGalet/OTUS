Задание: Vagrant-стенд для обновления ядра и создания образа системы
Выполнение:
1) Создать Vagrantfile (во вложении)
2) Создать ВМ: vagrant up
3) Поключиться к ВМ: vagrant ssh
4) Проверить текущую версию ядра: uname -r (Ядро_До.PNG)
5) Установка последнего ядра из репозитория elrepo-kernel (Kernel_Upd_N.PNG):
sudo yum --enablerepo elrepo-kernel install kernel-ml -y
6) Обновить конфигурацию загрузчика(grub2_config.PNG):
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
7) Выбрать загрузку нового ядра по-умолчанию:
sudo grub2-set-default 0
8) Проверить версию ядра: uname -r (Ядро_После.PNG)
