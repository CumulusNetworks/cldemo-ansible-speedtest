# DEPRECATED
## This repo is no longer maintained.<br>For a list of current demos, please visit:<br>https://gitlab.com/cumulus-consulting/goldenturtle/<br><br><br>

HOW TO TEST
===========

 * Install Ansible from Source

for i in {1..100}; do (time ansible-playbook run-commands.yml --extra-vars count=$i &> /dev/null) 2>&1 >/dev/null | grep real | cut -d "m" -f 2 | cut -d "s" -f 1 >> commands.csv; done
for i in {1..100}; do (time ansible-playbook run-nclu.yml --extra-vars count=$i &> /dev/null) 2>&1 >/dev/null | grep real | cut -d "m" -f 2 | cut -d "s" -f 1 >> nclu.csv; done
