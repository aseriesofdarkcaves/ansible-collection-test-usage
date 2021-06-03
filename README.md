# ansible-collection-test-usage
Tried to follow [these](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html#installing-a-collection-from-a-git-repository)
instructions, but can't seem to get it to work...

Turns out I was on Ansible 2.9 and support for this only came in 2.10...
```
ansible-galaxy collection install git@github.com:aseriesofdarkcaves/ansible-collection-test.git
```
