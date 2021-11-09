# ansible-collection-test-usage
Example sync of a Collection from a Git repository.

## Requirements
Ansible version 2.10 or later.

## Usage
Source documentation [here](https://docs.ansible.com/ansible/latest/user_guide/collections_using.html#installing-a-collection-from-a-git-repository).

Use `ínstall-requirements.sh` to pull the latest version of the collection specified in `requirements.yml`.

Or manually:
```shell
# via ssh
ansible-galaxy collection install --collections-path ./collections git@github.com:aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test

# via https
ansible-galaxy collection install --collections-path ./collections git+https://github.com/aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test

# force an update (because usually the content of versions shouldn't change, but maybe you're just messing about)
ansible-galaxy collection install --collections-path ./collections git+https://github.com/aseriesofdarkcaves/ansible-collection-test.git#aseriesofdarkcaves/ansible_collection_test --force
```

You can then use the base path of this repo to define Playbooks which use the Roles/Collections you pulled in.
You just need to make sure that you have told Ansible where to find the extra Roles/Collections via `ansible.cfg`
