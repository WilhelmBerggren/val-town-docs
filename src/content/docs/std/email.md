---
title: Email
---

`std/email` lets you send emails from Val town. You can send emails to yourself, only - unless you have Val Town Pro, in which case you can send emails to anyone.

:::note
Want to receive emails instead? [Create an email handler val](/types/email/)
:::

## Basic usage

```ts val
import { email } from "https://esm.town/v/std/email";

await email({ text: "emails emails emails!" });
```

## `to`, `cc`, and `bcc`

By default, the `to` field is set to the owner of the Val Town account that calls it.

If you have Val Town Pro, you can send emails to anyone via the `to`, `cc`, and `bcc` fields.

If you don't have Val Town Pro, you can only send emails to yourself, so leave those fields blank.

## `from`

The `from` is limited to a few options:

1. It defaults to `notifications@val.town` if you don't specify it.

2. If you do specify it, it must be of the form: `your_username.valname@valtown.email`.

## Attachments

You can attach files to your emails by using the `attachments` field.

```ts val
import { email } from "https://esm.town/v/std/email";

export const stdEmailAttachmentExample = email({
  attachments: [
    {
      content: btoa("hello attachments!"),
      filename: "test.txt",
      type: "text",
      disposition: "attachment",
    },
  ],
});
```

Here's an example sending a [PDF](https://www.val.town/v/stevekrouse/sendPDF2).
