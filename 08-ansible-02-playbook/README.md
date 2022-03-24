# Домашнее задание к занятию "08.02 Работа с Playbook"

## Основная часть
<<<<<<< HEAD
1 - https://github.com/aierohin/MNT-7/blob/master/08-ansible-02-playbook/playbook/inventory/prod.yml  
2, 3, 4 - https://github.com/aierohin/MNT-7/blob/master/08-ansible-02-playbook/playbook/site.yml  
5 - Ошибок нет.  
6 - ```ansible-playbook -i inventory/prod.yml site.yml -kK --check```  
7 - ```ansible-playbook -i inventory/prod.yml site.yml -kK --diff```  
8 - Идемпотентен.  
9 - https://github.com/aierohin/MNT-7/blob/master/08-ansible-02-playbook/playbook/README.md  
10 - https://github.com/aierohin/MNT-7/tree/master/08-ansible-02-playbook/playbook  
=======
1. Приготовьте свой собственный inventory файл `prod.yml`.
2. Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает kibana.
3. При создании tasks рекомендую использовать модули: `get_url`, `template`, `unarchive`, `file`.
4. Tasks должны: скачать нужной версии дистрибутив, выполнить распаковку в выбранную директорию, сгенерировать конфигурацию с параметрами.
5. Запустите `ansible-lint site.yml` и исправьте ошибки, если они есть.
6. Попробуйте запустить playbook на этом окружении с флагом `--check`.
7. Запустите playbook на `prod.yml` окружении с флагом `--diff`. Убедитесь, что изменения на системе произведены.
8. Повторно запустите playbook с флагом `--diff` и убедитесь, что playbook идемпотентен.
9. Подготовьте README.md файл по своему playbook. В нём должно быть описано: что делает playbook, какие у него есть параметры и теги.
10. Готовый playbook выложите в свой репозиторий, в ответ предоставьте ссылку на него.

---

### Как оформить ДЗ?

Выполненное домашнее задание пришлите ссылкой на .md-файл в вашем репозитории.

---
>>>>>>> db9e425c9807133245fc3ce70c96d05af0db650d
