---
id: services
title: Services
---

# Services Management

Services are the most fundamental part in Awini system.

Services modular contains multiple parts, that all corporates together to build it. We will explore them all.



## Service Entities

### Packages 

Packages are entity that holds the services into different groups, it apply general configuration for the services that it holds. And its the first thing the customers are presented with in the app.

![](assets/img/dashboard/packages-mobile.png)

As it shown in the image, when the user clicks on any packages listed he will be taken into services list under the selected packages. The user can only see the packages that are in the city he selected.



### Services

![](assets/img/dashboard/services-mobile.png)

The services are listed on the second page of the booking. some services had child services that will be displayed as in the first service "Pick up".



### Prices

Prices entity defines how the pricing system is structured. Each service has multiple pricing range. For example a service may had prices for orders that are between 0 km - 50 km distances, and other price for range of 50 km - 120 km, and so on.



### Addons

Addons are special extra that the user adds with his orders, for example *Labors for load and unload*, some addons may had extra charges that will be added to total order price, and may be included in the order commission as well.

### Areas

Area are locations that will change how the order price is calculated. It may increase or reduce the total order price based on the area type, and may be applied into multiple locations.

### Area Types

Area types are connected with **Area** entity defined above, it has two types (Increase, Reduction), it increases/reduces a percentage of the total order price. It will not be applied to **Addons** prices.



## Service Modules Attributes

We will explore each modular attributes, starting with **Service**.



### Service Attributes  

|        Attribute        |                         Description                          |
| :---------------------: | :----------------------------------------------------------: |
|          Name           | English name of the attribute, this name will be displayed whenever the service is requested in the dashboard |
|       Arabic name       |     Same as the *Name* attribute, but in Arabic language     |
|          Photo          |      The photo that will be displayed in the mobile app      |
|         Status          |  Whether the is available to be booked from the mobile app   |
|    Visible to users     | If it is active, the service will be displayed in the users mobile app |
|   Visible to drivers    | If it is active, the service will be displayed in the drivers app |
|    Commission limit     | The commission limit will be set to driver *commission limit*, when the driver registers and select this service. Note that this attribute has no other purpose other then the one mentioned here. |
|     Commission rate     | The commission rate will be set to driver *commission rate*, when the driver registers and select this service. Note that this attribute has no other purpose other then the one mentioned here. |
| Minimum booking notice  | Minimum booking notice to stop customers making bookings that start too soon, it displayed in minutes. |
| Maximum advance booking | Maximum advance booking to stop people making bookings that occur too far in the future, it displayed in minutes. |
|    Minutes interval     | The different between the times of the that will be displayed to the user in the mobile app. |
|    Auto cancel after    | If the booking time exceeds this value, and the order have not been assigned to a driver, it will be canceled. |
|         Cities          | The cities this service is available in. This service will not be displayed if the user city is not listed here. |

---

### Packages Attribute

|      Attribute      |                         Description                          |
| :-----------------: | :----------------------------------------------------------: |
|        Name         | English name of the attribute, this name will be displayed whenever the package is requested in the dashboard |
|     Arabic name     |     Same as the *Name* attribute, but in Arabic language     |
| English description | It will be used when the image is not loaded in the mobile app |
|     Arabic name     | It will be used when the image is not loaded in the mobile app |
|    English image    |    The image that will be displayed to users when booking    |
|    Arabic image     |    The image that will be displayed to users when booking    |
|        Order        |  In which order the package will be displayed to customers   |
|       Status        | The customer will not be able to select this package, If this option is inactive |
|      Services       | The services under this package, only these services will be displayed to the customer if he selects this package |
|       Cities        | The cities under this package, the package will be displayed only if the customer selects this city |

---

### Prices Attribute

|    Attribute     |                         Description                          |
| :--------------: | :----------------------------------------------------------: |
|     Service      |           The service this price entity belongs to           |
| Range starts at  | In which range this price starts at, must be less than *Range ends at* |
|  Range ends at   | In which range this price ends at, must be greater than *Range starts at* |
|    Base price    | When an order distance is in this price range, it will have this *base price* |
| Travel price/km  |   The price of each kilometer of distance the order takes    |
| Travel price/min | The price of each minute the order takes, only the time of traveling is counted here, and not the time of load and unload |

---

### Addons

|         Attribute          |                         Description                          |
| :------------------------: | :----------------------------------------------------------: |
|            Name            | English name of the addons, this name will be displayed to customers |
|        Arabic name         | Arabic name of the addons, this name will be displayed to customers |
|           Image            | The image that will be displayed to customers at the time of booking |
|        Special Type        | This option will give the addon special function in the system. <span style="color:red">avoid using this option</span> |
|            Type            | How this addon will be displayed to the customer in the time of booking. |
|        Price/piece         |             Price of every item for this addon.              |
|          Minimum           | The minimum number of this item the user can book. must be less than *Maximum* |
|          Maximum           | The maximum number of this item the can book. must be greater than *Minimum* |
|      Commission rate       | How much commission the driver will be charged of total of this addon price. If the addon commission rate is set to 0, then the driver will not be charged commission for providing this addon. <span style="color:orange">This attribute is different than the driver *commission rate*, and driver *commission rate* is not applied on addons price</span> |
|           Status           |    Whether this addons is active for users to use or not     |
| Double price for traveling | If the order distance is over 120 km, then the number of items the user added for this addon will be doubled along with it total price. |
|          Service           | The service this addon belongs to, it will only be displayed with this service |
|          Package           | The addon will only be available for customers if they selected these packages, and then selected the service this addon is available for as well |

---

### Areas Attribute

|     Attribute      |                         Description                          |
| :----------------: | :----------------------------------------------------------: |
|      Service       | The service this area belongs to, it will only be applied with this service |
|     Area type      | The area type, if the order is in this area, then the pricing of **Area type** will be applied |
|       Radius       |            The distance from the center location             |
| Latitude/Longitude | The coordination of this are location, it will be set automatically from the map |
|       Status       |  If this area is inactive it will not be applied for orders  |

---

### Area Types Attribute

|  Attribute  |                         Description                          |
| :---------: | :----------------------------------------------------------: |
|    Name     | English name of the Area type, this name will be displayed for customers |
| Arabic name | Arabic name of the Area type, this name will be displayed for customers |
|    Type     | Whether this entity increases or reduces the total order price |
| Percentage  | increase/reduction percentage that will be applied to order  |
|    Color    | The color of **Area** having this **Area Type** when it is displayed on the map |

