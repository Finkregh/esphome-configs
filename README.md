Workflow:

- copy the yaml content into a new device `set-me-up` in your esphome
- build firmware, download
- rename `set-me-up` in esphome to `template-do-notuse`
- upload firmware to device
- connect to device AP, set wifi parameters
- device should show up as `set-me-up` in esphome, ready to be adapted (here it gets its correct name, etc)
- after that the config looks like this:
  ```
  substitutions:
    name: "nous-5"
    friendly_name: Küche Steckdose Friteuse
  packages:
    finkregh.Nous AT1: github://finkregh/esphome-configs/nous-at1.yaml@main
  esphome:
    name: ${name}
    name_add_mac_suffix: false
    friendly_name: ${friendly_name}
  ```
- you can now add your own config parts (e.g. API key) and finally rename it via the UI
- if you want to change variables, do so via the `substitutions:` parts at the top, reference the file here to see available variables
