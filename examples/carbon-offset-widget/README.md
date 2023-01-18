# Carbon Offset Widget

> For testing with DOVU you will be using the staging server or *https://staging.dovu.market/*

An example of how to use the DOVU Carbon Offset Widget on any website can be found [here](/examples/carbon-offset-widget/carbonOffsetWidget.html).

The widget can be customised using the following parameters on the iFrame src url:

### Specify a set amount of carbon to offset

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>&amount=<AMOUNT>`

![Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetAmount.png)

### Specify a suggested amount of carbon to offset that can be edited

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>&placeholderAmount=<AMOUNT>`

![Placholder Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetPlaceholder.png)

### Pass no amount for the default behaviour

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>`

![No Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetDefault.png)

### Light and Dark Themes

The widget can be customised to use a light or dark theme by adding the `theme` parameter to the iFrame src url:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>&theme=<THEME>`

| Parameter         | Type        | Description                                                                                                              | Example  |
| ----------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------ | -------- |
| partnerId         | PATH        | Required: The partner ID who has reserved carbon with DOVU for their customers                                           | SWIRLDS  |
| customerRef       | Query Param | Required: An identifier for the customer buying the carbon offset                                                        | cust_123 |
| amount            | Query Param | Optional: The amount of carbon in tonnes to offset. If set, the widget will not allow the user to edit the value         | 42       |
| placeholderAmount | Query Param | Optional: The amount of carbon in tonnes to suggest offsetting. If set, the widget WILL allow the user to edit the value | 10       |
| theme             | Query Param | Optional: The theme of the widget. Can be either `light` or `dark`. It will default to `dark`.                           | light    |
