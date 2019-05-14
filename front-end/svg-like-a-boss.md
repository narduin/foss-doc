---
description: How to clean your .svg files.
---

# SVG like a boss

## SVG is life

Using vector images on the web is the best feeling ever. Beeing able to scale up or down a logo without quality loss with files no more than 20ko is great.

However, let's do that properly. When exporting svg from illustrator or sketch, you get some useless code added to the file.

{% code-tabs %}
{% code-tabs-item title="Illustrator code" %}
```markup
<!-- Generator: Adobe Illustrator 23.0.3, SVG Export Plug-In . SVG Version: 6.00 Build 0)  -->​
```
{% endcode-tabs-item %}
{% endcode-tabs %}

## SVG is love

We have to take care of svg as much as we love it. So we have to clean all the useless bits of code inside it.

{% hint style="success" %}
A very nice developer built a tool that does exactly that: [**SVGOMG**](https://jakearchibald.github.io/svgomg/)\*\*\*\*
{% endhint %}

**Svgomg** has a lot of options, so trust me and use them like follows :

![svgomg settings-1](../.gitbook/assets/1.jpg)

![svgomg settings-2](../.gitbook/assets/2.jpg)

## Example

Let's see for ourselves how this tool affects the following svg code.





