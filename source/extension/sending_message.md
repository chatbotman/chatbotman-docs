title: Sending message to subscriber by using extension access token
---

In order to optimize the traffic, we provide an endpoint for you to send message to your subscriber. 
To access the endpoint, you need to provide the extension access token. 

Here is an example request.
```
curl -X POST \
  https://int.chatbotman.com/api/facebookApi/sendMessage \
  -H 'Cache-Control: no-cache' \
  -H 'Content-Type: application/json' \
  -d '{
	"pageId": "<PAGE_ID>",
	"moduleAccessToken": "<YOUR_ACCESS_TOKEN>",
	"messages": [{
        "sender": {
            "id": "246969682484713"
        },
        "recipient": {
            "id": "<PAGE_ID>"
        },
        "message": {
            "text": "Hello World"
        }
    }]
}'
```
If you want to send with other message tempalte, you may refers to the [documentation of facebook](https://developers.facebook.com/docs/messenger-platform/send-messages/templates).