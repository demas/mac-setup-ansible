# Mac Development Ansible Playbook

This playbook installs and configures most of the software I use on my Mac for software development.

## Installation

1. Ensure Apple's command line tools are installed (`xcode-select --install`).
2. Install Ansible: 


``` python
python --version # 2.7
sudo easy_install pip
sudo pip install ansible
```

3. Run `ansible-galaxy install -r requirements.yml` to install Ansible roles.
4. Run `ansible-playbook main.yml -i inventory -K`.

### Running a specific set of tagged tasks

``` shell
ansible-playbook main.yml -i inventory --tags "dotfiles,homebrew"
```
