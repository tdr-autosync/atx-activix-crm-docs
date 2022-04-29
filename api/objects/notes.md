# Notes

The representation of a note on a lead is called a Note object.

## The `Notes` Object

| Attribute    | Type    | Description                                                                                                   |
| ------------ | ------- | ------------------------------------------------------------------------------------------------------------- |
| `id`         | integer | Unique identifier for the note.                                                                               |
| `parent_id`  | integer | Unique identifier for the note that is being replied to.                                                      |
| `lead_id`    | integer | ID of the lead associated with the note.                                                                      |
| `user_id`    | integer | ID of the user who wrote the note.                                                                            |
|              |         |                                                                                                               |
| `created_at` | string  | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the note was created.               |
| `updated_at` | string  | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the note was updated.               |
|              |         |                                                                                                               |
| `content`    | string  | <p>The content of the note.<br><br><em>Required when there is no <code>file_url</code> provided.</em></p>     |
| `file_url`   | string  | <p>The URL of the attached file.<br><br><em>Required when there is no <code>content</code> provided.</em></p> |
