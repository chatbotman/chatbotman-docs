title: Create a Private Reply
---
## What is private reply?
When someone read your post in your page and comment your post, the messenger pops up immediately and send a private message to this Facebook user. With the help of Chatbotman and Dialogflow, your chatbot can understand which post the follower is commenting and a correct event would be triggered in Dialogflow and therefore give a relevant response to the Facebook user.

In this tutorial, you will learn how to make a private reply for a specific post in your Facebook page.

## Step 1: Ensure the Facebook page is enabled for Chatbotman
Select your **Facebook page** on the top-left dropdown menu which you want to add a private reply for the post.

Go to **Settings > Facebook Page**, ensure the Facebook page has been enabled and with the Dialogflow developer access token configured. (See [Setup Your First Chatbot](setup.html) for details)

![](/screenshots/settings.png)

## Step 2: Find your Facebook post
To connect your Facebook post with your chatbot, simply find your post in **FB Posts** section and click **Connect with bot**. If you have just created a post and the post is not displayed, you can click **Refresh** button on the top right corner to refresh the post list.

![](/screenshots/fb-post-connect.png)

## Step 3: Click Connect with Bot
When you click **Connect with bot**, a pop-up **Bot Setup Introduction** dialog will tell you how to setup your bot with private reply. We recommend you to watch the video first.

![](/screenshots/fb-post-bot-setup-introduction.png)

{% note tip Take note of the name of the newly created intent %}
This steps will create an intent on your Dialogflow agent. Take note of the name and proceed to the next step.
{% endnote %}

## Step 4: Find the intent created in Dialogflow

A new intent will be created for each post when you click "Connect with Bot". This intent will be triggered whenever anyone comment on the post by triggering the event. You can go to Dialogflow Console to find the intent. Then, click the intent to edit the response.

![](/screenshots/dialogflow-intents.png)

## Step 5: Edit the intent with your custom response

After you found the intent, scroll to the bottom and click the **Facebook Messenger** tab. You will see a default **Text Response** for your intent. It means that when the Facebook user commented your Facebook post, the chatbot will respond to the Facebook user with this intent. Therefore, you can simply change the text response. Or, if you don't want a text response, you can click the **trash** button on the  **Text Response** section and add whatever you want by clicking the **Add Message Content** button.

Please remind to click the **Save** button on the top after you finished editing your intent.

![](/screenshots/dialogflow-edit-intent.png)

## Step 5: Test it
Finally, try to comment your post to see whether the chatbot will respond to you. If you do all the things correctly, you will see the chatbot response to you like this:

![](/screenshots/private-reply-test.png)
