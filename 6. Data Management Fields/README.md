# Data Management Fields

## Creating a Field in Vehicle Object

| Field Name        | Field Type                                                 | Description / Relation              |
|-------------------|--------------------------------------------------          |-------------------------------------|
| Vehicle Name      | Text                                                       | Vehicle name                        |
| Vehicle Model     | Picklist (Sedan, SUV, EV, etc.)                            | Vehicle model category              |
| Stock Quantity    | Number                                                     | Available stock quantity            |
| Price             | Currency                                                   | Vehicle price                       |
| Dealer            | Lookup (to Vehicle Dealer)                                 | Related dealer                      |
| Status            | Picklist (Available, Out of Stock, Discontinued)           | Vehicle availability status         |

> **Vehicle Name** already created from object creation before

![vehicle_model](./model.png)
> **Next - Next - Save & New**

![stock_quantity](./stock.png)
> **Next - Next - Save & New**

![price](./price.png)
> **Next - Next - Save & New**

![dealer](./dealer.png)
> Lookup Relation to Vehicle Dealer, **Next - Save & New**

![status](./status.png)

## Creating a Field in Vehicle Dealer Object

| Field Name        | Field Type    | Description / Relation | Note                                               |  
|-------------------|---------------|------------------------|  -                                                 |
| Dealer Name       | Text          | Dealer name            |                                                    |
| Dealer Location   | Text(60)          | Dealer location        | Length = 60                                        |
| Dealer Code       | Auto Number   | Unique dealer code     | Display Format = DC-{0000}, Starting Number = 001  |
| Phone             | Phone         | Dealer phone number    |                                                    |
| Email             | Email         | Dealer email address   |                                                    |

![dealer](./dealers.png)

## Creating a Field in Vehicle Order Object

| Field Name   | Field Type                                   | Description / Relation              |
|--------------|-----------------------------------------------|-------------------------------------|
| Customer     | Lookup (Vehicle Customer)                             | Related customer                    |
| Vehicle      | Lookup (Vehicle)                              | Related vehicle                     |
| Order Date   | Date                                          | Date of order                       |
| Status       | Picklist (Pending, Confirmed, Delivered, Canceled) | Order status                  |

![order](./order.png)


## Creating a Field in Vehicle Customer Object

| Field Name                | Field Type                               | Description / Relation              |
|---------------------------|------------------------------------------|-------------------------------------|
| Customer Name             | Text                                     | Customer full name                  |
| Email                     | Email                                    | Customer email address              |
| Phone                     | Phone                                    | Customer phone number               |
| Address                   | Text(60)                                     | Customer address                    |
| Preferred Vehicle Type    | Picklist (Sedan, SUV, EV, etc.)          | Preferred vehicle category          |

![customer](./customer.png)

## Creating a Field in Vehicle Test Drive Object

| Field Name        | Field Type                                   | Description / Relation              |
|-------------------|-----------------------------------------------|-------------------------------------|
| Customer          | Lookup (Vehicle Customer)                             | Related customer                    |
| Vehicle           | Lookup (Vehicle)                              | Related vehicle                     |
| Test Drive Date   | Date                                          | Scheduled test drive date           |
| Status            | Picklist (Scheduled, Completed, Canceled)    | Test drive status                   |

![test_drive](./drive.png)

## Creating a Field in Vehicle Service Request Object

| Field Name           | Field Type                                      | Description / Relation              |
|----------------------|--------------------------------------------------|-------------------------------------|
| Customer             | Lookup (Vehicle Customer)                                | Related customer                    |
| Vehicle              | Lookup (Vehicle)                                 | Related vehicle                     |
| Service Date         | Date                                             | Vehicle service date                |
| Issue Description    | Text(60)                                             | Description of service issue        |
| Status               | Picklist (Requested, In Progress, Completed)    | Service request status              |

![service](./service.png)
