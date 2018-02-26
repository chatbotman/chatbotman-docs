title: Label User
---

Sometime you may want to put an identifier to your user when he/she is talking to your bot. For example, when a user express interest to a particular product or service that you are offering, you may want to label this user automatically. Chatbotman has out-of-box function to support this use case. To do that, simply use the built-in action `Chatbotman_labelUser`

## Setup

Chatbotman can help you label a user when a particular intent is triggered. When the intent is triggered, use `Chatbotman_labelUser` as the action of the intent. In addition, provide a parameter called "label" and the value could be anything you would like.

![](/images/advance_usage/label_user/configure_action.png)


## Use the label

After the users are labelled, you can use this label when creating a campaign to send broadcast message to this specific group of users.

![](/images/advance_usage/label_user/use_the_label.png)
