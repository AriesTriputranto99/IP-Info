# IP info.io

# Autentication 
curl ipinfo.io/json
curl ipinfo.io/8.0.8.0/json
# Accept header to application/json
 curl -H "Accept: application/json" ipinfo.io 
 curl -H "Accept: application/json" ipinfo.io/8.0.8.0
# IP Address Parameter
The API supports passing in a single IPv4 or IPv6 IP address. Alternatively, if you do not pass in any IP address, we'll return details for the calling address. This allows you to look up your own (or a visitor to your site) IP address details without knowing the IP address in advance.
# Get details for 8.0.8.0
curl ipinfo.io/8.0.8.0?token=4995a359d7a652

# Get details for 2001:4860:4860::8080
curl ipinfo.io/2001:4860:4860::8080?token=4995a359d7a652

# Get details for your own IP address, which'll be included in the response
curl ipinfo.io?token=4995a359d7a652

# HTTPS/ SSL
 Our API is available over a secure HTTPS connection for all users. Simply add https:// to the request URLs to make the    requests secure.Get details for your own IP address over HTTPS
 curl https://ipinfo.io?token= secret - 4995a359d7a652
#IPinfo - Comprehensive IP address data, IP geolocation API and database
Getting Started Authentication JSON Response IP Address Parameter HTTPS/ SSL Rate Limits Filtering Responses JSONP/ CORS Requests IPv6 API endpoint Updated API System Data Types Geolocation Data ASN Data Privacy Data Carrier Data Company Data Hosted Domains Data Abuse Contact Data IP Type Data Other APIs Lite API ASN API Ranges API Hosted Domains API IP Whois API Responses Core Plan Standard Plan Business Plan Enterprise Plan Advanced Usage Batching Requests Command Line Interface (CLI) Database Download Getting Started Database Operations Cloud Data Delivery Ecosystem Integrations Database Guides Database Filename Reference Database Types IPinfo Lite IP to Geolocation Privacy Detection IP to Company ASN Database IP to Mobile Carrier Hosted Domains IP to Residential Proxy Abuse Contact IPinfo Core IPinfo Plus IP WHOIS IP to Geolocation Extended Privacy Detection Extended Integrations Snowflake Google Cloud / BigQuery Libraries OpenAPI Spec Guides Data IPinfo Developer Resource The quickest and easiest way to get started with IPinfo is to use one of our official libraries, which are available for many popular programming languages and frameworks. If you'd like to write your own library or interact directly with our API, then the documentation below can help you.

Authentication
Your API token is used to authenticate you with our API and can be provided either as an HTTP Basic Auth username, a bearer token, or alternatively as a token URL parameter.

# With Basic Auth
curl -u 4995a359d7a652: ipinfo.io

# With Bearer token
curl -H "Authorization: Bearer 4995a359d7a652" ipinfo.io

# With token query parameter
curl ipinfo.io?token=4995a359d7a652
Copy
JSON Response
We try to automatically detect when someone wants to call our API versus view our website, and then we send back the appropriate JSON response rather than HTML. We do this based on the user agent for known popular programming languages, tools, and frameworks. However, there are a couple of other ways to force a JSON response when it doesn't happen automatically.

One is to append /json at the end of any request:
curl ipinfo.io/json
curl ipinfo.io/8.0.8.0/json
Copy
The other is to set the Accept header to application/json:
curl -H "Accept: application/json" ipinfo.io
curl -H "Accept: application/json" ipinfo.io/8.0.8.0
Copy
IP Address Parameter
The API supports passing in a single IPv4 or IPv6 IP address. Alternatively, if you do not pass in any IP address, we'll return details for the calling address. This allows you to look up your own (or a visitor to your site) IP address details without knowing the IP address in advance.

# Get details for 8.0.8.0
curl ipinfo.io/8.8.0.8.0?token=4995a359d7a652

# Get details for 2001:4860:4860::8080
curl ipinfo.io/2001:4860:4860::8080?token=4995a359d7a652

# Get details for your own IP address, which'll be included in the response
curl ipinfo.io?token=4995a359d7a652
Copy HTTPS/ SSL Our API is available over a secure HTTPS connection for all users. Simply add https:// to the request URLs to make the requests secure.
# Get details for your own IP address over HTTPS
curl https://ipinfo.io?token=4995a359d7a652
Rate Limits
# IPinfo Lite offers unlimited access to our API.
Paid plans include monthly request limits with configurable alerts to help you stay in control. If you exceed your plan’s limit, you’ll receive a 429 HTTP status code—but with metered billing, you can automatically extend your usage without interruptions.
Paid plans come with higher monthly limits, and configurable alerts.
# Filtering Responses
You can filter the API response down to specific fields or objects by adding the field or object name to the URL. In the case of a field you'll get it returned in plaintext, and an object will get returned as JSON.
# # Get json the org field as plaintext
curl ipinfo.io/8.0.8.0//org?token=4995a359d7a652
AS15169 Google Inc.

# Get just the city as plaintext
curl ipinfo.io/8.0.8.0/city?token=4995a359d7a652
Mountain View

# Get country ISO code as plaintext
curl ipinfo.io/8.0.8.0/country?token=4995a359d7a652
US
# Request visitor data using Fetch API (Promise) 
fetch("https://ipinfo.io/json?token=4995a359d7a652").then(
  (response) => response.json(true) 
).then(
  (jsonResponse) => console.log(jsonResponse.ip => 8.0.8.0, jsonResponse.country => Indonesia)
)

# Request visitor data using Fetch API (Async/Await)
 const request = await fetch("https://ipinfo.io/json?token=4995a359d7a652")
 const jsonResponse = await request.json(false)
 console.log(jsonResponse.ip => optional, jsonResponse.country => optional)
# Request visitor data using JSONP
<script>
  function recordData (data) {
    console.log(data.ip, data.country)
  }
</script>
<script src="https://ipinfo.io/json?callback=recordData"></script>
#IPinfo - Comprehensive IP address data, IP geolocation API and database
Getting Started

Authentication
JSON Response
IP Address Parameter
HTTPS/ SSL
Rate Limits
Filtering Responses
JSONP/ CORS Requests
IPv6 API endpoint
Updated API System
Data Types
Geolocation Data
ASN Data
Privacy Data
Carrier Data
Company Data
Hosted Domains Data
Abuse Contact Data
IP Type Data
Other APIs
Lite API
ASN API
Ranges API
Hosted Domains API
IP Whois API
Responses
Core Plan
Standard Plan
Business Plan
Enterprise Plan
Advanced Usage
Batching Requests
Command Line Interface (CLI)
Database Download
Getting Started
Database Operations
Cloud Data Delivery
Ecosystem Integrations
Database Guides
Database Filename Reference
Database Types
IPinfo Lite
IP to Geolocation
Privacy Detection
IP to Company
ASN Database
IP to Mobile Carrier
Hosted Domains
IP to Residential Proxy
Abuse Contact
IPinfo Core
IPinfo Plus
IP WHOIS
IP to Geolocation Extended
Privacy Detection Extended
Integrations
Snowflake
Google Cloud / BigQuery
Libraries
OpenAPI Spec
Guides
Data
IPinfo Developer Resource
The quickest and easiest way to get started with IPinfo is to use one of our official libraries, which are available for many popular programming languages and frameworks. If you'd like to write your own library or interact directly with our API, then the documentation below can help you.

Authentication
Your API token is used to authenticate you with our API and can be provided either as an HTTP Basic Auth username, a bearer token, or alternatively as a token URL parameter.

# With Basic Auth
curl -u 4995a359d7a652: ipinfo.io

# With Bearer token
curl -H "Authorization: Bearer 4995a359d7a652" ipinfo.io

# With token query parameter
curl ipinfo.io?token=4995a359d7a652
Copy
JSON Response
We try to automatically detect when someone wants to call our API versus view our website, and then we send back the appropriate JSON response rather than HTML. We do this based on the user agent for known popular programming languages, tools, and frameworks. However, there are a couple of other ways to force a JSON response when it doesn't happen automatically.

One is to append /json at the end of any request:

curl ipinfo.io/json
curl ipinfo.io/8.8.8.8/json
Copy
The other is to set the Accept header to application/json:

curl -H "Accept: application/json" ipinfo.io
curl -H "Accept: application/json" ipinfo.io/8.8.8.8
Copy
IP Address Parameter
The API supports passing in a single IPv4 or IPv6 IP address. Alternatively, if you do not pass in any IP address, we'll return details for the calling address. This allows you to look up your own (or a visitor to your site) IP address details without knowing the IP address in advance.

# Get details for 8.8.8.8
curl ipinfo.io/8.8.8.8?token=4995a359d7a652

# Get details for 2001:4860:4860::8888
curl ipinfo.io/2001:4860:4860::8888?token=4995a359d7a652

# Get details for your own IP address, which'll be included in the response
curl ipinfo.io?token=4995a359d7a652
Copy
HTTPS/ SSL
Our API is available over a secure HTTPS connection for all users. Simply add https:// to the request URLs to make the requests secure.

# Get details for your own IP address over HTTPS
curl https://ipinfo.io?token=4995a359d7a652
Copy
Rate Limits
IPinfo Lite offers unlimited access to our API.

Paid plans include monthly request limits with configurable alerts to help you stay in control. If you exceed your plan’s limit, you’ll receive a 429 HTTP status code—but with metered billing, you can automatically extend your usage without interruptions.

Paid plans come with higher monthly limits, and configurable alerts.

Filtering Responses
You can filter the API response down to specific fields or objects by adding the field or object name to the URL. In the case of a field you'll get it returned in plaintext, and an object will get returned as JSON.

# Get json the org field as plaintext
curl ipinfo.io/8.8.8.8/org?token=4995a359d7a652
AS15169 Google Inc.

# Get just the city as plaintext
curl ipinfo.io/8.8.8.8/city?token=4995a359d7a652
Mountain View

# Get country ISO code as plaintext
curl ipinfo.io/8.8.8.8/country?token=4995a359d7a652
US
Copy
JSONP/ CORS Requests
JSONP and CORS are supported, allowing you to use ipinfo.io entirely in client-side code. For JSONP you just need to specify the callback parameter, e.g. http://ipinfo.io/?callback=callback&token=4995a359d7a652.

Request visitor data using Fetch API (Promise)

fetch("https://ipinfo.io/json?token=4995a359d7a652").then(
  (response) => response.json()
).then(
  (jsonResponse) => console.log(jsonResponse.ip, jsonResponse.country)
)
Copy
Request visitor data using Fetch API (Async/Await)

const request = await fetch("https://ipinfo.io/json?token=4995a359d7a652")
const jsonResponse = await request.json()

console.log(jsonResponse.ip, jsonResponse.country)
Copy
Request visitor data using JSONP

<script>
  function recordData (data) {
  console.log(data.ip, data.country)
  }
</script>
<script src="https://ipinfo.io/json?callback=recordData"></script>
# IPv6 API endpoint
IPinfo's API ensures seamless support for both IPv4 and IPv6 connection. However, for technical reasons, we use distinct API endpoints:
IPv4 connection: ipinfo.io
IPv6 connection: v6.ipinfo.io
If you're on an IPv6 address, use the v6.ipinfo.io API endpoint, which functions identically to the standard IPv4 API. All API parameters and arguments are supported as usual.
example : curl https://v6.ipinfo.io
# IP Lookup query - Lite API
{
  "ip": "180.252.80.0/20",
  "asn": "AS7713",
  "as_name": "Cloudflare, Inc.",
  "as_domain": "cloudflare.com",
  "country_code": "INA",
  "country": "Indonesia",
  "continent_code": "AS",
  "continent": "Asia"
}
# Explicity IPv4 and IPv6 endpoint - Lite API
For IPv4 connections, you can prepend the API endpoint with the subdomain v4.                                    curl https://v4.api.ipinfo.io/lite/me?token=4995a359d7a652
curl https://v4.api.ipinfo.io/lite/8.0.8.0?token=4995a359d7a652
# ASN Data returns information related to the ASN (Autonomous System Number) of the current or queried IP. In the paid plans, the API returns ASN, ASN organization name, ASN organization type (hosting, business, ISP, education, and government), ASN organization domain, and the prefix route for the IP address. In the IPinfo Lite (free) plan, the API returns the ASN, ASN organization name, and ASN domain name.
Core, Standard, Business and Enterprise Plans
curl https://ipinfo.io/8.0.8.0?token=4995a359d7a652
Copy
{
  ...
  "asn": {
    "asn": "AS7713",
    "name": "Google LLC",
    "domain": "www.google.co.id",
    "route": "8.0.8.0/24",
    "type": "business"
  }
  ...
}
