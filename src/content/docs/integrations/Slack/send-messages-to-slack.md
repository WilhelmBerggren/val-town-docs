---
title: Send messages to Slack
generated: 1701279907862

---

You can send messages to Slack from vals.

In this guide you’ll create an incoming webhook for your Slack workspace, and send a request to it with a message payload.

![Screenshot 2023-06-27 at 07.09.52.png](./send-messages-to-slack/screenshot_2023-06-27_at_070952.png)

# 1. Create a Slack app

Visit [https://api.slack.com/apps?new\_app=1](https://api.slack.com/apps?new_app=1), create a new app **From Scratch**, and choose your **App Name** and your workspace.

![Screenshot 2023-06-27 at 07.05.40.png](./send-messages-to-slack/screenshot_2023-06-27_at_070540.png)

# 2. Go to the incoming webhooks page

On the next page (or in the side bar), click **Incoming Webhooks**.

![Screenshot 2023-06-26 at 21.30.46.png](./send-messages-to-slack/screenshot_2023-06-26_at_213046.png)

# 3. Create an incoming webhook

Click the **Activate Incoming Webhooks** toggle.

![Screenshot 2023-06-26 at 21.31.07.png](./send-messages-to-slack/screenshot_2023-06-26_at_213107.png)

Scroll down, and click **Add New Webhook to Workspace**.

![Screenshot 2023-06-26 at 21.31.18.png](./send-messages-to-slack/screenshot_2023-06-26_at_213118.png)

Select the channel which the webhook will send messages to.

![Screenshot 2023-06-27 at 07.04.24.png](./send-messages-to-slack/screenshot_2023-06-27_at_070424.png)

# 4. Save the webhook address as a secret

You’ll be taken back to the ****Incoming Webhooks**** page (if not, you can find it via the side bar).

![Screenshot 2023-06-26 at 21.33.04.png](./send-messages-to-slack/screenshot_2023-06-26_at_213304.png)

Copy the **Webhook URL** for the webhook you just created and save it as a [Val Town secret](https://www.val.town/settings/secrets) as `slackWebhookURL`.

# 5. Use `[fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)` to send a message

Translate the sample cURL request to a `[fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)` request. You can copy and paste the following val.

<div class="not-content">
  <iframe src="https://www.val.town/embed/vtdocs.slackWebHookMessageExample" width="100%" frameborder="no" style="height: 400px;">
    &#x20;
  </iframe>
</div>

If it worked, you will get a message in the channel you configured earlier!

![Screenshot 2023-06-27 at 07.09.52.png](./send-messages-to-slack/screenshot_2023-06-27_at_070952-1.png)

Ran into a problem? Get help on the [Val Town Discord](https://discord.gg/dHv45uN5RY).