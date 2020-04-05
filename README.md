# Ansible template vars issue

Goal of this playbook is showing the diffrent behaviour in Ansible running on different operating systems:

* Ansible on CentOS 7.7 (Python 2.7)
* Ansible on CentOS 8.1 (Python 3.6)

The problem occurs by using a `set` followed by an `include` in Jinja2 templates.
On CentOS 8 it is required that all variables in scope can be resolved, even if these variables a not used within the template.
On CentOS 7 this was no issue.


## Run

1. Clone this repo
2. Go to the repo directory
3. Execute: `ansible-playbook playbook.yml`
