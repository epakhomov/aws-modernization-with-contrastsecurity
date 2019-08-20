+++
title = "How to discover a new vulnerability"
chapter = false
weight = 4
+++

In this part we will discover a new vulnerability in Webgoat application and examine the finding in Contrast Security.

It is important to reiterate that Contrast Security identifies vulnerabilities by looking at the normal traffic that goes through the aplication. With that in mind, let's identify a SQL injection in Webgoat with Contrast.

1. Log to Webgoat and navigate to Injection Flaws --> String SQL injection. Then please enter Smith or any other string into the field and click on Go button:

{{< figure src="/images/wg_1.png" width="1000" height="500">}}

2. Now let's go back to Contrast Security and click on Vulnerabilities. As you can see Contrast identified to new vulnerabilites: XSS and SQL injection. 

{{< figure src="/images/ce_4.png" width="1000" height="500">}}

Now you can click on either vulnerabilities to get more information.