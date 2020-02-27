---
id: drivers
title: Drivers Management
sidebar_label: Drivers
---


# Drivers Management

We will explore drivers management operations in this page. We will look at how can we create new driver account, approve drivers, and export them into excel file.



## Listing the drivers

To list the available drivers, go to side menu and select, Drivers >> Drivers

![Sidemenu drivers](assets/img/drivers/sidemenu-drivers.jpg)

You will be presented with drivers list page, from there you can perform various actions.

## Driver Commission

Commission is the amount that the drivers owe to Awini platform in exchange of receiving orders and utilize its services. 

The commission system works as follow.

When a driver registers in the application and his account has been approved by a dispatcher, the dispatcher will be asked to set driver *commission rate*, and *commission limit* for him. At initial point the driver *commission balance* will be at 0.

> **Note**: Check driver attribute bellow for more details on what commission rate, and commission limit are.



We will assume that the driver *commission rate*, and *commission limit* are set as follow:

- Commission rate: 20%
- Commission limit: 250 SAR



After the driver has been approved, the driver can start to receive orders on his mobile phone.

We will assume that the driver received an order with a total price of 200 SAR, and without any extra addons. When the driver accepts the order and complete it. A commission will be added to the driver *commission balance*, as follow:

Order total price is **200 SAR**

Driver *commission rate* is **20%**

Therefore, **20%** (driver *commission rate*) of **200 SAR** (order total price) equals **40 SAR**

And so, this **40 SAR** is added to the driver *commission balance*.



---

When the driver *commission balance* exceeds *commission limit*, his account will be suspended and he will no longer be able to receive orders. Until he clears his *commission balance* or part rof it.

## Creating New Driver

From the drivers listing page, click on **New** button from the above list actions. you will be presented with a form, fill out the required driver details. and submit it.

> **Note:** All required information of the driver must be filled out, in order to save the changes. The required fields are *(first name, last name, phone, national ID, password, and approval state)*

Please check the [driver attribute](#drivers-attributes) section, for more details.

## Drivers Approval 

In order for the drivers to receive orders, they must register from the mobile app, then their account must be reviewed by the dispatcher for approval.

To approve drivers account, follow the step:

1. Go to driver listing page, from the left side menu.
2. Then, use quick filter, to filter out the pending drivers account. Using this methods will give list of drivers that their *approval state* is pending and also they completed all registration steps.

![Pending filter](assets/img/drivers/quick-filter.jpg)

3. Then, go to "Pen icon" on the right side of the driver record that you want to approve.

![Pending filter](assets/img/drivers/pen-icon.jpg)

4. Then, review the driver account and that he satisfy the requirements. 
5. Go to Approval tab 

![approval tab](assets/img/drivers/approva-tab.jpg)

6. Fill out the approval form,

![approval form](assets/img/drivers/approval-form.jpg)

> **Note**: check Driver [Attributes section](#drivers-attributes) for more details

In case the driver did not meet the requirements, and you want to reject his account, you must provide *rejection reason* Then submit the form to save it.

In both the *Approval*, and *Rejection* cases, the driver will receive SMS message indicate his approval state.

Approval form can be updated later, and the driver *Approval State* can be changed as well. Each time the *Approval State* changes, the driver will receive SMS message notifying him of the new state.

After the approval, the driver can start to receive orders.



## Aerial View

In Aerial view page the dispatcher will be able to track drivers location real time.

Only approved drivers account, and opened their mobile app after the approval, are visible in **Aerial view**. 

> **Note**: Sometimes the drivers location are not updated, because some driver may have disabled the GPS system from the mobile app. you can check the last time his location have been updated from *last updated at* attribute

By dragging over the map it will refresh automatically to show more drivers.

![Aerial view](assets/img/drivers/aerial-view.jpg)

 to stop auto searching feature, check-in the ***Stop auto search***. then you can search manually by clicking on **Search** button. 

You also have the ability to filter out specific drivers, using the available filters. after applying a filter you must click on search button, or continue dragging the map to refresh it.

By clicking on  a driver from the right panel, the map will point you in into his location on open small window in the map. 

## Drivers Attributes

### Driver specific attributes

Attributes that are related to the drivers.

|    Attribute     |                         Description                          |
| :--------------: | :----------------------------------------------------------: |
|    First name    |                      driver first name                       |
|    Last name     |                       driver last name                       |
|      Phone       | drivers phone number, must start with country prefix ex. 966, 971 |
|   National ID    |        driver national Id, usually consists 10 digits        |
|     Password     |   driver password in order to register into the mobile app   |
|      Email       |               optional, used in sending emails               |
|     Service      |     The driver will only receive orders of this service      |
|     Company      | Which company this driver belongs to. The company will have the ability to change driver data |
|       IBAN       |             *International Bank Account Number*              |
|   With Labors    |         driver can provide labors for load & unload          |
| Can accept trips | Has three values, **Always**: can accept orders even if he has one going, **Only one**: can accept one order at a time, **Never**: can only take order that is assigned to him by a dispatcher |
|      Status      | Has three values, **Active**, and **inactive** if driver account is inactive than he can not login into his account, nor he can accept orders |
|   Black listed   |   Will have the same affect as the ***status*** attribute    |
|  Approval state  | Has three values, **Approved**, **Rejected**, and **pending**. Once the driver register through the mobile app his approval status will be pending |
| Rejection reason | If the driver is rejected, the dispatcher will provide the rejection reason |
|  Registered At   |                    The registration date                     |
| Last updated at  |           Last date the driver location is updated           |
|      Wallet      | How much the Awini owe to the driver. The driver can receive in his wallet in different ways |
|    Commission    | How much the driver owes to Awini. This field is increased by completing orders |
| Commission limit | How much the driver *commission* can be reached before his account is suspended |
| Commission rate  | How much commission the driver will pays for each order he completes |
|       Step       | The driver has three steps to register from the mobile application |
|  Fixed location  | Whether the has a fixed location, which will not be updated from driver mobile app. And only the dispatcher can update it |
|     Location     | This attribute is mandatory only if **Fixed location** is active. It will determine the driver fixed location |

### Vehicle specific attributes

Attriubte that are specific to the driver

| Attribute                  | Description                              |
| -------------------------- | ---------------------------------------- |
| Name                       | Name the driver provided for his vehicle |
| Model                      | Manufacture brand name                   |
| Number                     | Plate numbers                            |
| Plate character            | Plate characters                         |
| Year                       | Year of manufacture                      |
| Photo                      | Front photo of the vehicle               |
| Back photo                 | Back photo of the vehicle                |
| Vehicle registration photo | Governmental vehicle registration photo  |
| Insurance photo            | Vehicle Insurance photo                  |

