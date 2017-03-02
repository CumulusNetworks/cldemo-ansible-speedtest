HOW TO TEST
===========

 * Install Ansible from Source
 * pick a test, such as run-commands.yml
 * run the following three commands:
    * ansible-playbook run-cleanup.yml
    * time ansible-playbook run-commands.yml
    * time ansible-playbook run-commands.yml
 * the first time you run the command, you see how long it takes to change
   the switch.
 * the second time, you see how long it takes when there are no changes
   required
