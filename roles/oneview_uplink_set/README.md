## oneview_uplink_set
Manage OneView Uplink Set Network resources.

#### Synopsis
 Provides an interface to manage Uplink Set Network resources. Can create, update, and delete.

#### Requirements (on the host that executes the module)
  * hpeOneView >= 5.4.0

#### Options

| Parameter     | Required    | Default  | Choices    | Comments |
| ------------- |-------------| ---------|----------- |--------- |
| config  |   No  |  | |  Path to a .json configuration file containing the OneView client configuration. The configuration file is optional. If the file path is not provided, the configuration will be loaded from environment variables.  |
| data  |   Yes  |  | |  List with the Uplink Set Network properties.  |
| state  |   |  | <ul> <li>present</li>  <li>absent</li> </ul> |  Indicates the desired state for the Fibre Channel Network resource. `present` will ensure data properties are compliant with OneView. `absent` will remove the resource from OneView, if it exists.  |
| validate_etag  |   |  True  | <ul> <li>true</li>  <li>false</li> </ul> |  When the ETag Validation is enabled, the request will be conditionally processed only if the current ETag for the resource matches the ETag provided in the data.  |

## Example Playbook

```yaml
- hosts: all
  collections:
    - hpe.oneview
  roles:
    - hpe.oneview.oneview_uplink_set
```

## License

Apache

#### Return Values

| Name          | Description  | Returned | Type       |
| ------------- |-------------| ---------|----------- |
| uplink_set   | Has the facts about the managed OneView Uplink Set Network. |  On state 'present'. Can be null. |  dict |
