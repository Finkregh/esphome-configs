Workflow:

- copy the yaml content into a new device `set-me-up` in your esphome
- build firmware, download
- rename `set-me-up` in esphome to `template-do-notuse`
- upload firmware to device
- connect to device AP, set wifi parameters
- device should show up as `set-me-up` in esphome, ready to be adapted (here it gets its correct name, etc)
