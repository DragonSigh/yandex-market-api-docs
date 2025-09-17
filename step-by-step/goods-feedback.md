---
title: Product Reviews | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/goods-feedback
crawled_at: 2025-09-17T14:46:39.287852
---

Get product reviews
# Product Reviews
  * [Get product reviews](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#all-feedbacks)
  * [Get feedback that needs to be answered](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#need-reaction-feedbacks)
  * [Get product comments](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#all-comments)
  * [Send a response to the review](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#feedback-answer)
  * [Send a reply to a parent's comment](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#comment-answer)
  * [Edit your comment](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#edit)
  * [Skip reactions to reviews](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#skip-answer)
  * [Delete your comment](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#delete)


The Yandex.Market API allows you to receive product reviews and comments on them, as well as add, edit, and delete store comments.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#all-feedbacks)Get product reviews
Enable API notifications
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when there is a new review.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
Yandex MarketYour storeYandex MarketYour storeReceiving seller product reviewsAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller product reviews.
Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
The results are returned page by page, one page contains no more than 50 reviews.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#need-reaction-feedbacks)Get feedback that needs to be answered
Yandex MarketYour storeYandex MarketYour storeReceiving reviews that require a responsealt[Respond to review][Decline to respond to reviews]Account IDand NEED_REACTION value in the reactionStatus parameterPOST v2/businesses/{businessId}/goods-feedbackOK: reviews that require a response.Review ID and response textPOST v2/businesses/{businessId}/goods-feedback/comments/updateAddsa comment to the review.OK: information about the added comment.Review IDPOST v2/businesses/{businessId}/goods-feedback/skip-reactionRemoves the NEED_REACTION statusfrom the review.OK
Get the feedback you need to respond to with a request [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks), where pass the value `NEED_REACTION` in the parameter `reactionStatus`.
Status `NEED_REACTION` It is removed after you respond to the review or skip it. If the author changes the review, the status `NEED_REACTION` it will appear again.
To leave a comment, send the ID of the review to be replied to and the text of the response in the request. [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment).
If you don't want to respond to the review, skip it and pass the review ID in the request. [POST v2/businesses/{businessId}/goods-feedback/skip-reaction](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/skipGoodsFeedbacksReaction).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#all-comments)Get product comments
Enable API notifications
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when a new comment appears.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
If you already know the review IDs, skip the step of getting them.
Yandex MarketYour storeYandex MarketYour storeReceiving seller product reviewsRetrieving review commentsAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller product reviews.Review IDPOST v2/businesses/{businessId}/goods-feedback/commentsOK: review comments.
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Pass the review ID in the request. [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbackComments) to see the comments on this review.


The results are returned page by page, one page contains no more than 50 comments.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#feedback-answer)Send a response to the review
If you already know the review IDs, skip the step of getting them.
Yandex MarketYour storeYandex MarketYour storeReceiving product reviews for the sellerResponding to a reviewAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller's product reviews.Review ID and response textPOST v2/businesses/{businessId}/goods-feedback/comments/updateAddscomment to the review.OK: information about the added comment.
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Send the ID of the review to be responded to and the text of the response in the request. [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#comment-answer)Send a reply to a parent's comment
If you already know the IDs of the reviews and comments on the review, skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeReceiving product reviews from the sellerRetrieving review commentsResponding to a commentAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller's product reviews.Review IDPOST v2/businesses/{businessId}/goods-feedback/commentsOK: review comments.Parent comment ID and response textPOST v2/businesses/{businessId}/goods-feedback/comments/updateAddscomment.OK: information about the added comment.
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Pass the review ID in the request. [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbackComments) to see the comments on this review.
  3. Send the ID of the parent comment to respond to and the text of the response in the request. [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#edit)Edit your comment
Is it possible to change the comment?
Parameter `canModify` in the request [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment) indicates whether the seller can change the comments.
If you already know the IDs of the reviews and comments on the review, skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeReceiving product reviews from the sellerGetting comment IDEditing a commentAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller's product reviews.Review IDPOST v2/businesses/{businessId}/goods-feedback/commentsOK: comment ID.Comment ID and new textPOST v2/businesses/{businessId}/goods-feedback/comments/updateUpdatesthe comment.OK: information about the updated comment.
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Pass the review ID in the request. [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbackComments) to find out the ID of the comment that needs to be changed.
  3. Send the ID of this comment and the new text in the request. [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#skip-answer)Skip reactions to reviews
The transmitted reviews have the parameter `needReaction` will take the value `false` in the method of getting all the reviews [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
If you already know the review IDs, skip the step of getting them.
Yandex MarketYour storeYandex MarketYour storeReceiving product reviews for the sellerSkipping response to reviewsAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller's product reviews.Review IDsPOST v2/businesses/{businessId}/goods-feedback/skip-reactionUpdates the needReaction parameter to false.OK
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Pass the IDs of the reviews you don't want to respond to in the request. [POST v2/businesses/{businessId}/goods-feedback/skip-reaction](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/skipGoodsFeedbacksReaction).


If the author changes the review, the status `NEED_REACTION` it will appear again.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback#delete)Delete your comment
Can I delete a comment?
Parameter `canModify` in the request [POST v2/businesses/{businessId}/goods-feedback/comments/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/updateGoodsFeedbackComment) indicates whether the seller can delete comments.
If you already know the IDs of the reviews and comments on the review, skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeReceiving seller product reviewsGetting comment IDDeleting a commentAccount IDPOST v2/businesses/{businessId}/goods-feedbackOK: seller product reviews.Review IDPOST v2/businesses/{businessId}/goods-feedback/commentsOK: comment ID.Comment IDPOST v2/businesses/{businessId}/goods-feedback/comments/deleteDeletescomment.OK
  1. Get feedback on the seller's products by requesting [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbacks).
  2. Pass the review ID in the request. [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/getGoodsFeedbackComments) to find out the ID of the comment to delete.
  3. Pass the ID of this comment in the request. [POST v2/businesses/{businessId}/goods-feedback/comments/delete](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/goods-feedback/deleteGoodsFeedbackComment).


Copied
### Was the article helpful?
YesNo
Previous
[Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports)
Next
[Sales Boost](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost)
