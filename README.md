# imin Extension Namespace

This repository holds the [JSON-LD definition](http://ns.imin.co/imin.jsonld) of the imin namespace. The terms in this namespace are defined for use within the [imin Search API](https://docs.imin.co).

imin works as part of the [OpenActive Community Group](https://www.w3.org/community/openactive) to promote the usecases represented by the properties within this namespace, with the intention of standardising them over time.

This namespace MUST be referenced using the URL `"https://imin.co/"` (which will return the [JSON-LD definition](http://ns.imin.co/imin.jsonld) if the `Accept` header contains `application/ld+json`), and is designed to be used in conjunction with the `"https://openactive.io/"` namespace.

Please raise requests for content or issues related to the namespace via [GitHub](https://github.com/imin-ltd/ns/issues). 

Recommended usage as follows:
```json
{
  "@context": [
    "https://openactive.io/",
    "https://imin.co/"
  ],
  "type": "SessionSeries",
  "name": "Tai chi Class",
  "url": "http://www.example.org/events/1",
  "location": {
    "type": "Place",
    "imin:fullAddress": "ExampleCo Gym Kingswood, 1 High Street, Kingswood, South Gloucestershire, BS1 4SD",
    "name": "ExampleCo Gym Kingswood",
    "address": {
      "type": "PostalAddress",
      "streetAddress": "1 High Street",
      "addressLocality": "Kingswood",
      "addressRegion": "South Gloucestershire",
      "postalCode": "BS1 4SD",
      "addressCountry": "GB"
    }
  }
}
```

## Extension Properties

| Property                   | Type    | Description                                                        |
|----------------------------|---------|--------------------------------------------------------------------|
| `imin:publicAdultPrice`    | decimal | The adult price derived from the appropriate Offer                 |
| `imin:publicJuniorPrice`   | decimal | The junior price derived from the appropriate Offer                |
| `imin:membershipRequired`  | boolean | Indicates whether this Offer is only available to members.         |
| `imin:fullAddress`         | string  | Full address in one line                                           |
| `imin:specialRequirements` | Concept | List of related special requirements from a controlled vocabulary. |
