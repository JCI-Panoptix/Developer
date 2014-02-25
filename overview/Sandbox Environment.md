---
layout: default 
title: Sandbox Environment 
resource: true 
categories: [overview] 
--- 
##Sandbox Environment

Sample data for a virtual Panoptix® customer called Green Company, is available on the Sandbox environment. Green Company has the following configuration:
 
* 13 spaces (1 site, 3 buildings and 9 floors)
* 7 Electrical Meters (6 Interval Demand Points and 1 Instantaneous Consumption Point)
* 2 Natural Gas Meters (1 Instantaneous Demand Point)
* 2 Water Meters (1 Instantaneous Demand Point)
* 2 Steam Meters (1 Instantaneous Demand Point)
* 135 Variable Air Volume Boxes (Mixed configurations)
* 1 Air Handling Unit (Mixed configurations)
* 2 Chillers (Mixed configurations)
* 11 Utility Account(1 Electricity,1 Natural Gas,1 Water, 1 Sewer,1 Light Fuel Oil, 1 Heavy Fuel Oil,1 Propane, 1 Coal, 1 Steam, 1 Bagasse, 1 Chilled Water)
 
To simulate the continuous sampling of BAS point values new data is periodically inserted into the Sandbox every hour. Every insert will contain one hour of data in the future copied from the corresponding day and time in the previous week. i.e. at 1:59am UTC the system automatically inserts 1 full hour of samples from 02:00am to 02:59am.
 
*Note:* An artificial peak is inserted into the Engineering Building Electric Meter Interval Demand point's trend value on the first Friday on or after the tenth of the month at 1:00 p.m. UTC.

