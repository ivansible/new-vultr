# ivansible.new_vultr

This role creates a new Vultr box


## Requirements

None


## Variables

Available variables are listed below, along with default values.

    vultr_name: vultr1
Host name for new server.

    vultr_os: xenial
OS to install: `xenial` or `bionic`

    vultr_plan: 5
Plan: `$5` or `$10` or full name of the plan

    vultr_region: ams
Region: `ams` for `Amsterdam`, `ny` for `New York` or full region name.

    vultr_inventory: yes
Can be `yes` or `no` or full inventory host name.

    vultr_ssh_port: 22
SSH port

    vultr_username: ubuntu
Username for login

    vultr_uid
Desired `id` for new user

    vultr_ssh_key_file: ""
Path to the private SSH key file. Public key will be registered with Vultr.

    vultr_ssh_key_name: derived from `ssh_key_file`
Name for this SSH key to register with Vultr.


## Tags

- `vr_facts`
- `vr_ini`
- `vr_ssh_key`
- `vr_script`
- `vr_server`
- `vr_inven`
- `vr_info`


## Dependencies

None


## Example Playbook

    - hosts: localhost  # the host is controller
      roles:
         - role: ivansible.new_vultr
           vultr_name=vultr1
           vultr_os=xenial
           vultr_plan=5
           vultr_region=ams
           vultr_inventory=yes


## Testing

    ./scripts/vultr.sh list|ls plans|regions
    ./scripts/vultr.sh new <name> [-os xenial|bionic] [-plan 5|10] [-region ams|ny] [-inven yes|no|<name>] [options...]

## License

MIT

## Author Information

Created in 2018 by [IvanSible](https://github.com/ivansible)
