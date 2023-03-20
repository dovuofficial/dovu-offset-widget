# Carbon Offset Widget

> For testing with DOVU you will be using the staging server or *https://staging.dovu.market/*

An example of how to use the DOVU Carbon Offset Widget on any website can be found [here](/examples/carbon-offset-widget/carbonOffsetWidget.html).

The widget can be embedded on any website using an iFrame. The iFrame src url should be:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>`

`PARTNER_ID` is required and is the ID of the partner who has reserved carbon with DOVU for their customers.

`CUSTOMER_REF` is required and is your own internal identifier for the customer buying the carbon offset.

## Customisation

The widget can be customised using the following parameters on the iFrame src url:

### Specify a set amount of carbon to offset

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&amount=<AMOUNT>`

![Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetAmount.png)

### Specify a suggested amount of carbon to offset that can be edited

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&placeholderAmount=<AMOUNT>`

![Placholder Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetPlaceholder.png)

### Pass no amount for the default behaviour

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>`

![No Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetDefault.png)

### Light and Dark Themes

The widget can be customised to use a light or dark theme by adding the `theme` parameter to the iFrame src url:

### Pre-order

DOVU supports pre-ordering carbon offsets. This can be enabled by adding the `purchaseType` parameter to the iFrame src url and setting it to `pre-order`. This will automatically filter the list of carbon projects on the DOVU site to only show those that are available for pre-order.

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&theme=<THEME>`

![Light Theme](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetLight.png)

| Parameter           | Type        | Default   | Required | Description                                                                                                                                      | Example   |
| ------------------- | ----------- | --------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | --------- |
| `partnerId`         | PATH        | n/a       | ✔️       | The partner ID who has reserved carbon with DOVU for their customers                                                                             | SWIRLDS   |
| `customerRef`       | Query Param | n/a       | ✔️       | An identifier for the customer buying the carbon offset                                                                                          | cust_123  |
| `amount`            | Query Param | -         |          | The amount of carbon in tonnes to offset. If set, the widget will overide the `placeholderAmount` value and not allow the user to edit the value | 42        |
| `placeholderAmount` | Query Param | 1         |          | The amount of carbon in tonnes to suggest offsetting. If set, the widget WILL allow the user to edit the value                                   | 10        |
| `theme`             | Query Param | dark      |          | The theme of the widget. Can be either `light` or `dark`.                                                                                        | light     |
| `purchaseType`      | Query Param | available |          | The type of purchase. Can be either `available` or `pre-order`.                                                                                  | pre-order |
