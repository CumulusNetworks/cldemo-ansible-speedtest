HOW TO TEST
===========

 * Install Ansible from Source

for i in {1..100}; do (time ansible-playbook run-commands.yml --extra-vars count=10 &> /dev/null) 2>&1 >/dev/null | grep real | cut -d "m" -f 2 | cut -d "s" -f 1 >> commands.csv; done
for i in {1..100}; do (time ansible-playbook run-nclu.yml --extra-vars count=10 &> /dev/null) 2>&1 >/dev/null | grep real | cut -d "m" -f 2 | cut -d "s" -f 1 >> nclu.csv; done
