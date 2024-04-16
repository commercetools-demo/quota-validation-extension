# Quota validation extension
Service that validates cart quotas.
This service should be set up as an API Extension in order to apply the rules configured on the Quota Manager APP:
https://github.com/commercetools-demo/quota-manager


## Extension setup:

Set the extension with the triggers on Cart as resourceTypeId and update on the actions array, like the following example:
**Important** after your service deployment address, use the endpoint **/validate-cart**

```
{
    "destination": {
        "type": "HTTP",
        "url": "https://quota-validation-extension-felipe-test-quota-vikeh6xrjq-ew.a.run.app/validate-cart"
    },
    "triggers": [
    {
      "resourceTypeId": "cart",
      "actions": ["Update"]
    }
  ]
}
```
