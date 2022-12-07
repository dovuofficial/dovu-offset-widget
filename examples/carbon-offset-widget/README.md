# Carbon Offset Widget

An example of how to use the DOVU Carbon Offset Widget on any website can be found [here](/examples/carbon-offset-widget/carbonOffsetWidget.html).

The widget can be customised using the following parameters on the iFrame src url:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>&amount=<AMOUNT>`

| Parameter         | Description                                                                                                              | Example  |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------ | -------- |
| partnerId         | Required: The partner ID who has reserved carbon with DOVU for their customers                                           | TYMLEZ   |
| customerRef       | Required: An identifier for the customer buying the carbon offset                                                        | cust_123 |
| amount            | Optional: The amount of carbon in tonnes to offset. If set, the widget will not allow the user to edit the value         | 42       |
| placeholderAmount | Optional: The amount of carbon in tonnes to suggest offsetting. If set, the widget WILL allow the user to edit the value | 10       |

![Carbon Offset Widget](/examples/carbon-offset-widget/dovuCarbonOffsetWidget.png)
