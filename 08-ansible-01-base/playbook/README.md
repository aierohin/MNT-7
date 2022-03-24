# Самоконтроль выполненения задания

1. group_vars/all/examp.yml
2. ansible-playbook site.yml -i inventory/test.yml
3. ansible-vault encrypt group_vars/deb/examp.yml
4. ansible-vault decrypt group_vars/deb/examp.yml
5. Нет
6. ansible-playbook --ask-vault-password site.yml -i inventory/prod.yml
7. ansible_connection=winrm
8. ansible-doc -F | grep community.crypto
9. remote_user:

