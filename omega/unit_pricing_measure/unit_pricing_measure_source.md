---
title: "How To Optimize Your Google Shopping Feed With Unit Price Measurement"
slug: "how-to-optimize-google-shopping-feed-with-unit-price-measurement"
source_url: "https://www.omegatheme.com/blogs/how-to-optimize-google-shopping-feed-with-unit-price-measurement"
published_date: "2021-11-24T20:53:30.000Z"
category: "Google Shopping"
author: "Anita Nguyen"
thumbnail: "https://strapi.omegatheme.com/uploads/Unit_Price_Measurement_1c798343c4.png"
meta_description: "Use the Unit Pricing measurment to strengthen the data stream that Google Shopping provides. Read Omegatheme's tips to optimize Your Google Shopping Feed here."
---

# How To Optimize Your Google Shopping Feed With Unit Price Measurement

> **Source:** [https://www.omegatheme.com/blogs/how-to-optimize-google-shopping-feed-with-unit-price-measurement](https://www.omegatheme.com/blogs/how-to-optimize-google-shopping-feed-with-unit-price-measurement)  
> **Category:** Google Shopping | **Author:** Anita Nguyen | **Published:** 2021-11-24T20:53:30.000Z

![Featured Image](https://strapi.omegatheme.com/uploads/Unit_Price_Measurement_1c798343c4.png)

## Meta Description
Use the Unit Pricing measurment to strengthen the data stream that Google Shopping provides. Read Omegatheme's tips to optimize Your Google Shopping Feed here.

---

The product price and currency are required attributes for all products. Most of our customers said that they were impressed by the products that have clear information about unit price on the shopping tab. From Shopify’s statement, the unit prices are available only to stores located in Germany or France. Does that mean only stores from Germany and France can feed the unit price field to their Google Merchant account? Not actually. But, how? Let’s dive into this!

## What is Unit price measurement?

The unit\_pricing\_measure attribute contains information about how units of a product variant are measured. Together with a base measure, it’s used as an input to calculate unit prices (unit\_price). If you use the unit pricing measure, then use the [unit pricing base measure](https://support.google.com/merchants/answer/6324490?hl=en) [unit\_pricing\_base\_measure] attribute to include the denominator for your unit price. To make the unit prices more comparable for all ads and free listings on a page, your product might show a different base measure than what you provide here.

Let’s say you are selling 20m Satin silk with $60 for the price and the base measure is 1m (or 2, or whatever), the unit pricing measure would be 20m and the unit price would be $3/1m, for instance

With this, your customers can see the unit price in detail without wondering about it and they may not hesitate to click the link. Here is how it displays on the Google shopping tab:

![](https://strapi.omegatheme.com/uploads/ID_435_1_76ef4a106d.jpg)

### Format

It is a recommended attribute that Google Merchant uses to assess the measure and dimension of a given product without shipping packaging. It should be a positive number and the format has the be: Numerical value + Unit: 1m, 50ml, 16.9oz, etc

The unit measurement has to be expressed in one of the accepted units:

|  |  |
| --- | --- |
| **Type** | Positive number plus unit |
| **Supported units** | - Weight: oz, lb, mg, g, kg      - Volume (US imperial): floz, pt, qt, gal      - Volume (metric): ml, cl, l, cbm      - Length: in, ft, yd, cm, m      - Area: sqft, sqm      - Per unit: ct |
| **Repeated field** | No |

[For details on when and how to submit values in English, learn more about submitting your product data](https://support.google.com/merchants/answer/10668075)

### Is it required or optional?

Unit price measurement is what Google looks at when trying to understand the unit pricing information of an item

Broadly speaking, it’s optional & highly recommended for Hardware, Office Supplies, Food, Beverages, Flooring, Business Cards, Perfume, etc. because your customer might be interested in the price per unit for your product and it falls into one of the categories above, then we recommend that you submit the unit pricing measure **[unit\_pricing\_measure]** attribute.

Note that you may be required to provide this information based on local laws or regulations. It is mandatory in some countries (EU and Switzerland) where it is required by laws: UK, Germany, France, Italy, Spain, Switzerland, the Czech Republic, and the Netherlands

## How to set up the unit price with Google Shopping Feed by Omega?

With [Omega Google Shopping Feed](https://apps.shopify.com/google-shopping-feed-pro?utm_source=omegaweb&utm_medium=blog), you can easily add Unit prices for variants/products with several clicks no matter which country you are based in.

We offer a bulk assign option so that you can upload your CSV file following the format of a sample file we had. Please follow the following guidelines:

- Step 1: Choose products that you want to bulk assign unit price then select the Assign unit pricing measure by CSV

  ![](https://strapi.omegatheme.com/uploads/ID_435_7_59e218c8e2.jpg)
- Step 2: Download the sample file and fill it in with the required field then upload again after that 

  ![](https://strapi.omegatheme.com/uploads/ID_435_8_848749f7ab.jpg)

  Also, you can easily set the unit price for a single product by editing it

  ![](https://strapi.omegatheme.com/uploads/ID_435_4_7579f6023f.jpg)

  Now set the unit pricing measure and base measure for each variant, I bet the result on your Google Merchant account will surprise you.

  ![](https://strapi.omegatheme.com/uploads/ID_435_5_1_a908e5fd6a.jpg)

  Finally, don’t forget to sync the latest data to your Google Merchant account by clicking the feed now button  
  ![](https://strapi.omegatheme.com/uploads/ID_435_6_fc0ad137a6.jpg)  
  Now just wait for your products to appear on the Google shopping tab with the unit price in detail.

  **Additional guidelines**

  Review each section closely to determine if the requirements apply to your country or product. If you don’t follow the requirements that apply to you, Google will disapprove your product and let you know in Diagnostics in your Merchant Center account.One important note for Merchants in the United Kingdom only: Do not forget to submit metric values when targeting the UK. The imperial units (for example, fl, oz, pt, qt, gal) are interpreted as US imperial units, which are different than the imperial units used in the UK
