# Communication

Adds a communication object to the tender or a lot to describe the modalities of communication about key events.

If you are using the [Lots extension](https://extensions.open-contracting.org/en/extensions/lots/master/), [follow its guidance](https://extensions.open-contracting.org/en/extensions/lots/master/#usage) on whether to use `tender.lots` fields or `tender` fields.

## Legal context

In the European Union, this extension's fields correspond to [eForms BT-124, BT-127, BT-631, BT-632 and BT-738](https://docs.ted.europa.eu/eforms/latest/reference/business-terms/). See [OCDS for the European Union](http://standard.open-contracting.org/profiles/eu/master/en/) for the correspondences to Tenders Electronic Daily (TED).

## Example

### Tender

An example of a planning notice from which a competition notice will follow.

```json
{
  "tender": {
    "communication": {
      "atypicalToolName": "ACertainTool",
      "atypicalToolUrl": "https://ecomm-procurement.example.net",
      "futureNoticeDate": "2020-06-17T00:00:00+01:00",
      "noticeRequestedPublicationDate": "2020-03-15T00:00:00+01:00",
      "documentAvailabilityPeriod": {
        "startDate": "2020-06-15T00:00:00+01:00",
        "endDate": "2020-07-10T00:00:00+01:00"
      }
    }
  }
}
```

### Lot

An example of a planning notice divided into lots which is also a call for competition.

```json
{
  "tender": {
    "lots": [
      {
        "id": "LOT-0001",
        "communication": {
          "atypicalToolName": "ACertainTool",
          "atypicalToolUrl": "https://ecomm-procurement.example.net",
          "noticeRequestedPublicationDate": "2020-03-15T00:00:00+01:00",
          "documentAvailabilityPeriod": {
            "startDate": "2020-06-15T00:00:00+01:00",
            "endDate": "2020-07-10T00:00:00+01:00"
          },
          "invitationToConfirmInterest": "2020-11-15T09:00:00+01:00"
        }
      }
    ]
  }
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.

## Changelog

### 2023-03-09

* Add `communication.invitationToConfirmInterest`, `communication.atypicalToolName`, `communication.noticeRequestedPublicationDate` and `Lot.communication`

### 2021-01-19

* Add `tender.communication.documentAvailabilityPeriod` field

### 2020-04-24

* Add `minProperties`, `minItems` and/or `minLength` properties.

This extension was originally discussed as part of the [OCDS for EU profile](https://github.com/open-contracting-extensions/european-union/issues) and in [pull requests](https://github.com/open-contracting-extensions/ocds_communication_extension/pulls?q=is%3Apr+is%3Aclosed).
