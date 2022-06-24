# Product

The representation of a product is called a `Product` object.

## The `Product` Object

| Attribute    | Type    | Description                                                                                                                                                          |
| ------------ | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `created_at` | string  | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the product was created.                                                                   |
| `updated_at` | string  | [ISO datetime](https://en.wikipedia.org/wiki/ISO\_8601) representing when the product was last updated.                                                              |
|              |         |                                                                                                                                                                      |
| `category`   | string  | The category of the product.                                                                                                                                         |
| `minutes`    | integer | <p>Time representing the work duration.</p><p><em>For <strong>service</strong> products only.</em></p>                                                               |
| `name`       | string  | Name of the product.                                                                                                                                                 |
| `notes`      | string  | Notes.                                                                                                                                                               |
| `premium`    | boolean | Determine if it is a premium product.                                                                                                                                |
| `price`      | numeric | Price of the product.                                                                                                                                                |
| `sold`       | boolean | Determine if the product is sold.                                                                                                                                    |
| `type`       | string  | <p>The type of product. Possible values are <strong>commercial</strong> or <strong>service</strong>.<br></p><p><em>New values might be added in the future.</em></p> |

### List of available products

| ID | Name                                | Type        | Label                              |
| -- | ----------------------------------- | ----------- | ---------------------------------- |
| 1  | ins\_filling                        | commercial  | Replacement ins.                   |
| 2  | ins\_rental                         | commercial  | Leasing insurance                  |
| 3  | ins\_invalidity                     | commercial  | Invalidity insurance               |
| 4  | ins\_health                         | commercial  | Health insurance                   |
| 5  | ins\_life                           | commercial  | Life insurance                     |
| 6  | extended\_warranty                  | commercial  | Extended warranty                  |
| 7  | rustproofing                        | commercial  | Rustproofing                       |
| 8  | chiselling                          | commercial  | Chiselling                         |
| 9  | anti\_theft                         | commercial  | Anti theft                         |
| 10 | starter                             | commercial  | Remote starter                     |
| 11 | window\_tint                        | commercial  | Window tint                        |
| 12 | pre\_paid\_maintenance              | commercial  | PPM                                |
| 13 | seat\_protection                    | commercial  | Seat protection                    |
| 14 | financing                           | commercial  | Financing                          |
| 15 | pef                                 | commercial  | PEF                                |
| 16 | pep                                 | commercial  | PEP                                |
| 17 | other                               | commercial  | Other                              |
| 18 | pellicule                           | commercial  | 3M pellicule                       |
| 19 | windshield\_treatment               | commercial  | Windshield treatment               |
| 20 | paint\_treatment                    | commercial  | Paint treatment                    |
| 21 | roof\_treatment                     | commercial  | Roof treatment                     |
| 22 | leather\_tissu\_interior\_treatment | commercial  | Leather & cloth interior treatment |
| 23 | wheel\_protection                   | commercial  | Wheel protection                   |
| 24 | mouse\_repellent                    | commercial  | Mouse repellent                    |
| 25 | burn\_protection                    | commercial  | Burn protection                    |
| 26 | flame\_quard\_protection            | commercial  | Flame Guard protection             |
| 27 | maintenance\_a                      | service     | Maint. A                           |
| 28 | maintenance\_b                      | service     | Maint. B                           |
| 29 | maintenance\_c                      | service     | Maint. C                           |
| 30 | maintenance\_d                      | service     | Maint. D                           |
| 31 | maintenance\_recommended            | service     | Maint. Recomm.                     |
| 32 | diagnostic                          | service     | Diagnost.                          |
| 33 | air\_filter                         | service     | Air Filter                         |
| 34 | pollen\_filter                      | service     | Pollen Filter                      |
| 35 | alignment                           | service     | Align.                             |
| 36 | brakes                              | service     | Brakes                             |
| 37 | injection                           | service     | Injection                          |
| 38 | transmission                        | service     | Transmiss.                         |
| 39 | wash                                | service     | Wash                               |
| 40 | tires                               | service     | Tires                              |
| 41 | parts                               | service     | Parts                              |
| 42 | body                                | service     | Body                               |
| 43 | oil\_filter                         | service     | Oil & Filter                       |
| 44 | others                              | service     | Others                             |
| 60 | niotext                             | commercial  | NioText                            |
| 61 | walk\_in                            | commercial  | Walk-in                            |
| 62 | sale\_table                         | commercial  | Sales                              |
| 63 | in\_turn                            | commercial  | Next up                            |
| 64 | renewal                             | commercial  | renewal                            |
| 65 | event                               | commercial  | Event                              |
| 66 | service                             | commercial  | Service                            |
