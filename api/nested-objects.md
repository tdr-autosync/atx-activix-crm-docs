# Nested Objects

Many resources have nested objects that can be returned with the results. For example a `Lead` may have an associated `Advisor`. Those objects can be included using the `include` request parameter.

You can include multiple nested objects at once by identifying multiple items in the `include` array.

#### Usage Example

In the following example, the nested emails and phones objects will be included in the resulted leads.

```text
/leads?include[]=emails&include[]=phones
```

