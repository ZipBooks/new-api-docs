# Index Invoice



## Request

`GET https://api.zipbooks.com/v2/invoices`

## Response

- **Status:** 200 OK
- **Body:**

```json
{
  "data": [
    {
      "attributes": {
        "accept-credit-cards": "boolean",
        "accept-paypal": "boolean",
        "archived-at": null,
        "created-at": "datetime",
        "currency-code": "string",
        "date": "string",
        "days-outstanding": null,
        "due-date": "string",
        "external-id": "string",
        "google-drive-id": "string",
        "notes": "string",
        "number": "string",
        "paid-total": "string",
        "po-number": "string",
        "sent-date": null,
        "status": "string",
        "terms": "string",
        "title": "string",
        "total": "string",
        "updated-at": "datetime"
      },
      "id": "538",
      "relationships": {
        "account": {
          "data": {
            "id": "1492",
            "type": "account"
          }
        },
        "contact": {
          "data": {
            "id": "885",
            "type": "contact"
          }
        },
        "estimate": {
          "data": null
        },
        "line-items": {
          "data": [
            {
              "id": "1199",
              "type": "line-item"
            },
            {
              "id": "1198",
              "type": "line-item"
            }
          ]
        },
        "logo-cloud-file": {
          "data": {
            "id": "3599",
            "type": "cloud-file"
          }
        },
        "recurring-profile": {
          "data": null
        }
      },
      "type": "invoice"
    }
  ],
  "included": [
    {
      "attributes": {
        "address-1": "string",
        "address-2": "string",
        "allow-review-invites": "boolean",
        "archived-at": null,
        "city": "string",
        "country": "string",
        "created-at": "datetime",
        "department": "string",
        "display-name": "string",
        "email": "string",
        "expenses": "string",
        "first-name": "string",
        "industry": "string",
        "is-1099-required": "boolean",
        "is-visible": "boolean",
        "last-name": "string",
        "name": "string",
        "notes": "string",
        "phone": "string",
        "postal-code": "string",
        "revenue": "string",
        "state": "string",
        "suggested-next-estimate-number": "string",
        "suggested-next-invoice-number": "string",
        "unbilled-journal-entry-lines": "boolean",
        "unbilled-time-entries": "boolean",
        "updated-at": "datetime",
        "website": "string"
      },
      "id": "885",
      "relationships": {
        "account": {
          "data": {
            "id": "1492",
            "type": "account"
          }
        },
        "estimates": {},
        "integration-object": {},
        "invoices": {},
        "payment-bank-accounts": {
          "data": []
        },
        "people": {},
        "projects": {},
        "public-profile": {},
        "recurring-profiles": {},
        "time-entries": {}
      },
      "type": "contact"
    },
    {
      "attributes": {
        "created-at": "datetime",
        "discount": "string",
        "end-date": "string",
        "name": "string",
        "notes": "string",
        "order": "integer",
        "quantity": "string",
        "rate": "string",
        "start-date": "string",
        "taxes": [],
        "type": "Eum laudantium harum culpa.",
        "updated-at": "datetime"
      },
      "id": "1198",
      "relationships": {
        "chart-account": {
          "data": null
        },
        "line-itemable": {
          "data": {
            "id": "538",
            "type": "invoice"
          }
        }
      },
      "type": "line-item"
    },
    {
      "attributes": {
        "created-at": "datetime",
        "discount": "string",
        "end-date": "string",
        "name": "string",
        "notes": "string",
        "order": "integer",
        "quantity": "string",
        "rate": "string",
        "start-date": "string",
        "taxes": [],
        "type": "Id.",
        "updated-at": "datetime"
      },
      "id": "1199",
      "relationships": {
        "chart-account": {
          "data": null
        },
        "line-itemable": {
          "data": {
            "id": "538",
            "type": "invoice"
          }
        }
      },
      "type": "line-item"
    },
    {
      "attributes": {
        "category": null,
        "content-type": "string",
        "created-at": "datetime",
        "download-url": "string",
        "filename": "string",
        "height": "integer",
        "is-explicit": "boolean",
        "is-uploaded": "boolean",
        "size": null,
        "token": "string",
        "updated-at": "datetime",
        "width": "integer"
      },
      "id": "3599",
      "type": "cloud-file"
    }
  ],
  "jsonapi": {
    "version": "string"
  },
  "links": {
    "self": "string"
  },
  "meta": {
    "from": "integer",
    "to": "integer",
    "total": "integer",
    "unfiltered-total": "integer"
  }
}
```

## Example

```bash
curl -X GET \
     
     -H 'accept: application/vnd.api+json' \
     
     -H 'content-type: application/vnd.api+json' \
     
     -H 'authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJjYWxsZXIiOm51bGwsInN1YiI6IjEyNzAiLCJpc3MiOiJodHRwczpcL1wvYXBwLnppcGJvb2tzLmNvbVwvdjJcL2F1dGhcL2xvZ2luIiwiaWF0IjoxNTY3NTM1OTM4LCJleHAiOjE1ODMwODc5MzgsIm5iZiI6MTU2NzUzNTkzOCwianRpIjoiODlkZTA0NDItODUwZC00ZTI3LTk3ZGQtMjYwNmJlMWQ4ZjZmIiwic3RlYWx0aCI6ImZhbHNlIiwiYWNjb3VudF9pZCI6MTQ5MiwidXBkYXRlZF9hdCI6IjIwMTktMDktMDMgMTg6Mzg6NThaIn0.-IW5mOVV42aQZ2Drj-jafVEQCIHTCFnvuF2pPZXpKTI' \
     
     "https://api.zipbooks.com/v2/invoices"
```
