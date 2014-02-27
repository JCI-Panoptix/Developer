--- 
layout: previous 
title: Retrieve Building Data 
previous-version: true
categories: [Building] 
--- 

##Retrieve Building Data
To retrieve the list of all Buildings, use the following URL:
 
[https://api.mypanoptix.johnsoncontrols.com/v1/Configuration/Buildings](https://api.mypanoptix.johnsoncontrols.com/v1/Configuration/Buildings)
 
| | |
|-------------|-------- |
|Result Format|	JSON|
|HTTP Method|	GET|
|Requires Authentication	|Yes|
 
###Response Body Format
 
Note: Text within <> is a descriptive placeholder for a value or repeated elements.

{% highlight javascript linenos %}

    {  
	    "Address1": "6434 154th Ave NE",  
	    "Address2": "Park View",  
	    "Area": 4322.8,  
	    "AreaUnitofMeasureCode": "SQUARE_FEET",  
	    "BuildingDescription": "Corporate Headquarters2",  
	    "BuildingName": "Corporate Headquarters2/",  
	    "BuildingUrl": "adv://space/Wayne Enterprises/Corporate Headquarters2/",  
	    "City": "Seattle",  
	    "Latitude": 42.909716,  
	    "Longitude": -87.899382,  
	    "PostCode": "121",  
	    "StateCode": "56",  
	    "TimezoneCode": "Central Standard Time"  
	},  
	{  
	    "Address1": "5434 154th Ave NE",  
	    "Address2": "Park View",  
	    "Area": 4232.8,  
	    "AreaUnitofMeasureCode": "SQUARE_FEET",  
	    "BuildingDescription": "Corporate Headquarters1",  
	    "BuildingName": "Corporate Headquarters1/",  
	    "BuildingUrl": "adv://space/Wayne Enterprises/Corporate Headquarters1/",  
	    "City": "Seattle",  
	    "Latitude": 42.909716,  
	    "Longitude": -87.899382,  
	    "PostCode": "121",  
	    "StateCode": "56",  
	    "TimezoneCode": "Central Standard Time"  
	},  
	<...>  

{% endhighlight %} 
 
###Response Properties
 
 
AHUs response properties are described in the table below.

|Property	|Description	|Data Type	|Nullable|
|------------|---------------|----------|--------|
Address1	|First line of the building address. (ex. ""6434 154th Ave NE"")	|string	|yes
Address2	|Second line of the building street address if it does not all fit on first line. (ex. ""Park View"")	|string	|yes
Area	|Size of the building in the units specified in AreaUnitOfMeasure property. (ex. 4322.8)	|real	|yes
AreaUnitOfMeasureCode	|Unit of measure for the area property. (ex. ""SQUARE_FEET"") See [Valid Unit of Measure Codes]({{ site.baseurl }}/resources/UOM.html) for UnitofMeasureCodes.	|enumeration	|yes
BuildingDescription	|Customer defined description for the building. (ex. ""Corporate Headquarters2"")	|string	|yes
BuildingName	|Customer display name for the building. (ex. ""Corporate Headquarters2"")	|string	|no
BuildingUrl	|Unique identifier for the building. (ex. ""adv://space/Wayne Enterprises/Corporate Headquarters2/"")	|string	|no
City	|City the building is located in. (ex. ""Seattle"")	|string	|yes
Latitude	|Horizontal Global Positioning System coordinate on the earh. (ex. 42.909716)	|real	|yes
Longitude	|Vertical Global Positioning System coordinate on the earh. (ex.-87.899382)	|real	|yes
PostCode	|Mailing code that assists in sorting mail. (a.k.a zip code) (ex. ""53202"")	|string	|yes
StateCode	|State code for state the building is located in. (ex. ""WI"")	|string	|yes
TimezoneCode	|Time zone for the location of the building. (ex. ""Central Standard Time"") See [Time Zone Code ]({{ site.baseurl }}/resources/timezone.html)(for all return values for the TimezoneCode field.	|enumeration	|yes
