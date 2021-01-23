# OpenDKIM

[![Build Status](https://drone.osshelp.ru/api/badges/ansible/opendkim/status.svg)](https://drone.osshelp.ru/ansible/opendkim)

The role installs and setups OpenDKIM (plus key generation).

## Usage (example)

See [playbook.yml](molecule/default/playbook.yml).

## Available parameters

### Main

| Param | Default | Description |
| -------- | -------- | -------- |
| `opendkim_setup` | `full` | Setup mode. See [OSSHelp KB article](https://oss.help/kb4895) |
| `opendkim_keys`| `[]`| Opendkim keys list |
| `opendkim_trustedhosts`| `[]`| Opendkim trusted hosts |

### Key parameters

| Param | Default | Description |
| -------- | -------- | -------- |
| `name` | - | Key name |
| `size` | `2048` | Key size. Used if `key` is not defined |
| `selector` | `default` | Selector |
| `key` | - | Private RSA key |
| `sign_email_from_domain` | - | Domains for which email will be sign |

### Misc

See [defaults](defaults/main.yml).

## FAQ

...

## Useful links

- [Official documentation](http://opendkim.org/)
- [OSSHelp KB article](https://oss.help/kb575)

## TODO

- show pub files in log (needed?)

## License

GPL3

## Author

OSSHelp Team, see <https://oss.help>
