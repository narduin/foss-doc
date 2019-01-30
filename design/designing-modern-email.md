---
description: General guidelines and tips to design email in a modern 2019 way.
---

# Designing modern email

## Perspective

Keep in mind that every template file \(photoshop, sketch…\) will be converted into code at some point.  
This guide aims at sharing good practices while designing email templates and preserving mental health among developers.

{% hint style="info" %}
I use both Photoshop and Sketch to design emails.  They're both ok.

I also use the [MJML framework](https://mjml.io) to develop emails because no one should have to do it by hand nowadays… ever again.
{% endhint %}

## General knowledge

Email is one of the least advanced type of internet content. It is still being developed with `table` elements and the **huge diversity** of email clients make it almost impossible to achieve 100% compatibility.

{% hint style="info" %}
I am aiming for the maximum email clients compatibility possible so I won't be using stuff like  `media-queries` as they are not supported by all clients.
{% endhint %}

### Responsiveness

Emails can be responsive but we have very little control over it.  
As email usually are up to 800px wide, there are only two versions: one desktop and one mobile.  
Thus, what you see on one version will be identical in the other.

For example, if you align an image to the right-hand side on desktop because of a two columns layout, the image will stay right-aligned on the one column mobile version.  
**Which can be weird :**

![desktop 2 columns - image align : right - text align : left](../.gitbook/assets/desktop.jpg)

![mobile 1 column - image align : right - text align : left](../.gitbook/assets/mobile.jpg)

{% hint style="info" %}
When designing anything, we tend to think mobile first. Email, for once, follows the trend!
{% endhint %}

### Images

Images are handsomely used in emails. Sometimes too much. In order to be the most readable & accessible possible, avoid putting text on an image. If you have to, don't put a key information on an image. If the client blocks images \(by default on a lot of clients\) your email won't contain the necessary data to be relevant.

If you want to use a drop shadow, be sure to design it **inside** your margins.

![case 1 the shadow bleeds outside of the content-area - case 2 is ok.](../.gitbook/assets/shadow-mobile.jpg)

