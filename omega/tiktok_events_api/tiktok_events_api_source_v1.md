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

In 2026, relying solely on browser-based tracking can quietly drain your ad budget—costing Shopify merchants up to 30%–50% of their conversion signals due to iOS privacy restrictions, Safari ITP, and aggressive ad blockers. This article explains why not carefully choosing your TikTok pixel installation & event setup option could be a costly decision, and why the **TikTok Events API** has become an essential server-side tracking lifeline for modern eCommerce stores.

Alright, it’s tempting to gravitate towards the easy way prebuilt and laid out. For some, installing it through Shopify is the best choice as you don’t have to define events yourself in the TikTok Event Manager.

![](https://strapi.omegatheme.com/uploads/tiktok_shopify_method_3918933d6c.png)

For many others, manually installing the pixel with a standard event setup method would be a go-to. TikTok advises you, advertisers, to choose this anyway.

![](https://strapi.omegatheme.com/uploads/manual_dc91c5e47e.png)

![](https://strapi.omegatheme.com/uploads/dev_mode_tiktok_pixel_f8ad75c0ce.png)

Both ways seem completely solve your humble needs for tracking. Until you find out that relying on basic client-side browser setups alone leaves critical blind spots in your attribution data.

## Why would I even want to change the way my pixels are set up?

4 percent. That’s how many [iOS users in the U.S.](https://sea.mashable.com/tech/15641/after-update-only-4-percent-of-ios-users-in-us-let-apps-track-them) let apps track them. Today in 2026, strict privacy frameworks—including Apple’s App Tracking Transparency (ATT), Safari Intelligent Tracking Prevention (ITP), Firefox Enhanced Tracking Protection (ETP), and widespread browser ad blockers—severely restrict traditional client-side cookies and JavaScript pixels.

*Do the below scenarios seem familiar to you?*

- Shopify orders recorded X but your TikTok Pixel only got half the purchases
- Your cost per action is flying blind as a result of a low-quality lookalike audience, which stemmed from an insufficient view custom audience
- You found your hands tied when it comes to tracking custom events (like form submission or page scrolling) and retargeting to these high-intent prospects.
- ROAS doesn’t show up as you don’t know how to attach price and order value parameters to your purchase events.

If you’re not aiming to make ads decision on a severely eclipsed view of data, you might want to switch your TikTok tracking server-side.

## Enter the TikTok Event API solution

Think of it like this:

While the browser-side TikTok pixel can easily fail you when it’s blocked, TikTok Event API stays. And do all the tracking server-side. Each and every event your visitors take on your store can be tracked, logged into a server, and sent directly to the TikTok server.

| Comparison Criteria | 1. Browser-Side TikTok Pixel | 2. Server-Side Events API Only | 3. Hybrid Tracking (Pixel + Events API) |
|:---|:---|:---|:---|
| **Data Collection Mechanism** | Collected via JavaScript running in the user's browser | Transmitted directly from your web/eCommerce server to TikTok | Runs both streams in parallel with `event_id` deduplication |
| **Impact of AdBlockers / iOS** | Loses 30% to 50% of events due to cookie and script blocking | Completely immune to browser ad blockers and Safari ITP | Eliminates 100% of browser-side tracking blind spots |
| **Event Match Quality (Match Rate)** | Moderate (relies heavily on third-party cookies) | High (relies on server order data and IP address) | **Excellent (85%+ via Advanced Matching and SHA-256)** |
| **Setup Complexity** | Very simple (paste snippet into theme header) | Complex if custom-coding a server (AWS/GCP/sGTM) | **Simple when using a dedicated partner integration app** |
| **TikTok's Recommendation** | Outdated for scaling paid campaigns | Good for custom headless architectures | **TikTok's official gold standard in 2026** |

That means:

- **Take back all the would-have-been-miss events:** From *page view, product details page view, add to cart, initiate checkout to complete payment*, all can be recorded and sent to your TikTok Event Manager despite browsers block, across devices with custom event code.
- **Reduce your cost with a more accurate advanced matching:** Say you want to run Dynamic Product Ads (DPA) retargeting to TikTok users who have purchased from your website once, of course, you have to first start with a custom audience based on the actions/events people took on your web. This is where reliable capturing of customer data comes in. To improve the matching quality, it’s best that you could capture *phone number, email, click ID (`ttclid`), IP, user agent, and external ID if applicable.* Then you must send those customer identifiers safely to TikTok by **normalizing and hashing them using the one-way SHA-256 cryptographic standard** (`email`, `phone`, `external_id`). This ensures that TikTok cannot read raw personal data of non-TikTok users while still achieving high deterministic match rates across its ad network.

![](https://strapi.omegatheme.com/uploads/custom_audience_tiktok_ads_b53286f0c7.png)

- **Expand your audience in an accurate way:** If you would like to expand your audience using a lookalike of people who have taken action on your web (not necessarily a purchase and not necessarily attributed events), advanced matching and sufficient event collection is also a must.

In short, only when you can ensure **accurate, sufficient data collection and data sharing** will you be able to guide TikTok to a more optimized target and spending.

**Here’s what you need for a complete setup:**

*One*, you need to ensure **Advanced Matching** parameters (hashed via SHA-256) are sent alongside your web and server events through TikTok Events Manager’s consolidated connection endpoint.

*Two*, you can only ensure the full-funnel view of your event data if server-side tracking through the **Events API is enabled** alongside your browser pixel.

### **How Event Deduplication Works on TikTok**

When running a **Hybrid Setup** (both Browser Pixel and Server-Side Events API active at the same time), you need to prevent the same customer action from being counted twice. TikTok Events Manager handles this automatically through **Event Deduplication**:

- **Matching `event_id` and `event_name`:** Every time a shopper triggers an action—such as `AddToCart`, `InitiateCheckout`, or `CompletePayment`—both your browser pixel and your server payload send the exact same unique `event_id` and `event_name`.
- **48-Hour Deduplication Window:** When TikTok receives both events with identical IDs within a 48-hour window, it automatically merges them into a single conversion record, enriching the browser signal with server-side customer parameters without inflating your reported ROAS.

*Now you might be thinking:*

## TikTok Event API is too technical for me

“Isn’t that too much work to do?” You’re right. These are often developers’ responsibilities as so many technical resources are involved.

The good news is there’s an app that’s designed the exact tasks, applicable for both [Shopify](https://apps.shopify.com/tiktok-multi-pixels?surface_detail=article_id_433&surface_type=omega_blog) and [Wix](https://www.wix.com/app-market/tiktok-shop-connector-by-omega). All you need to do is create the pixels, copy the pixel IDs, generate access tokens, and follow several copies and pastes. Server-side tracking for TikTok is just several clicks away.

## Do I even need to install multiple TikTok pixels?

“It’s nice with the TikTok Event API, but why would I need multiple pixels if my primary pixel is already running?”

In the past, advertisers worried that running both the TikTok Pixel and the Events API simultaneously would cause double-counting of purchases and inflated ROAS. Fortunately, **TikTok has fully rolled out Event Deduplication** across its Events Manager.

By passing an identical `event_id` and `event_name` from both the browser-side pixel and the server-side Events API for the exact same customer action (such as a checkout completion), TikTok’s machine learning algorithm seamlessly merges the signals. It prioritizes the server event containing rich customer parameters (such as hashed email and phone number) while discarding the duplicate browser hit within a 48-hour window. This **Hybrid Setup** is now the official industry standard recommended by TikTok for 100% data reliability (supported seamlessly by apps like [Omega TikTok Multi Pixels](https://apps.shopify.com/tiktok-multi-pixels?surface_detail=article_id_433&surface_type=omega_blog) and [Facebook Multi Pixels](https://apps.shopify.com/facebook-multi-pixels?surface_detail=article_id_433&surface_type=omega_blog)).

However, it’s still strategic to install **multiple TikTok pixels** for **ad account backup and niche segmentation**:
- **Backup Asset Protection:** If your primary TikTok Ad Account encounters unexpected suspension or billing locks, having a secondary backup pixel already seasoned with conversion data ensures you can relaunch campaigns immediately without starting from zero.
- **Collection & Niche Segmentation:** If you run a general Shopify store with distinct product categories (e.g., Pet Supplies vs. Home Decor), assigning dedicated pixels to specific collections keeps your custom audience data clean and hyper-relevant.

With more conversions collected, TikTok will get better at delivering your ads to people who are more likely to take certain actions. You don’t want to miss out on chances to create high-quality custom audiences with data collected through the Event API. And note that **a pixel must have at least 1000 conversion events** before you can create a custom audience out of it.

### **How to Capture and Pass the TikTok Click ID (`ttclid`)**

When a user clicks on your TikTok ad, a unique click identifier called `ttclid` is automatically appended to the destination URL (e.g., `https://yourstore.com/products/summer-dress?ttclid=E.C.P_AbCdEf123...`).

Capturing this parameter is essential for deterministic ad attribution. Here is how it functions:
1. **Capture upon Landing:** When the prospect enters your Shopify store, your tracking script extracts the `ttclid` value from the URL query string and stores it in a first-party cookie or session storage.
2. **Attach to Server Events:** When the customer later initiates checkout or completes a purchase, your server includes this stored `ttclid` inside the event payload sent to the TikTok Events API.
3. **Instant Attribution:** TikTok instantly ties the conversion back to the exact ad creative, ad group, and campaign—even if the user purchased days later or used a privacy-focused browser.

Using automated apps like **Omega TikTok Multi Pixels** handles the capturing, storage, and server-side relay of `ttclid` automatically without writing a single line of custom JavaScript. You can also refer to the official [TikTok Marketing API documentation](https://ads.tiktok.com/marketing_api/docs?rid=4eezrhr6lg4&id=1701890980108353) for technical payload specifications.

### **3 Costly Mistakes to Avoid When Implementing TikTok Events API**

1. **Sending Mismatched Event IDs During Hybrid Tracking:**
   If your browser pixel fires a `CompletePayment` event with `event_id: "1001"` while your server-side payload sends `event_id: "order_1001"`, TikTok will treat them as two distinct transactions, artificially inflating your reported revenue. Always guarantee identical event IDs and event names across both channels.

2. **Sending Raw (Unhashed) Personal Identifiable Information (PII):**
   TikTok’s privacy policy strictly requires that customer emails and phone numbers must be normalized (converted to lowercase, stripped of whitespace) and hashed using the **SHA-256** algorithm before transmission. Submitting plain text PII violates data compliance and causes TikTok to drop the payload.

3. **Omitting Value and Currency Parameters on Purchase Events:**
   Tracking the occurrence of a purchase without transmitting the exact `value` and `currency` (e.g., `value: 49.99`, `currency: "USD"`) disables TikTok's Value-Based Optimization (VBO) algorithms, preventing your campaigns from optimizing for higher Return on Ad Spend (ROAS).

## Frequently Asked Questions (FAQs)

**Q1: Can I use both the TikTok Pixel and TikTok Events API at the same time?**  
**A:** Yes, absolutely. In fact, running both simultaneously in a **Hybrid Setup** is the official recommendation from TikTok. As long as you pass matching `event_id` parameters for deduplication, TikTok will combine the strengths of both methods without duplicating conversion metrics.

**Q2: Does TikTok Events API bypass ad blockers?**  
**A:** Yes. Because the Events API transmits conversion data directly from your eCommerce web server or cloud backend to TikTok’s data intake endpoint, it does not rely on client-side browser scripts that ad blockers, browser privacy extensions, or Safari ITP routinely intercept.

**Q3: What customer data does TikTok Advanced Matching require?**  
**A:** For the highest match rate, TikTok recommends passing hashed email addresses (`em`), hashed phone numbers (`ph`), client IP address (`ip`), user agent (`user_agent`), and the TikTok Click ID (`ttclid`). All personal identifiers must be encrypted with SHA-256 before transmission.

**Q4: How do I test if my TikTok Events API setup is working correctly?**  
**A:** In your **TikTok Ads Manager**, navigate to **Tools > Events > Web Events**, select your Pixel/Event Set, and click on the **Test Events** tab. Enter your website URL or generate a test code, trigger actions on your store (e.g., Add to Cart, Purchase), and observe live incoming events labeled with the "Events API" connection method and "Deduplicated" verification badges.
