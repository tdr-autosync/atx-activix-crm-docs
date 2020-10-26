# Custom Fields

Users of Activix CRM may create custom fields to fulfill their specific needs.

The representation of a custom field is called an `Custom Field` object.  
Custom fields are identified by a unique incremental ID.

Each `Lead` can have many `Custom Field` of different types.

## The `Custom Field` Object

| **Attribute** | **Type** | **Description** |
| :--- | :--- | :--- |
| `id` | integer | Unique identifier for the custom field. |
|  |  |  |
| `name` | string | Name of the custom field. |
| `type` | string | Indicate the type of custom field. Possible values are **array**, **boolean**, **currency**, **datetime** and **string**. |
| `value` | string | The value of the custom field. |

