title: Protect your endpoint
---

To protect your endpoint, you need to define you extension secret in Chatbotman interface.
![](/images/private_extension/extension_configuration.png)

Then, you need to verify the "x-hub-signature" header. Here is an example function that verify x-hub-signature.
```Typescript
import * as crypto from 'crypto';
export const verifyXHubChallenge = (challenge: string, body: string, secret: string) => {
    return ("sha1=" + crypto.createHmac("sha1", secret).update(body, "utf8").digest("hex")) === challenge;
};
```
