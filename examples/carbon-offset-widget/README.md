# Carbon Offset Widget

An example of how to use the DOVU Carbon Offset Widget on any website can be found [here](/examples/carbon-offset-widget/carbonOffsetWidget.html).

The widget can be customised using the following parameters on the iFrame src url:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUST_REF>&amount=<AMOUNT>`

| Parameter         | Description                                                                                            | Example  |
| ----------------- | ------------------------------------------------------------------------------------------------------ | -------- |
| partnerId         | The partner ID who has reserved carbon with DOVU for their customers                                   | TYMLEZ   |
| customerRef       | An identifier for the customer buying the carbon offset                                                | cust_123 |
| amount            | The amount of carbon in tonnes to offset, if set the widget will not allow the user to edit the value  | 42       |
| placeholderAmount | The amount of carbon in tonnes to suggest offsetting, the widget WILL allow the user to edit the value | 10       |

![Carbon Offset Widget](/examples/carbon-offset-widget/dovuCarbonOffsetWidget.png)
