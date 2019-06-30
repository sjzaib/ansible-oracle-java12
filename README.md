# ansible-oracle-java12
Sample playbook to install oracle java via ansible on ubuntu linux

## Usuage:
1. Open 'hosts' file and replace test.exmaple.com with dns name or ip address
of your target ubuntu box where you want to install oracle java 12 

2. Run it like this 
```ansible-playbook playbook.yml --extra-vars "--extra-vars "ansible_user=ubuntu ansible_password=<ssh-password-for-target>"```

## Sample Run

```
$ ansible-playbook playbook.yml --extra-vars "ansible_user=ubuntu ansible_password=mypassword"

PLAY [app] *************************************************************************************************************************************

TASK [Gathering Facts] *************************************************************************************************************************
ok: [192.168.10.12]

TASK [Install add-apt-repostory] ***************************************************************************************************************
changed: [192.168.10.12]

TASK [Add Oracle Java Repository] **************************************************************************************************************
changed: [192.168.10.12]

TASK [Accept Java 12 License] ******************************************************************************************************************
changed: [192.168.10.12]

TASK [Install Oracle Java 12] ******************************************************************************************************************
changed: [192.168.10.12] => (item=[u'oracle-java12-installer', u'ca-certificates', u'oracle-java12-set-default'])

PLAY RECAP *************************************************************************************************************************************
192.168.10.12                : ok=5    changed=4    unreachable=0    failed=0   
```
