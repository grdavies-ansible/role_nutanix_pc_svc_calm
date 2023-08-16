# Nutanix Role to manages the Calm service within Prism Central

This Ansible role manages the Calm service on Prism Central.


## Role Variables

| Variable                                          | Required | Default | Choices                   | Comments                                                                                               |
|---------------------------------------------------|----------|---------|---------------------------|--------------------------------------------------------------------------------------------------------|
| nutanix_host                                      | yes      |         |                           | The IP address or FQDN for the Prism Centra) where you want to enable the service.                     |
| nutanix_username                                  | no       | "admin" |                           | A valid username with appropriate rights to access the Nutanix API.                                    |
| nutanix_password                                  | yes      |         |                           | A valid password for the supplied username.                                                            |
| nutanix_port                                      | no       | 9440    |                           | The Prism TCP port                                                                                     |
| validate_certs                                    | no       | no      | yes / no                  | Whether to check if Prism UI certificates are valid.                                                   |
| nutanix_debug                                     | no       | no      | yes / no                  | Whether to output variable contents for debugging purposes.                                            |
| nutanix_calm_enable                               | yes      |         | yes / no                  | Set value to 'yes' to enable Calm.                                                                     |


## Dependencies

None


## Example Playbook

```
- hosts: localhost
  gather_facts: false
  roles:
    - role: grdavies.role_nutanix_pc_svc_calm
  vars:
    nutanix_host: 10.38.179.39
    nutanix_username: admin
    nutanix_password: nx2Tech283!
    nutanix_calm_enable: yes
```

## License

See LICENSE.md

## Author Information

Ross Davies
