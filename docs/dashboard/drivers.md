---
id: drivers
title: Drivers Management
sidebar_label: Drivers Management
---


# Drivers Management

We will explore drivers management features in this page. We will look at drivers creating process, approval, and exporting them into excel file.



## Listing the drivers

Go to drivers page from the side menu

Drivers >> Drivers

<img src="/img/drivers/sidemenu-drivers.jpg" style="zoom:67%;" />

## Driver Commission

The commission system works as follow.

When a driver register in the application and his account has been approved by a dispatcher, the dispatcher set a *commission rate*, and *commission limit* for this drivers. And as initial his *commission balance* is 0.

> **Note**: Check driver attribute bellow for more details on what commission rate, and limit means



Let us assume driver commission rate, and limit as follow:

- Commission rate: 20%
- Commission limit: 250 SAR



After the driver has been approved he can receive customer orders. We will assume the total order price is 200 SAR. Now when the driver accept the order and completes it. A commission will be added to his *commission balance* 

Order total price is 200 SAR

Driver commission rate is 20

So, 20% of 200 SAR equals 40 SAR

So 40 SAR is added into the driver commission balance.

---

When the driver *commission balance* exceeds *commission limit*, his account will be suspended and he will not be able to receive order. Until he clears his commission or part of it.

## Creating New Driver

Got to drivers listing page, then click on **New** button from the above

Then fill out the driver details.

> **Note:** All required information of the driver must be filled in order to save the changes. which are *(first name, last name, phone, national ID, password, and approval state)*



Please check the driver attribute details from 



## Drivers Approval 

For drivers approval.

First go into driver listing page, from the side menu.

Then use quick filter, to filter out only the pending account. Using this methods will give list of drivers that their *approval state* is pending and also they completed all 3 registration steps.

![Pending filter](/img/drivers/quick-filter.jpg)

Now go to "Pen icon" on the right side of the driver details

![Pending filter](/img/drivers/pen-icon.jpg)


Then, after verifying his account details,  go to Approval tab 

<img src="/img/drivers/approva-tab.jpg" style="zoom:67%;" />

Fill out the form,

<img src="/img/drivers/approval-form.jpg" style="zoom:67%;" />



> **Note**: Please check Driver Attributes section for more details

In case you want to reject driver registration, you must provide *rejection reason*. Then, submit the form to save it.

The driver will receive SMS message indicate his approval state, for both *Approval*, and *Rejection*.

This form can be updated later, and the driver *Approval State* can be changed as well. Each time the driver *Approval State* changes he will receive SMS message notifying him.



## Aerial View

From Aerial view page the dispatcher can track drivers location real time.  By dragging over the map it will refresh automatically to show more drivers.

<img src="/img/drivers/aerial-view.jpg" style="zoom:67%;" />

 to suspend auto searching, check-in the ***Stop auto search***. then you can search manually by clicking on **Search** button. 

You also have the ability to filter out specific drivers, using the available filters. after applying a filter you must click on search button, or continue dragging the map to refresh it.

By clicking on  a driver from the right panel, the map will point you in into his location on open small window in the map. 

## Drivers Attributes

### Driver specific attributes

Attributes that are related to the drivers, 

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

### 

