---
tags:
  - discover
  - google
  - imagery
author:
  display_name: Rick Kelson
  email: rkelson@utah.gov
date: 2015-02-09 08:00:09 -0700
title: Discover Server Resources and Information
categories: []
---

### Discover Server
{: .text-left}

AGRC’s cloud-based server Discover provides imagery and base maps services in Open Geospatial Consortium (OGC) standard Web Map Tile Service (WMTS) and Web Map Service (WMS) in the Web Mercator WGS84 projection (wkid: 3857).

One featured offering from Discover is statewide 6 inch imagery collected and licensed by Google. Due to this licensed content, access to the Google imagery is only for **Utah’s cities, counties, special districts, state agencies, K12/Higher education, and tribes and contractors and formal partners of the immediate licensees.** To obtain access to the Discover server you need to fill out and understand the **[Organizational Usage Agreement](https://docs.google.com/a/utah.gov/forms/d/e/1FAIpQLScL5uUQIvw7op_ZcF4bijxcoOMGhNF0MXwJNGqSXS6IbjbKhA/viewform)** available from the **[Google Imagery License]({{"/discover/license/" | prepend: site.baseurl }})** page. Once the Organizational Usage Agreement is completed, you will receive information about the services and URL links to access the Discover server. The URLs to access the server will contain a quad-word (ex. `https://discover.agrc.utah.gov/login/path/your-unique-quad-word/`) unique to each user or organization.

If you are not covered by the license agreement for the Google imagery service you will need to fill out the **[Discover Server Access](https://docs.google.com/a/utah.gov/forms/d/e/1FAIpQLScvASb37-R9WeFHNUsbIYEcVzQ_ceT__G4PZUaCx_xZxTuEpA/viewform)** form. Once the form has been completed, you will receive information about the services and URL links to access the Discover server. The URLs to access the server will contain a quad-word (ex. `https://discover.agrc.utah.gov/login/path/your-unique-quad-word/`) unique to each user or organization.

- For imagery downloads visit [this page]({{ "/data/aerial-photography/" | prepend: site.baseurl }}).
- Instructions on how to [use the Discover services in Pro/ArcMap](#adding-a-wmts-or-wms-service-to-esri-products).
- Instructions on how to [use the Discover services in CAD](#adding-a-wms-service-to-cad).
- Instructions on how to [use the Discover services in Web Maps]({{site.baseurl}}{% post_url 2015-12-21-using-agrcs-new-web-mercator-services-in-your-web-maps %}).

### Coordinate System and Datum
{: .text-left}

The native coordinate system for the Google files and services is Web Mercator with a WGS 1984 datum. Many end users in Utah work in coordinate systems with a different datum (NAD 1983 for example). It will be critical for end users that require the highest locational precision to set up their working environment through the use of the appropriate geographic transformation. The geographic transformation parameter is needed to overcome the locational difference between the WGS84 and NAD83 datum's “realization points” that are about a meter apart. Without the proper geographic transformation, reprojection algorithms will not be able to resolve the last meter of positional accuracy. In order for the imagery to be positioned as accurately as possible when there is a difference between the native projection and datums of the imagery and the client viewing application, a [datum conversion]({{ "/downloads/Transformation.png" | prepend: site.baseurl }}) must be set. AGRC uses the `NAD_1983_To_WGS_1984_5` transformation when creating base map tiles and web applications. **There may be more accurate transformations based on the data you are working with**. The default (no transformation specified) will likely introduce several feet of horizontal positional error. More information: [NAD_1983_To_WGS_1984_5](https://support.esri.com/en/knowledgebase/techarticles/detail/24159)

### Horizontal Positional Accuracy
{: .text-left}

Stated horizontal positional accuracy of the Google imagery is expected to achieve or exceed one meter (CE90) in most areas without significant vertical relief. Higher precision is expected in urban areas, where existing supplemental ground control was more abundant.

### Adding a WMTS or WMS Service to esri Products
{: .text-left}

**ArcGIS Pro 2.x:**

1. `Insert -> Connections -> New WMTS Server`
1. Paste the `WMTS` link [you have been provided]({{ "/discover/license/" | prepend: site.baseurl }} "view Discover sign up information") into the `Server URL:` line and click `OK`
1. Navigate to the newly added `utah imagery - WMTS on discover.agrc.utah.gov.wmts` connection under `Servers` in the Catalog window.
1. Expand the nodes until you see a list of all of the imagery and base map services that are offered. The list can be viewed on the main [Discover]({{ "/discover/#services" | prepend: site.baseurl }}) page.

**ArcMap 10.x**

1. In ArcMap go to `Add Data -> GIS Server -> Add WMTS server`
1. Paste the `WMTS` link [you have been provided]({{ "/discover/license/" | prepend: site.baseurl }} "view Discover sign up information") into the `URL:` line and click `OK`
1. Navigate to the newly added `utah imagery – WMTS on discover.agrc.utah.gov` connection and **double click** to connect.
  - You can rename the connection after it has been added
1. Expand the nodes until you see a list of all of the imagery and base map services that are offered. The list can be viewed on the main [Discover]({{ "/discover/#services" | prepend: site.baseurl }}) page.


### Adding a WMTS or WMS Service to a Web Map
{: .text-left}

{%capture contact %}{% include contact.html subject=page.title contact=site.data.contacts.discover text='send an email to' hide-punctuation=true %}{% endcapture %}

Interested in using AGRC's Web Mercator services in your web maps? Take a look at [this page]({{"/using-agrcs-new-web-mercator-services-in-your-web-maps/" | prepend:site.baseurl}}) for more information. **Remember, if the web map is going to be public facing you need to request a separate quad-work link**. To do this {{ contact | strip_newlines }} and provide your web map URL domains.

### Adding a WMS Service to CAD
{: .text-left}

- **Bentley Microstation** users should take a look at the [How To document]({{ "/downloads/MicroStationGoogleWMS_HowTo.pdf" | prepend: site.baseurl }}).
- **AutoCAD Civil 3D 2016** users should take a look at the [How To document](https://us-support.nearmap.com/hc/en-us/articles/212242658-AutoCAD-Civil-3D-2016-WMS-Integration).

### Printing Web Maps with Discover Services
{: .text-left}

Take a look at this blog post for information about [Printing Web Maps with Discover Services]({{"/printing-web-maps-with-discover-services/" | prepend:site.baseurl}}).

### Google Archive Services
{: .text-left}

In addition to the statewide `Google` imagery service layer there are archive layers available (ex. `Google 2011archive`) of the Google imagery organized by year collected.

### Google Flight Dates
{: .text-left}

The [dates of each Google imagery flight](ftp://ftp.agrc.utah.gov/UtahSGID_Vector/UTM12_NAD83/INDICES/UnpackagedData/Google_UtahServiceDates/_Statewide/) block can be downloaded from our ftp site as a shapefile, viewed in [ArcGIS Online](https://arcg.is/1E0wq3b), or utilized through our SDE as layer `SGID10.INDICES.Google_UtahServiceDates`.

### Pro/ArcMap User Considerations
{: .text-left}

{%capture contact2 %}{% include contact.html subject=page.title contact=site.data.contacts.discover text='please contact' %}{% endcapture %}

If you have not yet received quad-word links to the service (ex. `https://discover.agrc.utah.gov/login/path/your-unique-quad-word/`) that do not require a username and password {{ contact2 | strip_newlines }}

Users experiencing problems with the service, such as blurry tiles or different year vintages at different scales, may need to clear their local cache.

- **ArcMap** Go to the service’s `Layer Properties -> Cache` tab and selecting `Clear Local Cache Now`. Be patient as this could take several minutes. If the blurry tiles persist you have the options to `Clear cache when the session ends` or `Don't cache any data locally`. Another option is to completely clear your ArcMap cache by going to `Customize -> ArcMap Options -> Display Cache -> Clear Cache`.

- **ArcGIS Pro** Go to the service’s `Layer Properties -> Cache` tab and selecting `Clear Cache`. You can also clear your entire Pro cache by going to the Pro project's `Options -> Display` and check `Clear cache` and selecting `OK`.

**ArcMap 10.1 users** should use the WMS service and not the WMTS. The WMTS in ArcMap 10.1 does not render correctly.

### Usage Tracking
{: .text-left}

To access the GCP services individual organizations will be provided URL links for the service unique to their organization. This will allow for tracking usage metrics and performance of the imagery service. Do not distribute the URL links outside of your organization or division.

### Google Logos
{: .text-left}

[Download zipfile of Google logos]({{ "/downloads/google_logos.zip" | prepend: site.baseurl }})
![white transparent]({{ "/images/ImageryCGoogle_WhiteTransparent.png" | prepend: site.baseurl }})
![white on black]({{ "/images/ImageryCGoogle_WhiteOnBlack.png" | prepend: site.baseurl }})

### Requests for On-Premise Use
{: .text-left}

{%capture contact3 %}{% include contact.html subject=page.title contact=site.data.contacts.discover text='Please provide the following information to' hide-punctuation=true %}{% endcapture %}

Request can be made to consume the imagery off-line when the provided imagery service does not suffice. {{ contact3 | strip_newlines }} for consideration:
  -	Name & organization:
  - Reason for request:
  - Working on behalf of:
  - Project names:
  - Project locations:

### Frequently Asked questions
{: .text-left}

- From time to time it is suggested that you refresh the connection to the imagery services by right-clicking your service connection, in ArcCatalog or ArcMap's Catalog Viewer, and select the `Refresh`  button to see the latest list of available services.
- Since the Google acquisition flight blocks are not done all at once (as opposed to the NAIP product for example), there will certainly be color and positional changes at flight block boundaries. For large area maps, the color-balanced NAIP may be a more aesthetically pleasing cartographic choice.
- A tile index of the .jp2 images that make up the service is available from our SDE as SGID10.INDICES.Google_Tiles or as a [download from our ftp](ftp://ftp.agrc.utah.gov/UtahSGID_Vector/UTM12_NAD83/INDICES/UnpackagedData/Google_Tiles/_Statewide/).
- For future updates, Utah can certainly pass along requests to Google for additional update areas or for specific collection periods. But there is no provision in the current contract to create any expectation that those requests will be acted upon.
- AGRC has downloaded a statewide master set of the image files for redistribution, as the download process directly from Google incurs transactional costs for cloud server & bandwidth usage.
- AGRC has a [feedback reporting form](https://docs.google.com/a/utah.gov/forms/d/1UGU77SPM_HX0r8zblIs05C-H5mLyRja1gRT7Fu4aKZk/viewform?fbzx=-6743712545663240221) for imagery users around the state to report imagery and service issues so these can be passed along to Google. Please direct your feed back to the form.
