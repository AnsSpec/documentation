# Ansible Specifications

## Roles

### Skeleton

```shell
/defaults/main.yml
/tasks/main.yml
```

### Role ansspec.base

`ansspec/defaults/main.yml`:

```yaml
dir_bin: "/opt/{{ software.name }}/bin"
dir_conf: "/opt/{{ software.name }}/conf"
dir_data: "/data/{{ software.name }}"
dir_log: "/var/log/{{ software.name }}"
dir_tmp: "/tmp/{{ software.name }}"

username: "{{ software.name }}"
groupname: "{{ software.name }}"
servicename: "{{ software.name }}"
```

### Role ansspec.{software}

`ansspec.<software>/vars/main.yml`:

```yaml
software:
  name: <software>
  version: <software_version>
```

## Variables

```yaml
software:
  name:
  version:

file_bin:

url_download:
```
