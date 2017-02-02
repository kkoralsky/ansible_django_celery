Django celery worker
====================

Requirements
------------

Debian OS, queue broker and result store backends installed on current or other
machine: either:
- Redis or,
- AMQP or,
- Mongodb


Role Variables
--------------

- `app` - app label
- `program_name` - name for supervisor entry: defaults to `{{ app }}`
- `threads` - 
- `priority` - 
- `app_path`  - path to application,
- `venv_path` - path to virtual environment inside which run worker
- `django_settings_module` - /dotted/ python module path

Dependencies
------------

- https://github.com/ansible_django_supervisor

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: django_celery, app: my_app }

License
-------

BSD
