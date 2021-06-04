# ansible-collection-test-usage
Example for how to sync a collection from a Git repository.
## Requirements
Ansible version 2.10 or later.

## Usage
See `ansible.cfg` for specifying the collection installation target. 

Source documentation [here](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html#installing-a-collection-from-a-git-repository).
```
# via ssh
ansible-galaxy collection install git@github.com:aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test

# via https
ansible-galaxy collection install git+https://github.com/aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test

# force an update (because usually the content of versions shouldn't change, but maybe you're just messing about)
ansible-galaxy collection install git+https://github.com/aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test --force
```
