# Ansible swap role

An ansible role that creates a swap file and enables swapping.

The role includes the following tasks:
1. Create and configure an extra swap file with a specified size at `/extraswap`.
2. Add a corresponding line to the `fstab` file.
3. Run a `swapon` command to enable all swap areas.

## Requirements

None

## Role Variables

The only variable you need to specify is `swap_size`. By default, its value is 2048 MB (see `defaults/main.yml`):

```yaml
swap_size: 2048
```

## Dependencies

None

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: swap
```

To reduce the size of the swap file, change the value of the corresponding variable:

```yaml
swap_size: 1024
```

## License

Licensed under the [MIT License](https://opensource.org/licenses/MIT).
