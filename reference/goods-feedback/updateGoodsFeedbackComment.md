---
title: Adding/changing a comment - Product Reviews | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/updateGoodsFeedbackComment
crawled_at: 2025-09-17T14:40:26.601320
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body)
    * [UpdateGoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#updategoodsfeedbackcommentdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body1)
    * [GoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype)
    * [GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentstatustype)
    * [GoodsFeedbackCommentAuthorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthordto)
    * [GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthortype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body7)


# Adding a new or changing a created comment
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management


Adds a new store comment or modifies a comment that the store left earlier.
To create a comment on a review, send only the review ID. `feedbackId`.
To add a comment to another comment, send:
  * `feedbackId` — the review ID.
  * `comment.parentId` — ID of the parent comment.


To edit a comment, send:
  * `feedbackId`— the review ID.
  * `comment.id` — ID of the comment that needs to be changed.


If you transmit at the same time `comment.parentId` and `comment.id`, an existing comment will be changed.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/goods-feedback/comments/update

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body)Body
application/json
```
{
    "feedbackId": 0,
    "comment": {
        "id": 0,
        "parentId": 0,
        "text": "string"
    }
}

```

**Name** |  **Description**  
---|---  
comment* |  **Type:** [UpdateGoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#updategoodsfeedbackcommentdto) Comment parameters.  
feedbackId* |  **Type:** integer<int64> The review ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#updategoodsfeedbackcommentdto)UpdateGoodsFeedbackCommentDTO
A comment on a review or other comment.
**Name** |  **Description**  
---|---  
text* |  **Type:** string The text of the comment. _Min length:_ `1` _Max length:_ `4096`  
id |  **Type:** integer<int64> ID of the comment to edit. Leave the field empty if you want to add a new comment.  
parentId |  **Type:** integer<int64> ID of the parent comment to respond to.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#200-ok)200 OK
Information about the added or changed comment.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "id": 0,
        "text": "string",
        "canModify": false,
        "parentId": 0,
        "author": {
            "type": "USER",
            "name": "string"
        },
        "status": "PUBLISHED",
        "feedbackId": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentdto) Comment on the review.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentdto)GoodsFeedbackCommentDTO
Comment on the review.
**Name** |  **Description**  
---|---  
feedbackId* |  **Type:** integer<int64> The review ID.  
id* |  **Type:** integer<int64> ID of the review comment.  
status* |  **Type:** [GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentstatustype) Comment status:
  * `PUBLISHED` — published.
  * `UNMODERATED` — not verified.
  * `BANNED` — blocked.
  * `DELETED` — deleted.

_Enum:_ `PUBLISHED`, `UNMODERATED`, `BANNED`, `DELETED`  
text* |  **Type:** string The text of the comment. _Min length:_ `1` _Max length:_ `4096`  
author |  **Type:** [GoodsFeedbackCommentAuthorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthordto) Information about the comment's author.  
canModify |  **Type:** boolean Whether the seller can change the comment or delete it.  
parentId |  **Type:** integer<int64> ID of the review comment.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentstatustype)GoodsFeedbackCommentStatusType
Comment status:
  * `PUBLISHED` — published.
  * `UNMODERATED` — not verified.
  * `BANNED` — blocked.
  * `DELETED` — deleted.

**Type** |  **Description**  
---|---  
[GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentstatustype) |  _Enum:_ `PUBLISHED`, `UNMODERATED`, `BANNED`, `DELETED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthordto)GoodsFeedbackCommentAuthorDTO
Information about the comment's author.
**Name** |  **Description**  
---|---  
name |  **Type:** string The name of the author or the name of the cabinet.  
type |  **Type:** [GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthortype) Type of author:
  * `USER` — the user.
  * `BUSINESS` — an office.

_Enum:_ `USER`, `BUSINESS`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthortype)GoodsFeedbackCommentAuthorType
Type of author:
  * `USER` — the user.
  * `BUSINESS` — an office.

**Type** |  **Description**  
---|---  
[GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#goodsfeedbackcommentauthortype) |  _Enum:_ `USER`, `BUSINESS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body2)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body3)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body4)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body5)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body6)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#body7)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "feedbackId": 0, "comment": { "id": 0, "parentId": 0, "text": "string" } }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Comments on the review](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments)
Next
[Skipping reactions to reviews](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/skipGoodsFeedbacksReaction)
