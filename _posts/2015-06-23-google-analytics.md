---
layout: post
title: "Landing Page Guide 7: Understanding Your Traffic"
tags: landing_page_guide
---

After you've started promoting your awesome product to people, they'll start visiting your website. It would be helpful if we could find out how many people are coming to your website and see what the percentage of people who sign up for your mailing list is. 

In order to do this, we're going to use Google Analytics. It can also tell you where the majority of your traffic is coming from, so you can focus your efforts in the place that gives you the most bang for your buck.

## Setting Up Google Analytics

1. In Google Analytics, click **Admin**. 
![Google Analytics Main](/assets/analytics-main.png)
2. Create a new property to track.
![Google Analytics Admin](/assets/analytics-admin.png)
3. Complete the new property creation form.
![Google Analytics New](/assets/analytics-new.png)
4. After setting up a new property, you'll receive a tracking code.
![Google Analytics Tracking](/assets/analytics-tracking.png)
Paste the Google Analytics code between the `<head>...</head>` tags in your website for every page that you want to track. 
{% highlight html %}
<head>
	...
	<script>
	    (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	    m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	    })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

	    ga('create', 'UA-00000000-1', 'auto');
	    ga('send', 'pageview');
	</script>  
</head>
{% endhighlight %}
5. asdsa

## Check If It's Working

After you've pasted the code into your website, we should check to make sure that the site is being tracked properly.

### Real Time

1. Navigate to your website.
2. In another tab or browser window, go to Google Analytics and click on the **Real-Time** button on the sidebar. You should be able to see your visit to on your website show up as an active user.

> #### I'm on my website, but Google Analytics doesn't show it!
Do you have a Javascript blocker installed? Either disable it for now or add your website to the whitelist. I often forget to do this and I get mad when my visits don't show up during testing.

### Tracking Status

You can also check the status of the website, by going to **Admin > Tracking Info > Tracking Code**. 
![Google Analytics Admin Tracking](/assets/analytics-admin-tracking.png)

At the top of the page, you can see the current status of the tracking code. If it says **Receiving Data**, your analytics should be running. Don't worry if it doesn't, as the updates to this status can take up to 24 hrs to take effect.
