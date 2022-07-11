# Quick Overview

| Env                       | Example                  | Default                        | Description                                                                                                 |
| :------------------------ | :----------------------- | :----------------------------- | :---------------------------------------------------------------------------------------------------------- |
| TRAINS_PATH               | "./charts"               | "./charts"                     | Path where trains are stored                                                                                |
| IMAGE_PATH                | "./mirror"               | "./mirror"                     | Path where "mirror" is stored                                                                               |
| PORT_LIST_FILE            | "./default_port_list.md" | "./default_port_list.md"       | Name and path of the port list file                                                                         |
| VOLUME_LIST_FILE          | "./volume_list.md"       | "./volume_list.md"             | Name and path of the volume list file                                                                       |
| DESCRIPTION_LIST_FILE     | "./description_list.md"  | "./description_list.md"        | Name and path of the description list file                                                                  |
| EXCLUDE_TRAINS            | "dev,games"              | ""                             | List of excluded trains                                                                                     |
| EXCLUDE_TRAINS            | "traefik,nextcloud"      | ""                             | List of excluded apps                                                                                       |
| VERBOSE                   | "False"                  | "True"                         | Print Verbose Output                                                                                        |
| GENERATE_PORT_FILE        | "False"                  | "True"                         | Set to false to NOT generate a file                                                                         |
| GENERATE_VOLUME_FILE      | "False"                  | "True"                         | Set to false to NOT generate a file                                                                         |
| GENERATE_DESCRIPTION_FILE | "False"                  | "True"                         | Set to false to NOT generate a file                                                                         |
| PRINT_IMAGE_SOURCE        | "False"                  | "True"                         | Set to false to NOT print the image source                                                                  |
| SPLIT_DESCRIPTION_EVERY   | 70                       | 70                             | Split description into lines every n character.<br />If character is not " ", it will do on the nearest " " |
| FALLBACK_URL              | "https://truecharts.org" | "https://truecharts.org"       | URL to return if the URL we are trying to get does not exist (eg, links for `home:`)                        |
| SORT_VOLUMES_BY_STATUS    | "False"                  | "True"                         | Set to false to NOT generate a file                                                                         |
| TRAIN_ORDER_FOR_FILES     | "core,stable"            | "core,stable,dependency,games" | Order of trains which will appear in the files                                                              |

---

## Environment Variables in depth

### TRAIN_ORDER_FOR_FILES

This ordered will be used, any trains not listed here and not excluded will be added automatically to the end. Any trains added to this list but not existing in file system will be ignored.

### SORT_VOLUMES_BY_STATUS

Volumes make sense to order by app name, so each app has it's volumes one after the other. If we sort by status, (eg disabled etc), volumes will be all over the place

### Boolean envs

Anything other than `True`, `true` or `1` is considered `False`

#### How to run this

- Install `pipenv`
  - `pip install pipenv`
- Install dependencies
  - `pipenv install`
- Activate pipenv environment
  - `pipenv shell`
- Run it
  - `python app.py`
