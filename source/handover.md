title: Handover to Page Inbox App
---

Sometimes you may want to pass the conversation from a bot to a live agent for various reasons. Chatbotman has built-in support for passing the conversation to Facebook Page Inbox App.

Facebook supports [passing the thread control](https://developers.facebook.com/docs/messenger-platform/reference/handover-protocol/pass-thread-control) of a primary receiver to a secondary receiver.

### Setup

You need to manually configure Chatbotman as the primary receiver.

Go to your page -> Settings -> Messenger Platform. Choose Chatbotman as the "Primary Receiver" and Page Inbox as "Secondary Receiver"

![](/images/handover/page_settings.png)


### Pass control to Page Inbox

You can pass the control to Page Inbox App by specifying the action of the intent as `Chatbotman_PassThreadControl`. Any intent configured with action `Chatbotman_PassThreadControl` will pass the current thread control to Page Inbox App

![](/images/handover/pass_thread_control_intent.png)


### Pass control back to Chatbotman

Once your agent is finished with the customer in the Page Inbox App, they simply just click the "Mark as Done" button in the Page Inbox App. The conversation thread will be moved to the Done folder and the  control will be passed back to Chatbotman.

![](/images/handover/mark_as_done.png)
