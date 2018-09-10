# imin Model Extension Namespace

This repository holds the JSON-LD definition of the imin namespace. The terms in this namespace are defined for use within the [imin Search API](https://docs.imin.co).

imin works as part of the [OpenActive Community Group](https://www.w3.org/community/openactive) to promote the usecases represented by the properties within this namespace, with the intention of standardising them over time.

## Extension Properties

| Property                   | Type    | Description                                                        |
|----------------------------|---------|--------------------------------------------------------------------|
| `imin:publicAdultPrice`    | decimal | The adult price derived from the appropriate Offer                 |
| `imin:publicJuniorPrice`   | decimal | The junior price derived from the appropriate Offer                |
| `imin:membershipRequired`  | boolean | Indicates whether this offer is only available to members.         |
| `imin:fullAddress`         | string  | Full address in one line                                           |
| `imin:specialRequirements` | Concept | List of related special requirements from a controlled vocabulary. |
