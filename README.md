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
bin_path: "/opt/{{ software.name }}/bin"
conf_path: "/opt/{{ software.name }}/conf"
data_path: "/data/{{ software.name }}"
log_path: "/var/log/{{ software.name }}"
tmp_path: "/tmp/{{ software.name }}"

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

bin_file:

download_url:
```
