# ansible-plzimg

An ansible-role to manage a plzimg configuration

## Variables

| variable | default | description |
| -------- | ------- | ----------- |
| plzimg__python_dependencies | [flask,pillow] | Python packages that need to be installed (via pip) |
| plzimg__git_url | https://github.com/itbane/plzimg | git repo to pull the app from |
| plzimg__git_version | `master` | git version to pull |
| plzimg__deployment_dir | `/usr/local/lib` | Folder that plzimg should be deployed to |
| plzimg__data_dir | `{{ plzimg__deployment_dir }}/plzimg` | Folder the app lives in |

## Usage

~~~yaml
- name: deploy plzimg
  hosts: all
  roles:
    - plzimg
~~~
