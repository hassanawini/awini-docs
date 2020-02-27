---
id: trips
title: trips
---

# Trips

Trips are created by customers and carried out by drivers or service providers, each trip that the user creates is attached with one type of the available services. Most trips have two location, pickup location and drop off location. And may have extra addons that the customers request along with the service.

How to manage trips, from listing the trips and filtering them, and updating it.



## Listing Trips

From the left side menu go to Trips >> Trips, to list the available trips.

![Trips list](assets/img/dashboard/trips-list.jpg)



### List filtering

![Trips list quick filter](assets/img/dashboard/trips-quick-filter.jpg)



Here are the available filters that can be applied to the list, from the quick filter option:

- **Completed Trips**: list all completed trips
- **In progress Trips**: list the trips that have been taken by a driver, and currently the driver proceeding it
- **Scheduled Trips**: list the trips are not yet taken by a driver, and its booking time have not yet reached
- **Canceled Trips**: list all canceled trips



### With labor trips

Some trips service will be presented with extra **W/L** in their name

![Trip list service](assets/img/dashboard/trips-list-services.jpg)

This indicate that the user requested a service and added special **addons** *Labors for load & unload*.

It presented here just for quick representation of trips with addons *Labors for load & unload*. And it is not part of the service name.



## Trips Price structure

Trip price depends on multiple factors,  which are:

- Distance and duration price
- Addons price
- Areas price
- Discounts from Promo or user wallet

### Distance and Duration price

When the user books a trip he will be requested to provide pickup and destination locations, then the system will calculate the distance and the duration that it will take the driver to complete the trip.

Then based on the distance and duration we got, the system will calculate the price depending on the **service Price** the user requested.

> **Note**: refer [Service Price section](dashboard/services.md#prices) for more details on how the service price is structured.



### Addons price

If the user requested additional addons with his booking, and the **Addons** have price. Then the customer will be charged extra for the addons. 

> **Note**: refer [Service Addons section](dashboard/services.md#addons) for more details.



### Areas price

Areas are locations when the user request a trip and set the destination to that location he will receive increase or reduction (depending on the area type) on his total trip price.

This additional increase or reduction will only include applied on the *distance and duration price*, and will not include prices of **Addons**, or discount from the promo and user wallet.

> **Note**: refer [Service Areas section](dashboard/services.md#areas) for more details



### Discounts from promo or user wallet

The user will receive a discount for his trip if he applied a **Promo** code, or he has amount in his wallet.

Discount amount depends on the promo configuration or the user wallet amount.

If the user applied promo code and he has amount in his wallet, then the promo code discount will take precedence over user wallet.



## Trips status

The trip may go through different state, it will be shown in different dashboard pages, here is the list

|                            Status                            |                         Description                          |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| <span style="background-color:#f39c12; color:white;border-radius:2px;padding:2px 4px; font-size:14px">Urgent</span> | the user requested on demand service and its currently waiting for a driver to accept it |
| <span style="background-color:#f39c12; color:white;border-radius:2px;padding:2px 4px; font-size:14px">Waiting offers </span> | the trip is scheduled and waiting for the providers to bid their prices on the order |
| <span style="background-color:#d2d6de;border-radius:2px;padding:2px 4px; font-size:14px">Scheduled</span> | the trip is scheduled and waiting for a driver to accept it  |
| <span style="background-color:#00c0ef;color:#fff;border-radius:2px;padding:2px 4px; font-size:14px">In progress</span> | the trip have been accepted, and currently the driver in his way to the pickup location |
| <span style="background-color:#00c0ef;color:#fff;border-radius:2px;padding:2px 4px; font-size:14px">Reached</span> |        the driver have reached to the pickup location        |
| <span style="background-color:#00c0ef;color:#fff;border-radius:2px;padding:2px 4px; font-size:14px">On Route</span> |      the driver started to go to the drop off location       |
| <span style="background-color:#00a65a;color:#fff;border-radius:2px;padding:2px 4px; font-size:14px">Completed</span> |              the driver have completed the trip              |
| <span style="background-color:#dd4b39;color:#fff;border-radius:2px;padding:2px 4px; font-size:14px">Cancled</span> | the trip have been canceled, it may be canceled by either the driver, the user, or the system |



## Trip Attributes

|      Attribute      |                         Description                          |
| :-----------------: | :----------------------------------------------------------: |
|       Service       |                the service the user requested                |
|        User         |               the user who requested this trip               |
|       Driver        |               The driver caring out this trip                |
|        Promo        |          The promo that been applied for this trip           |
|       status        |      Please refer Trip [status section](#trips-status)       |
|   Pickup Address    |                Address of the pickup location                |
| Destination Address |               Address of the drop off location               |
|     Created At      |            The date the user requested the server            |
|    Booking date     |             The date the user want this trip at              |
|      Distance       | Total distance of the trip from the pickup location to destination location |
|      Duration       | Total duration it will take the driver from the pickup location to reach to the destination location. After the driver completes that trip it will be updated to reflect the total time the took to complete this trip |
|        Price        | Total price of the trip, including the distance and duration price, addons price, and areas price |
|       Offers        | The offers that the service providers have gave the customer |
|    Cancel Reason    | The reason of the trip cancelation. The trip may be canceled by the user, driver, or the system |
|     Commission      |     total commission of the trip, including addons price     |
|        Areas        | The applied **Areas** for this trip. It will increase or reduces the total trip price, refer [Service Areas section](dashboard/services.md#areas) for more details |
|       Addons        | The applied **Addons** for this trip. refer [Service Addons section](dashboard/services.md#addons) for more details |
|        Times        |            Track of the trip status changes time             |
|     Description     |     The description the user provided during the booking     |
|       Weight        |       The weight the user provided during the booking        |
|       Images        |       The images the user provided during the booking        |
|      Fare Type      | Can have two values, **Estimate Tracking**: meaning the final trip price will be determined based on the actual distance the driver traveled from the pickup location to the destination location, **Fixed**: the final trip price will not be changed, and its based on the prediction of the distance and duration the trip will take |
|    Booking Type     | Can have tow values, **Urgent**: the user requested *On Demand* service, **Scheduled**: the user requested the service on later time |

