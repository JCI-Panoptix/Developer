---
layout: default 
title: Quick Start Guide 
overview: true 
categories: [main]
--- 

## Quick Start Guide

This is a quick start guide for developers who want to integrate the Panoptix® API set into their application. This guide assumes you are familiar with the basic concepts of APIs, XML, HTTP request methods, and the REST style of software architecture. If you require further information after reading this guide, please documentation under the REST API Reference section.

## Getting Started

To get up and running quickly with the Panoptix APIs, perform the following steps:

  * Create an account (see step one below).
  * Request an access token (see step two below).
  * Make an API call (see step three below).

## The Steps

### One - Create a Panoptix Developer Center account.

  1. [Sign up for API access.](https://developer.panoptix.com/signup) Enter your user and company information.
  2. Read and agree to the Johnson Controls, Inc. API Usage Agreement and click "Sign Up."
  3. Upon receiving approval via email (may take up to two business days), sign in to your account.
  4. Under Sandbox, click "View" next to Demo app.

	![]({{site.baseurl}}/images/quickstart/Step One_Select Applications.png?raw=true)

  5. Record the Client ID and Client Secret.

	![]({{site.baseurl}}/images/quickstart/Step One_Record the Client ID and Client Secret.png?raw=true)

  6. Record your Freemium Panoptix Credential (username and password).

	![]({{site.baseurl}}/images/quickstart/Step One_Record your Freemium.png?raw=true)

### Two - Request access token.

  1. Download and install [Chrome Advanced Rest Client App](https://chrome.google.com/webstore/detail/hgmloofddffdnphfgcellkdfbfbjeloo).

  2. Create https POST request against the URL:

	[ https://mypanoptixstaging.johnsoncontrols.com/identity/issue/oauth2/token](https://mypanoptixstaging.johnsoncontrols.com/identity/issue/oauth2/token)


  3. Add the following URL query string parameters:

	grant_type=password

	username=[Freemium panoptix UserName]

	password=[Freemium panoptix Password]

	For example:

	[ https://mypanoptixstaging.johnsoncontrols.com/identity/issue/oauth2/token?grant_type=password&amp;username=test@example.com&amp;password=example](https://mypanoptixstaging.johnsoncontrols.com/identity/issue/oauth2/token?grant_type=password&amp;username=test@example.com&amp;password=example/)

  4. Add the header fields:

	Authorization: Basic [client_id:client_secret] must be base 64 encoded

	Content-Type: application/json

	![]({{site.baseurl}}/images/quickstart/Step Two_4.png?raw=true)

  5. Click "Construct" to build the Basic Authorization field and enter your Client_ID and Client_Secret.

	![]({{site.baseurl}}/images/quickstart/Step Two_5.png?raw=true)

  6. Send the request and Copy the access_token field value to clipboard.

	![](/images/quickstart/Step Two_6.png?raw=true)

### Three - Calling a Panoptix API

  1. Create https GET request against this URL:

	[https://api.mypanoptixstaging.johnsoncontrols.com/V1/Configuration/Meters](https://api.mypanoptixstaging.johnsoncontrols.com/V1/Configuration/Meters)

  2. Add the header field: Authorization: Bearer [access_token value].

	![]({{site.baseurl}}/images/quickstart/Step Three_2.png?raw=true)

  3. Send the request.

	![]({{site.baseurl}}/images/quickstart/Step Three_3.png?raw=true)
