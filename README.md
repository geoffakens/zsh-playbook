# Ansible playbook to install/configure oh-my-zsh

NOTE:  This is only tested and known to work on MacOS.  Additionally, the oh-my-zsh theme installed by this playbook is best with additional fonts that are not installed by the playbook.  If you're using iTerm2, the theme will prompt to download the fonts when you launch the terminal.

Prerequisites:

* Ansible
* Homebrew (on MacOS)

First, install the required roles:

```bash
ansible-galaxy install -r requirements.yml 
```

Optionally, you can override the default oh-my-zsh plugins installed by adding a `config.yml` file and defining a `plugins` variable.  See `default.config.yml` for the default plugins.

The playbook will run on the local machine by default.  This can be changed by editing `inventory`.

Finally, run the playbook:

```bash
ansible-playbook main.yml --ask-become-pass
```