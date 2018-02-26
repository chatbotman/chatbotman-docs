title: Trigger Event
---

## What is Trigger Event?

Trigger event is a Chatbotman built-in function that let you trigger Dialogflow intents by outputting an event. It allows you to achieve the following purposes:

1. When you want to say something after the conversation end.
2. When you want to add promotional message after replying the subscribe.

## How to use it?

You need to output an action named `Chatbotman_TriggerEvent`. Chatbotman will detect this action name and trigger an event for you.

Here is an example intent of trigger event.

First, create an intent that output `Chatbotman_TriggerEvent` action and output a parameter called `eventName` with value `PromotionalMessage`
![](/images/advance_usage/trigger_event_step01.png)

Second, create an intent that accept `PromotionalMessage` event.
![](/images/advance_usage/trigger_event_step02.png)

This is the result.
![](/images/advance_usage/trigger_event_step03.png)
