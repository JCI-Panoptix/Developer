--- 
layout: previous 
title: API Overview 
previous-version: true
categories: [General] 
--- 

## Overview: Version One APIs
The Panoptix® API set is currently based on HTTPS requests and conforms to the design principles of REST; all requests are either HTTP GET or HTTP POST and return JSON responses. You can use any programming language to access the API, as long as the programming language can make HTTPS requests and parse JSON responses.
 
###Base URLs
 
The Panoptix Platform Services endpoints have the following URL structure:

	https://{HOST}/v1/

The HOST available are:

- Production: api.mypanoptix.johnsoncontrols.com
	
- Sandbox: api.mypanoptixstaging.johnsoncontrols.com
 
Example: [https://api.mypanoptix.johnsoncontrols.com/V1/Configuration/Meters](https://api.mypanoptix.johnsoncontrols.com/V1/Configuration/Meters)
 
###Parameters
 
API parameters such as meterUrl, pointUrl, startDate and endDate are used to provide input values in the request URL. These parameters also specify the desired results by acting as a filter. The format used is standard query string key/value pairs.
 
	key = value

The first pair is preceded by a ? and each subsequent pair is separated by an &, as shown in the following example.

[https://api.mypanoptix.johnsoncontrols.com/v1/Energy/Trends?meterUrl=adv://equip/Config/8/507/Building1 Whole Building Electric Utility Meter/&pointUrl=adv://811137E4-0AAB-4EC6-BBC6-2CB1B261CBFB/&startDate=2008-01-0100:00:00Z&endDate=2008-03-30 23:45:00Z](https://api.mypanoptix.johnsoncontrols.com/v1/Energy/Trends?meterUrl=adv://equip/Config/8/507/Building1%20Whole%20Building%20Electric%20Utility%20Meter/&pointUrl=adv://811137E4-0AAB-4EC6-BBC6-2CB1B261CBFB/&startDate=2008-01-0100:00:00Z&endDate=2008-03-30%2023:45:00Z)

 
Find links and method call information for the Panoptix API methods under the REST API Reference heading.

