# Credit Purchase Widget

> For testing with DOVU you will be using the staging server or *https://staging.dovu.market/*

An example of how to use the DOVU Credit Purchase Widget on any website can be found [here](/examples/carbon-offset-widget/carbonOffsetWidget.html).

The widget can be embedded on any website using an iFrame. The iFrame src url should be:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>`

`PARTNER_ID` is required and is the ID of the partner who has reserved credits with DOVU for their customers.

`CUSTOMER_REF` is required and is your own internal identifier for the customer buying the credits.

## Customisation

The widget can be customised using the following parameters on the iFrame src url:

### Specify a set amount of credits to purchase

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&amount=<AMOUNT>`

![Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetAmount.png)

### Specify a suggested amount of credits to purchase that can be edited

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&placeholderAmount=<AMOUNT>`

![Placholder Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetPlaceholder.png)

### Pass no amount for the default behaviour

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>`

![No Amount](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetDefault.png)

### Purchase Types

DOVU supports selling credits at different stages of the credit life cycle.

As a Partner, if you have multiple projects available to purchase credits from and these projects span across differnet credit types then you can choose which projects are displayed by default when the user enters our site.

This can be enabled by adding the `purchaseType` parameter to the iFrame src url and setting it to `available`, `pre-order` or `verified`.

The default is `available`. Please see the below for more information on each purchase type.

#### Available

The credit has been certified and the credit has a full audit trail on Hedera mainnet. Once sold, the credit is instantly retired.

#### Pre-order

A project believes it has the data to support it issuing a credit in the future (once verification and certification has been completed)

#### Verified

A verifier has measured and verified the credits (this can include self-verification) but no certification body has certified the credit.

## Unit Types

The widget can be customised to show different unit types by adding the `unitType` parameter to the iFrame src url:

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&unitType=<UNIT_TYPE>`

The default is `carbon`. Please see the below for more information on each unit type.

#### Carbon

Will display `tonnes of CO2e` as the unit type.

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&unitType=carbon`

![Carbon](/examples/carbon-offset-widget/dovuCarbonOffsetWidget.png)

#### Biodiversity

Will display `hectares` as the unit type.
`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&unitType=biodiversity`

![Biodiversity](/examples/carbon-offset-widget/dovuBiodiversityWidgetAmount.png)

#### ELV

Will display `ELV Certificates of Deposit` as the unit type.

`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&unitType=elv`

![ELV](/examples/carbon-offset-widget/dovuElvWidgetAmount.png)

### Light and Dark Themes

The widget can be customised to use a light or dark theme by adding the `theme` parameter to the iFrame src url:
`https://dovu.market/partner/<PARTNER_ID>/embed?customerRef=<CUSTOMER_REF>&theme=<THEME>`

![Light Theme](/examples/carbon-offset-widget/dovuCarbonOffsetWidgetLight.png)

| Parameter           | Type        | Default   | Required | Description                                                                                                                               | Example      |
| ------------------- | ----------- | --------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| `partnerId`         | PATH        | n/a       | ✔️       | The partner ID who has reserved credits with DOVU for their customers                                                                     | SWIRLDS      |
| `customerRef`       | Query Param | n/a       | ✔️       | An identifier for the customer buying the credits                                                                                         | cust_123     |
| `amount`            | Query Param | -         |          | The amount of credits to purchase. If set, the widget will overide the `placeholderAmount` value and not allow the user to edit the value | 42           |
| `placeholderAmount` | Query Param | 1         |          | The amount of credits to suggest purchasing. If set, the widget WILL allow the user to edit the value                                     | 10           |
| `theme`             | Query Param | dark      |          | The theme of the widget. Can be either `light` or `dark`.                                                                                 | light        |
| `purchaseType`      | Query Param | available |          | The type of purchase. Can be either `available`, `pre-order` or `verified`.                                                               | pre-order    |
| `unitType`          | Query Param | carbon    |          | The credit unit being purchase. Can be either `carbon`, `biodiversity` or `elv`.                                                          | biodiversity |
