---
layout: post
title: Creating a dashboard with NagiosTV and Livesocket
---

Hey all. I was tasked with setting up a new NagiosXI instance and we needed a dashboard for the office. I found one, NagiosTV, which is super clean and easy to use. The only problem I ran into was creating a dashboard that was able to be accessed without credentials. I ended up using MK Livestatus to fetch the data to display on our big screen.

I'll show you how to do this here, just because it took a bit to get it figured out. But first, some credits:

<a href="https://nagiostv.com/">NagiosTV</a> Created and maintained by chriscareycode on github.

Livestatus now resides with CheckMK, I'll post the specific download link.
<a href="https://docs.checkmk.com/latest/en/intro.html">CheckMK</a>
<b>Note:</b> I don't believe they are releasing any more version of Livestatus. The last version I see is 1.5.0p24. Newer releases only offer Checkmk with OMD.


<a href="https://download.checkmk.com/checkmk/1.5.0p24/mk-livestatus-1.5.0p24.tar.gz">

Let's begin

First you'll need to download the tar file from above.

```bash
$ wget https://download.checkmk.com/checkmk/1.5.0p24/mk-livestatus-1.5.0p24.tar.gz
```
