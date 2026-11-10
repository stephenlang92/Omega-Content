---
title: "TikTok Events API – a complete install guide for Shopify stores [2026]"
slug: "set-up-tiktok-pixels-to-track-events-with-events-api-server-side-tracking-for-tiktok-ads"
source_url: "https://www.omegatheme.com/blogs/set-up-tiktok-pixels-to-track-events-with-events-api-server-side-tracking-for-tiktok-ads"
published_date: "2022-03-16T09:49:00.000Z"
category: "TikTok Advertising"
author: "Tristan Do"
thumbnail: "https://strapi.omegatheme.com/uploads/Tik_Tok_event_api_cb00a862d5.jpg"
meta_description: "This article explains why not carefully choosing your TikTok pixel installation & event setup option could be a costly decision."
---

# TikTok Events API – a complete install guide for Shopify stores [2026]

> **Source:** [https://www.omegatheme.com/blogs/set-up-tiktok-pixels-to-track-events-with-events-api-server-side-tracking-for-tiktok-ads](https://www.omegatheme.com/blogs/set-up-tiktok-pixels-to-track-events-with-events-api-server-side-tracking-for-tiktok-ads)  
> **Category:** TikTok Advertising | **Author:** Tristan Do | **Published:** 2022-03-16T09:49:00.000Z

![Featured Image](https://strapi.omegatheme.com/uploads/Tik_Tok_event_api_cb00a862d5.jpg)

## Meta Description
This article explains why not carefully choosing your TikTok pixel installation & event setup option could be a costly decision.

---

![](https://strapi.omegatheme.com/uploads/Tik_Tok_event_api_cb00a862d5.jpg)

This article explains why not carefully choosing your TikTok pixel installation & event setup option could be a costly decision.

Alright, it’s tempting to gravitate towards the easy way prebuilt and laid out. For some, installing it through Shopify is the best choice as you don’t have to define events yourself in the TikTok Event Manager.

![](https://strapi.omegatheme.com/uploads/tiktok_shopify_method_3918933d6c.png)

For many others, manually installing the pixel with a standard event setup method would be a go-to. TikTok advises you, advertisers, to choose this anyway.

![](https://strapi.omegatheme.com/uploads/manual_dc91c5e47e.png)

![](https://strapi.omegatheme.com/uploads/dev_mode_tiktok_pixel_f8ad75c0ce.png)

Both ways seem completely solve your humble needs for tracking. Until you find out these options and **modes can’t be changed later on.**

## Why would I even want to change the way my pixels are set up?

4 percent. That’s how many [iOS users in the U.S.](https://sea.mashable.com/tech/15641/after-update-only-4-percent-of-ios-users-in-us-let-apps-track-them) let apps track them. Google also planned to phase out third-party cookies by the end of 2023. Imagine the cookie-less world we’re entering.

*Do the below scenarios seem familiar to you?*

- Shopify orders recorded X but your TikTok Pixel only got half the purchases
- Your cost per action is flying blind as a result of a low-quality lookalike audience, which stemmed from an insufficient view custom audience
- You found your hands tied when it comes to tracking custom events (like form submission or page scrolling) and retargeting to these high-intent prospects.
- ROAS doesn’t show up as you don’t know how to attach price and order value parameters to your purchase events.

If you’re not aiming to make ads decision on a severely eclipsed view of data, you might want to switch your TikTok tracking server-side.

## Enter the TikTok Event API solution

Think of it like this:

While the browser-side TikTok pixel can easily fail you when it’s blocked, TikTok Event API stays. And do all the tracking server-side. Each and every event your visitors take on your take can be tracked, logged into a server, and send directly to the TikTok server.

That means:

- **Take back all the would-have-been-miss events:** From *page view, product details page view, add to cart, initiate checkout to complete payment*, all can be recorded and sent to your TikTok Event Manager despite browsers block, across devices with custom event code.
- **Reduce your cost with a more accurate advanced matching**Say you want to run Dynamic Product Ads (DPA) retargeting to TikTok users who have purchased from your website once, of course, you have to first start with a custom audience based on the actions/events people took on your web. This is where reliable capturing of customer data comes in. To improve the matching quality, it’s best that you could capture *phone number, email, click ID, IP, user agent, and external ID if applicable.*Then you would want to send those events safely to TikTok by **hashing them**. This is so that TikTok is not able to identify customers who are not TikTok users while still able to find the match.

![](https://strapi.omegatheme.com/uploads/custom_audience_tiktok_ads_b53286f0c7.png)

- **Expand your audience in an accurate way:** If you would like to expand your audience using a lookalike of people who have taken action on your web (not necessarily a purchase and not necessarily attributed events), advanced matching and sufficient event collection is also a must.

In short, only when you can ensure **accurate, sufficient data collection and data sharing** will you be able to guide TikTok to a more optimized target and spending.

**But here’s the catch:**

*One*, you can only send the advanced matching parameters together with events if your pixel was created through **Developer Mode.**

*Two*, you can only ensure the full-funnel view of your event data if tracking server-side through the **Event API is enabled.**

Thinking about switching mode now? It’s too late. As said above, you cannot change modes. At least for the moment, that’s not an option TikTok allows. What do you do now?

Create new pixels. Use the developer mode, custom your event code to capture events, have a server to store them, and send them to TikTok without the need for browsers.

*Now you might be thinking:*

## TikTok Event API is too technical for me

“Isn’t that too much work to do?” You’re right. These are often developers’ responsibilities as so many technical resources are involved.

The good news is there’s an app that’s designed the exact tasks, applicable for both [Shopify](https://apps.shopify.com/tiktok-multi-pixels?surface_detail=article_id_433&surface_type=omega_blog) and [Wix](https://www.wix.com/app-market/tiktok-shop-connector-by-omega). All you need to do is create the pixels, copy the pixel IDs, generate access tokens, and follow several copies and pastes. Server-side tracking for TikTok is just several clicks away.

## Do I even need to install multiple TikTok pixels?

“It’s nice with the TikTok Event API but isn’t it redundant as I’ve already had a pixel? I can’t get rid of my first pixel anyway now that it got so much data”.

Ideally, advertisers should be able to enable the browser-side pixel to work alongside the Event API so you won’t need to create a new pixel ID just for the sake of developer mode. Both streams of data should arrive and be deduplicated in the Event Manager (exactly what Facebook allows advertisers to do, with supporting apps like [Facebook Multi Pixels](https://apps.shopify.com/facebook-multi-pixels?surface_detail=article_id_433&surface_type=omega_blog)). This, unfortunately, is not an available option in TikTok yet.

However, it’s still worth it to create another pixel alongside as a **backup or preparation.** With more conversions collected, TikTok will get better at delivering your ads to people who are more likely to take certain actions. You don’t want to miss out on chances to create high-quality custom audiences with data collected through the Event API. And note that **a pixel must have at least 1000 conversion events** before you can create a custom audience out of it.

### Set up ttclid

ttclid helps you to match users and attribute event to your TikTok ads accurately. It is strongly encouraged to set up ttclid to improve your ads performance.

Refer document [here.](https://ads.tiktok.com/marketing_api/docs?rid=4eezrhr6lg4&id=1701890980108353)

**Result:**

`https://ads.tiktok.com/marketing_api/docs?rid=4eezrhr6lg4&id=1701890980108353`

Copy
