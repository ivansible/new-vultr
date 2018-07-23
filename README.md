# ivansible.new-vultr
This role creates a new Vultr box


## Requirements

None


## Variables

Available variables are listed below, along with default values.

    variable1: 1
    variable2: 2

## Tags

- `role1_tag1` -- action1
- `role1_tag2` -- action2


## Dependencies

None


## Example Playbook

    - hosts: vagrant-boxes
      strategy: linear
      roles:
         - role: ivansible.new-vultr
           variable1: 1
           variable2: 2


## License

MIT

## Author Information

Created in 2018 by [IvanSible](https://github.com/ivansible)
