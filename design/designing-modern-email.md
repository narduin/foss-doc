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
I am aiming at the maximum email clients compatibility possible so I won't be using stuff like  `media-queries` as they are not supported by all clients.
{% endhint %}

Emails can be responsive but we have very little control over it.  
As email usually are up to 800px wide, there are only two versions: one desktop and one mobile.  
Thus, what you see on one version will be identical in the other.

For example, if you align an image to the left-hand side on desktop because of a two column layout, the image will stay left aligned on the one column mobile version. Which can be weird.

| \[image\] | Some text |
| :--- | :--- |




