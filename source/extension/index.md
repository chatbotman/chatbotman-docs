title: Overview
---

Chatbotman allows you to integrate your external services by coding extensions. Whenever DialogFlow return an unhandled action, your extension will receive a callback. You can process that callback and then reply to your subscriber.

Here are some goals that can achieve by Chatbotman extension:
1. Response flight status to your subscriber
2. Make an appointment through chatbot
3. More...

## Getting Started

To create an extension, a Http Server that accept POST request is required in order to receive callbacks from Chatbotman.

The following guide will use aws lambda function to demonstrate how to create an extension to get current time.

#### 1. Clone the project.

`git clone --depth=1 https://github.com/chatbotman/demo-what-time-is-it.git`

#### 2. Install npm packages.

`cd demo-what-time-is-it && npm install`

#### 3. Install serverless-cli and aws-cli. You can find the guide [here](https://github.com/serverless/serverless/blob/master/README.md#quick-start).


#### 4. Copy and save your configuration.
![](/images/private_extension/extension_configuration.png)

#### 5. Put your secret and access token into src/config.ts or you can set the environment variable in AWS.
```TypeScript
export default {
    moduleAccessToken: process.env.MODULE_ACCESS_TOKEN, // modify here
    secret: process.env.MODULE_SECRET, // modify here
    chatbotmanUrl: "https://app.chatbotman.com/api/",
};
```

#### 6. Deploy your project to aws.

`sls deploy`

Output
```
Serverless: Bundling with Webpack...
...
endpoints:
  POST - https://_________.execute-api.us-east-1.amazonaws.com/dev/getCurrentTime << Your endpoint
functions:
  GetCurrentTime: demo-what-time-is-it-dev-GetCurrentTime
```

#### 7. Create an intent to trigger your module.
![](/images/private_extension/dialogflow_demo.png)
#### 8. What time is it?
![](/images/private_extension/chat_result.png)

## Example callback request body
```Typescript
interface RequestBody {
    dialogFlow: {
        action: string;
        parameters: {
            [key: string]: string | number;
        }
    },
    facebookPage: {
        pageId: string;
        name: string;
        pictureUrl: string;
    },
    facebookUser: {
        pageScopedId: string;
        name: string;
        preferredLanguage: string;
        firstName?: string;
        lastName?: string;
        gender?: string;
        timezone?: string;
        subscribed: boolean;
        profilePic?: string;
        locale?: string;
    }
}
```

## Examples & Demo

1. [Search Flight Status (Mehri Bacem)](https://github.com/MehriBacem/ChatbotExtension)
2. [Get Current Time (Kencckw)](https://github.com/chatbotman/extension-what-time-is-it)


