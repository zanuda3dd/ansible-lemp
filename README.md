# PetrovAP_LEMP

# Установить роли
ansible-galaxy install geerlingguy.nginx
ansible-galaxy install geerlingguy.php
ansible-galaxy install geerlingguy.mysql


# Запуск плейбука
ansible-playbook -i inventory.yaml playbook.yml  -e "@.vault" --ask-become-pass --ask-vault-pass
или
ansible-playbook -i inventory.yaml playbook.yml  -e "@.vault" --ask-become-pass --vault-password-file .vault_pass.txt
