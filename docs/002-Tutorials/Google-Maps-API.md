---
layout: default
title: • Google Maps Static API
parent: Tutorials
nav_order: 1
description: "How to use the Google Map Static API"
permalink: /google-static-api/
image: 
author: James H. Jay
---
<img src="/assets/images/maps_static/maps_static_api.png" width="80%" alt="img">

# Google Maps Static API for Beginners!
{: .no_toc }

---

## Introduction

The Google Maps Static API retrieves an image (in GIF, PNG, or JPEG format) via a URL with three *required* pieces of information:
- The center location
- The zoom Level 
- The size of the map

---

### Quick Peek
{: .no_toc }

The following URL will return an image that can be directly embedded to your website that accepts an <img> tag. No javascript required.

```
https://maps.googleapis.com/maps/api/staticmap?center=San%20Francisco,CA&zoom=12&size=600x600&key=YOUR_API_KEY
```

><small> NOTE: Replace YOU_API_KEY in the URL with your private API Key in order to access the Google Map Static API. (Keep this API key private.) </small>


<!-- MAP OF LA
-->
<img src="/assets/images/maps_static/map_la.png" width="450px" alt="img">

---

## Before you begin:
{: .no_toc }

This guide is intended for beginners. Only key parameters that are absolutely necessary to retrieve an image will be covered. 
For a more advanced tutorial on the static API, see [Google Maps Static API](https://developers.google.com/maps/documentation/maps-static).

## In this lesson, we'll cover:
{: .no_toc }
## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## API Key and Enable Billing

Before requesting an image, create a personal API key and enable billing <br> <small>(💡 NOTE: the service is free for the first 90 days) in order to use Google's Map API service.</small>

- Review the <a href="https://developers.google.com/maps/documentation/maps-static/get-api-key#creating-api-keys"> authentication requirements </a> and register for a free API key. 
- Review the <a href="https://developers.google.com/maps/documentation/maps-static/usage-and-billing"> API usage and billing</a> information.<small>(you need to enable billing onto your project).

---

## What is a URL

### Base URL:
{: .no_toc }

A URL is a Uniform Resource Locator, the name given to the way webpages are referenced and found when using web browsers. Below is a typical structure of a URL and a description of its components:

<img src="/assets/images/maps_static/url2.png" width="600px" alt="img">

| components  | Description |
| ----------- | ------------|
| Protocol   | `https://` *(Hypertext Transfer Protocol)* tells the web server which protocol to use when accessing a web page. Another example of a common protocol you may have seen is `mailto://`.       |
| Subdomain | `www` *(World Wide Web)* is the most commonly used subdomain which contains the website's web pages. |
| Domain | `google`, the websites name, is the highest-level part of the URL and can be thought of as the location where your webpage is stored. |
| Top-level domain | `.com` is the top-level domain and plays an important role in the DNS lookup. Other examples of common top-level domains are `.org`, `.net` `.info`. |

To learn more about URLs, see <a href="">URL Construction</a>.

---

### Query Strings

Query strings are used to pass in additional information via the URL to the server. Query strings appear after the `?` and are part of the URL which contain key-value pairs where data is passed.

<img src="/assets/images/maps_static/url3.png" width="800px" alt="img">

| components  | Description |
| ----------- | ------------|
|?|`?` is the identifier that separates the base URL from the query strings. All query strings begin with `?`.|

> (Key = Value pair)

| ----------- | ---------- |
|Parameter|`paramater1` is the name of the paramter defined by the server.|
|=|`=` is the separator that connects key and value pairs.|
|value|`value1` is the value assigned to the parameter.|

|&|The `&` joins multiple query strings, if present.|

---

### Required parameters

3 parameters are required *(along with our private API KEY)* to retrieve an image using Google Maps Static API.

> Required parameters: <br>
> <a href="#Location"> 1. Center location </a><br>
> <a href="#Zoom_level"> 2. Zoom level </a><br>
> <a href="#Size"> 3. Size of the map </a>

<!-- Map annotations
-->
<img src="/assets/images/maps_static/map_details.png" width="600px" alt="img">




<!-- 1. CENTER LOCATION
-->
<h3 id="Location">1. Center location</h3>  
The `center` parameter accepts two forms:

> <a href="#longlat"> • Longitude and Latitude Coordinates </a> <br>
> or <br>
> <a href="#address"> • String address </a>

---



<!-- LONG/LAT DETAILS
-->
<h4 id="longlat"> • Longitude and Latitude</h4>

> Longitude and latitude coordinates specify locations using numbers separated by commas. 

>> Example: <big>`(23.1234, 12.1234)`</big><br>
>> *Note: Anything more than 6 digits per coordinate will be ignored.*
> To retrieve the longitude and latitude coordinates of a specific location, see <a href="https://www.google.com/maps"> Get Coordinates</a>



<!-- STRING ADDRESS DETAILS
-->
<h4 id="address"> • String address</h4>

> The string address is the more common way of thinking of locations. Google maps converts string addresses into a geographic point, a process known as geocoding.

>When using String addresses, strings must be URL-enocded like so: <br>
>> Example: <big>`San Francisco`</big> should be written as <big>`San+Francisco`</big>. <br>
*(the <big>`+`</big> will take the place of the space using URL-encoding).*

> For more information, see <a href="https://developers.google.com/maps/url-encoding">URL encoding</a>.

---

<h3 id="Zoom_level">2. Zoom level</h3> 

The `Zoom` parameter defines the magnification level of the map. Zoom levels start from 0 (widest level) to 21+ (most detailed).

Here's the general guideline of approximate zoom levels:

> - Level 1: World (widest view)
> - Level 5: Continent 
> - Level 10: City
> - Level 15: Streets
> - Level 20: Buildings (detailed view)

About Zoom Levels:<br>
<small>- Each succeeding zoom level doubles the precision in both horizontal and vertical dimensions.</small><br>
<small>- Zoom levels vary depending on the location. </small><br>
<small>- If you send a request with a zoom level that is not available, the api will return the maximum zoom level available at that location. </small>

---

<h3 id="Size">3. Size</h3> 

The `size` paramenter determines the dimensions in pixels of the returned image. This parameter takes 2 sets of numerals in the form of (horizontal_value) x (vertical_value).

> Example: `500x400` results in a map of 500 pixles wide by 400 pixels high. 

>Note: Maps smaller than 180 pixels in width will display a reduced-size google logo. 

---

## Putting it all together
Our goal is to retrieve an image at `street level` of the `Golden Gate Bridge` that's about `medium width and height` in size.

Our parameters may look something like this:

| Key parameters | Values |
|------------|--------------|
| center | Golden Gate Bridge |
| Zoom | 17 |
| Size | 500x500 |
| Your_API_KEY | (insert private API key) |

When componsed together, our final URL will look like this:
```
https://maps.googleapis.com/maps/api/staticmap?center=Golden%Gate%Bridge&zoom=17&size=500x500&key=YOUR_API_KEY
```

---

## What's next

And that's it! In this lesson, we've covered:
> - Creating your first API key.
> - Understanding how a URL is constructed.
> - Composed a custom query string
> - Retrieved your first image using the Maps Static API. 

 To see more features you can add to your map, see <a href="https://developers.google.com/maps/documentation/maps-static">Maps Static API</a>.
 
<br>

---

<h1><center> You may also like </center></h1>
<div class="row">
    <div class="column_grid">
        <a href="/google-static-api">
            <img border="0" alt="img" src="/assets/images/cards/maps_static.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/swift-variables">
            <img border="0" alt="img" src="/assets/images/cards/var.png" width="230" height="450">
        </a>
    </div>
    <div class="column_grid">
        <a href="/swift-arrays">
            <img border="0" alt="img" src="/assets/images/cards/arrays.png" width="230" height="450">
        </a>
    </div>
</div>