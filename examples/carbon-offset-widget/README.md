# Carbon Offset Widget

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

| Parameter         | Description                                                                                                              | Example  |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------ | -------- |
| partnerId         | Required: The partner ID who has reserved carbon with DOVU for their customers                                           | SWIRLDS  |
| customerRef       | Required: An identifier for the customer buying the carbon offset                                                        | cust_123 |
| amount            | Optional: The amount of carbon in tonnes to offset. If set, the widget will not allow the user to edit the value         | 42       |
| placeholderAmount | Optional: The amount of carbon in tonnes to suggest offsetting. If set, the widget WILL allow the user to edit the value | 10       |

![Carbon Offset Widget](/examples/carbon-offset-widget/dovuCarbonOffsetWidget.png)
