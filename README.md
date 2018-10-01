# imin Extension Namespace Vocabulary Terms

This repository holds the [JSON-LD definition](http://ns.imin.co/imin.jsonld) of the imin namespace. The terms in this namespace are defined for use within the [imin Search API](https://docs.imin.co), and are not designed to be used by data publishers. Data publishers should consider publishing thier own extension namespace or using the [OpenActive Beta Namespace](https://www.openactive.io/ns-beta/).

imin works as part of the [OpenActive Community Group](https://www.w3.org/community/openactive) to promote the usecases represented by the properties within this namespace, with the intention of standardising them over time.

This namespace MUST be referenced using the URL `"https://imin.co/"` (which will return the [JSON-LD definition](http://ns.imin.co/imin.jsonld) if the `Accept` header contains `application/ld+json`), and is designed to be used in conjunction with the `"https://openactive.io/"` namespace.

Please raise requests for content or issues related to the namespace via [GitHub](https://github.com/imin-ltd/extension-namespace/issues). 

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

# Namespace

## Properties

| (Class) Property    |  Expected Type  | Description                                                         |
|---------------------|-----------------|---------------------------------------------------------------------|
| ([`schema:AggregateOffer`](https://schema.org/AggregateOffer)) <br/> `imin:publicAdultPrice` | [`schema:Float`](https://schema.org/Float) | Price for adult non-members derived from the appropriate Offer. |
| ([`schema:AggregateOffer`](https://schema.org/AggregateOffer)) <br/> `imin:publicJuniorPrice` | [`schema:Float`](https://schema.org/Float) | Price for junior non-members derived from the appropriate Offer. |
| ([`schema:Event`](https://schema.org/Event)) <br/> `imin:level` | [`imin:LevelType`](https://imin.co/LevelType) | The difficulty level of an Event, in a structured format. |
| ([`schema:Offer`](https://schema.org/Offer)) <br/> `imin:membershipRequired` | [`schema:Boolean`](https://schema.org/Boolean) | Indicates whether this offer is only available to members. |
| ([`schema:PostalAddress`](https://schema.org/PostalAddress)) <br/> `imin:fullAddress` | [`schema:String`](https://schema.org/String) | Full address in one line. |



## Classes

| Class                      | subClass | Description                                                                                 |
|----------------------------|----------|---------------------------------------------------------------------------------------------|
| `imin:LevelType` | [`schema:StructuredValue`](https://schema.org/StructuredValue) | Structured difficulty levels with free-text labels to allow them to vary based on context. |



## Enumeration Values

| Type          | Value    | Description                                                                    |
|---------------|----------|--------------------------------------------------------------------------------|
| [`imin:LevelType`](https://imin.co/LevelType) | `https://imin.co/AdvancedLevel` | Advanced difficulty level |
| [`imin:LevelType`](https://imin.co/LevelType) | `https://imin.co/BeginnerLevel` | Beginner difficulty level |
| [`imin:LevelType`](https://imin.co/LevelType) | `https://imin.co/IntermediateLevel` | Intermediate difficulty level |
