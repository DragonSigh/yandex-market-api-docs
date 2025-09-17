---
title: Comments on the review - Product Reviews | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/getGoodsFeedbackComments
crawled_at: 2025-09-17T14:40:20.668339
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body1)
    * [GoodsFeedbackCommentListDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentlistdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype)
    * [GoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentdto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#forwardscrollingpagerdto)
    * [GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentstatustype)
    * [GoodsFeedbackCommentAuthorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthordto)
    * [GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthortype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body7)


# Getting comments on a review
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns comments to the review, except for:
  * those that were deleted by users or Yandex.Market.
  * comments on deleted reviews.


You can also set up API notifications.
Yandex.Market will send you [request](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/push-notifications/reference/sendNotification) when a new comment appears. And full information about it can be obtained using this method.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/push-notifications/)
The results are returned page by page, one page contains no more than 50 comments.
The comments are arranged in the order of publication, so you can send a specific page ID to `page_token` if you have received it before.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/goods-feedback/comments

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body)Body
application/json
```
{
    "feedbackId": 0,
    "commentIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
commentIds |  **Type:** integer<int64>[] Comment IDs. , Do not use this field at the same time as other filters. If you want to use them, leave the field empty.   
ID of the review comment. _Min items:_ `1` _Max items:_ `50` _Unique items_  
feedbackId |  **Type:** integer<int64> The review ID.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#200-ok)200 OK
The tree of comments on the review.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "comments": [
            {
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
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GoodsFeedbackCommentListDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentlistdto) Comments on the review.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentlistdto)GoodsFeedbackCommentListDTO
Comments on the review.
**Name** |  **Description**  
---|---  
comments* |  **Type:** [GoodsFeedbackCommentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentdto)[] A list of comments.  
Comment on the review.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentdto)GoodsFeedbackCommentDTO
Comment on the review.
**Name** |  **Description**  
---|---  
feedbackId* |  **Type:** integer<int64> The review ID.  
id* |  **Type:** integer<int64> ID of the review comment.  
status* |  **Type:** [GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentstatustype) Comment status:
  * `PUBLISHED` — published.
  * `UNMODERATED` — not verified.
  * `BANNED` — blocked.
  * `DELETED` — deleted.

_Enum:_ `PUBLISHED`, `UNMODERATED`, `BANNED`, `DELETED`  
text* |  **Type:** string The text of the comment. _Min length:_ `1` _Max length:_ `4096`  
author |  **Type:** [GoodsFeedbackCommentAuthorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthordto) Information about the comment's author.  
canModify |  **Type:** boolean Whether the seller can edit the comment or delete it.  
parentId |  **Type:** integer<int64> ID of the review comment.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentstatustype)GoodsFeedbackCommentStatusType
Comment status:
  * `PUBLISHED` — published.
  * `UNMODERATED` — not verified.
  * `BANNED` — blocked.
  * `DELETED` — deleted.

**Type** |  **Description**  
---|---  
[GoodsFeedbackCommentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentstatustype) |  _Enum:_ `PUBLISHED`, `UNMODERATED`, `BANNED`, `DELETED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthordto)GoodsFeedbackCommentAuthorDTO
Information about the comment's author.
**Name** |  **Description**  
---|---  
name |  **Type:** string The name of the author or the name of the cabinet.  
type |  **Type:** [GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthortype) Type of author:
  * `USER` — the user.
  * `BUSINESS` — an office.

_Enum:_ `USER`, `BUSINESS`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthortype)GoodsFeedbackCommentAuthorType
Type of author:
  * `USER` — the user.
  * `BUSINESS` — an office.

**Type** |  **Description**  
---|---  
[GoodsFeedbackCommentAuthorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#goodsfeedbackcommentauthortype) |  _Enum:_ `USER`, `BUSINESS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbackComments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "feedbackId": 0, "commentIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[All reviews](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/getGoodsFeedbacks)
Next
[Adding/changing a comment](https://yandex.ru/dev/market/partner-api/doc/en/reference/goods-feedback/en/reference/goods-feedback/updateGoodsFeedbackComment)
