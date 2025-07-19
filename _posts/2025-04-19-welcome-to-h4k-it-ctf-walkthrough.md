---
title: "h4k-it CTF Walkthrough!"
date: 2025-07-18T15:34:30-04:00
categories:
  - blog
excerpt: "Writeup for the PHP-J4G challenge from h4k-it.com"
author_profile: true
toc: true
toc_label: "Steps"
toc_icon: "cogs"
categories:
  - CTF
  - Writeups
tags:
  - Web
  - PHP
  - CTF
  - h4k-it
  - Reverse Engineering
---

Hello! This is my write-up for the **PHP-J4G web challenge** from [h4k-it.com](https://h4k-it.com).

---

## Challenge Setup

We’ve been provided with an IP address and a port to access the challenge website.

---

## Step 1: Exploring the Site

After accessing the website, we’re greeted with a login page that requires a password.

![Login Page](/assets/images/pic1.png)

I attempted default credentials and random values, but none were successful.

---

## Step 2: Viewing the Source Code

I decided to view the page source and discovered some hex values embedded in the HTML.

![Hex Values](/assets/images/pic2.png)

---

## Step 3: Decoding the Hex

I copied the hex and decoded it using [CyberChef](https://gchq.github.io/CyberChef/), selecting the "From Hex" operation. This revealed a PHP script.

![CyberChef Output](/assets/images/pic3.png)

---

## Step 4: Analyzing the PHP Script

I examined the PHP script to identify any potential backdoors or useful logic.

Two inputs were suggested in the script: `"VAWULENCE"` and `"a"`.

- Trying `"VAWULENCE"` → no success.
- Trying `"a"` → **BOOM! Got the flag** 🎉

![Flag Reveal](/assets/images/pic4.png)

---

## 🏁 Flag

GoH{Wh47_Typ3_w45_th3_1nPu7_Ag41n?}

yaml
Copy
Edit

---

## Thank You

Challenge completed!  
Thanks to @Duncan for this one.
