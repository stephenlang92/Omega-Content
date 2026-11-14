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

When shoppers browse Google Shopping for packaged goods—such as cosmetics, bulk groceries, beverages, or flooring—total product price alone rarely tells the full story. Discerning buyers immediately compare the **unit price** (e.g., $0.75/100ml or $2.50/sq ft) to find the best value. 

Under Google Merchant Center guidelines, the `[unit_pricing_measure]` attribute allows merchants to display clear, standardized unit prices directly on Shopping ads and free listings. Under the **EU Price Indication Directive (Directive 98/6/EC)**, as well as UK and Swiss consumer protection regulations, displaying unit prices is legally mandated across the European Union, the UK, and Switzerland—and contrary to old misconceptions that Shopify only supported unit pricing in Germany and France, merchants worldwide (including the US, Canada, and Australia) can now submit this attribute to boost ad click-through rates (CTR) and build shopper trust.

In this updated 2026 guide, we'll explain how `[unit_pricing_measure]` works, the exact formatting rules required by Google, how to resolve common disapproval errors, and how to configure it effortlessly across your Shopify catalog.

## What is Unit price measurement?

The unit\_pricing\_measure attribute contains information about how units of a product variant are measured. Together with a base measure, it’s used as an input to calculate unit prices (unit\_price). If you use the unit pricing measure, then use the [unit pricing base measure](https://support.google.com/merchants/answer/6324490?hl=en) [unit\_pricing\_base\_measure] attribute to include the denominator for your unit price. To make the unit prices more comparable for all ads and free listings on a page, your product might show a different base measure than what you provide here.

Let’s say you are selling 20m Satin silk with $60 for the price and the base measure is 1m (or 2, or whatever), the unit pricing measure would be 20m and the unit price would be $3/1m, for instance.

| Product Name | Sale Price (`price`) | Package Quantity (`unit_pricing_measure`) | Base Denominator (`unit_pricing_base_measure`) | Displayed Unit Price on Google Shopping (`unit_price`) |
|:---|:---|:---|:---|:---|
| Organic Green Tea (100 Bags) | $15.00 | `100ct` | `10ct` | **$1.50 / 10ct** |
| Cold Pressed Olive Oil (500ml) | $12.00 | `500ml` | `100ml` | **$2.40 / 100ml** |
| Oak Laminate Flooring (Box) | $45.00 | `25sqft` | `1sqft` | **$1.80 / 1sqft** |
| Whole Bean Coffee (2 lb Bag) | $18.00 | `2lb` | `1lb` | **$9.00 / 1lb** |

With this, your customers can see the unit price in detail without wondering about it and they may not hesitate to click the link. Here is how it displays on the Google shopping tab:

![](https://strapi.omegatheme.com/uploads/ID_435_1_76ef4a106d.jpg)

### Format

It is a recommended attribute that Google Merchant uses to assess the measure and dimension of a given product without shipping packaging. It should be a positive number and the format has to be: Numerical value + Unit (`1m`, `50ml`, `16.9floz`, etc.), using a period `.` as the decimal separator.

The unit measurement has to be expressed in one of the accepted units:

| Measurement Category | Accepted Units (GMC Standard) | Valid Format Examples | Important Formatting Notes |
|:---|:---|:---|:---|
| **Weight** | `oz`, `lb`, `mg`, `g`, `kg` | `500g`, `2.5lb`, `1kg` | Always use a period `.` for decimals; never use a comma `,`. |
| **Volume (Metric)** | `ml`, `cl`, `l`, `cbm` | `750ml`, `1.5l` | Mandatory for campaigns targeting the United Kingdom (UK) and European Union (EU). |
| **Volume (US Imperial)** | `floz`, `pt`, `qt`, `gal` | `16.9floz`, `1gal` | Applicable only for the United States (US) market. |
| **Length** | `in`, `ft`, `yd`, `cm`, `m` | `50m`, `12ft` | Commonly used for fabrics, electrical cables, ribbons, and curtains. |
| **Area** | `sqft`, `sqm` | `25sqm`, `150sqft` | Popular for hardwood flooring, carpets, ceramic tiles, and wallpaper. |
| **Per Unit (Count)** | `ct` | `100ct`, `24ct` | Used for supplement capsules, tea bags, face masks, and detergent pods. |

[For details on when and how to submit values in English, learn more about submitting your product data](https://support.google.com/merchants/answer/10668075)

### Is it required or optional?

Unit price measurement is what Google looks at when trying to understand the unit pricing information of an item.

Broadly speaking, it’s optional & highly recommended for Hardware, Office Supplies, Food, Beverages, Flooring, Business Cards, Perfume, Cosmetics, and Pet Food because your customer might be interested in the price per unit for your product and if it falls into one of the categories above, then we recommend that you submit the unit pricing measure **[unit\_pricing\_measure]** attribute to improve ad CTR.

Note that you may be required to provide this information based on local laws or regulations. Under the **EU Price Indication Directive (Directive 98/6/EC)** and the **UK Competition and Markets Authority (CMA) Price Marking Order**, submitting unit pricing is mandatory when targeting countries in the European Economic Area (EEA), the UK, and Switzerland—including Germany, France, Italy, Spain, the Netherlands, the Czech Republic, the UK, and Switzerland—as well as specific jurisdictions in Australia and the US where local unit pricing laws apply.

### **How to Fix Common Google Merchant Center Disapprovals for Unit Price**

Submitting unit pricing incorrectly is one of the most frequent reasons for Google Merchant Center warnings. Here are the top 3 errors and how to resolve them:

1. **"Invalid real number in attribute: unit pricing measure"**
   - **Root Cause:** Submitting numerical values with comma separators (e.g., `1,5kg` or `1,000ml`) instead of standard periods, or using fractions (e.g., `1/2lb`).
   - **The Fix:** Format all decimal numbers using a period: `1.5kg` or `0.5lb`. Never include thousand separators or extra spaces between digits.

2. **"Unit pricing base measure missing denominator"**
   - **Root Cause:** When you submit `[unit_pricing_measure]`, Google expects a clear reference point. If omitted, Google attempts to default to standard units (1kg, 100ml), which may misrepresent high-value concentrated items.
   - **The Fix:** Always provide `[unit_pricing_base_measure]` alongside `[unit_pricing_measure]` (for instance, `unit_pricing_measure: 50ml` and `unit_pricing_base_measure: 10ml`).

3. **"Unrecognized unit of measurement"**
   - **Root Cause:** Submitting abbreviations not recognized in Google's taxonomy (e.g., writing `fl. oz.`, `capsules`, `pieces`, `sq. meters`, or `liters` in full text).
   - **The Fix:** Restrict your units strictly to Google's standard enum list: use `floz` (not `fl. oz.`), `ct` (for pieces/capsules), `l` (for liters), and `sqm` (for square meters).

## How to set up the unit price with Google Shopping Feed by Omega?

With [Omega Google Shopping Feed](https://apps.shopify.com/google-shopping-feed-pro?utm_source=omegaweb&utm_medium=blog), you can easily add Unit prices for variants/products with several clicks no matter which country you are based in.

We offer a bulk assign option so that you can upload your CSV file following the format of a sample file we had. Please follow the following guidelines:

- Step 1: Choose products that you want to bulk assign unit price then select the Assign unit pricing measure by CSV

  ![](https://strapi.omegatheme.com/uploads/ID_435_7_59e218c8e2.jpg)
- Step 2: Download the sample file and fill it in with the required field then upload again after that 

  ![](https://strapi.omegatheme.com/uploads/ID_435_8_848749f7ab.jpg)

  Also, you can easily set the unit price for a single product by editing it

  ![](https://strapi.omegatheme.com/uploads/ID_435_4_7579f6023f.jpg)

  Now set the unit pricing measure and base measure for each variant, I bet the result on your Google Merchant account will surprise you.

  ![](https://strapi.omegatheme.com/uploads/ID_435_5_1_a908e5fd6a.jpg)

  Finally, don’t forget to sync the latest data to your Google Merchant account by clicking the feed now button  
  ![](https://strapi.omegatheme.com/uploads/ID_435_6_fc0ad137a6.jpg)  
  Now just wait for your products to appear on the Google shopping tab with the unit price in detail.

| Pre-Sync Verification Step | What to Check Before Clicking "Feed Now" | Example of Valid Entry |
|:---|:---|:---|
| **1. Decimal Separator** | Ensure all decimal numbers use a period `.` rather than a comma `,` | `1.5kg` (not `1,5kg`) |
| **2. Accepted Unit Code** | Match unit abbreviations strictly against Google's supported enum list | `16.9floz` (not `16.9 fl. oz.`) |
| **3. Matching Dimension Class** | Both `unit_pricing_measure` and `unit_pricing_base_measure` must share the same category (e.g., both weight or both volume) | `500ml` and `100ml` |
| **4. Variant-Level Mapping** | Verify that multi-size variants (e.g., 250g vs. 500g) each have their own exact measure assigned | SKU-250: `250g` / SKU-500: `500g` |

**Additional guidelines**

> **Important Cross-Border Note (UK Metric vs. US Imperial):** Review each section closely to determine if the requirements apply to your target country or product. If you don’t follow the requirements that apply to you, Google will disapprove your product and notify you in the **Needs Attention (Diagnostics)** tab of your Google Merchant Center account. For merchants targeting the **United Kingdom (UK)**, always submit **Metric values** (`ml`, `l`, `g`, `kg`). Google interprets imperial abbreviations (`floz`, `pt`, `qt`, `gal`) strictly as **US Imperial units**, which differ in volume from UK Imperial units (for example, 1 US gallon is 3.785 liters, whereas 1 UK Imperial gallon is 4.546 liters).

## Frequently Asked Questions (FAQs)

**Q1: Can I submit unit pricing measure for products sold in bundles or multi-packs?**  
**A:** Yes. For multi-packs (e.g., a pack of 6 bottles of 500ml), calculate the total volume across all units contained in the package (`3000ml` or `3l`) as the `[unit_pricing_measure]`. If sold as individual count units, use `6ct` with a base measure of `1ct`.

**Q2: Does displaying unit price increase my Google Shopping CPC?**  
**A:** No. Displaying unit pricing does not increase Cost-Per-Click. In fact, by providing upfront transparency to shoppers, listings with accurate unit prices typically see higher Click-Through Rates (CTR) and better Quality Scores, which can lower effective CPCs.

**Q3: What happens if my Shopify store is based in the US, but I sell to the UK and Germany?**  
**A:** Google applies regulations based on the **target country** of your shopping feed, not your business registration address. If your feed targets users in Germany or the UK, submitting `[unit_pricing_measure]` is legally required for applicable goods. You must also ensure UK feeds use Metric units (ml, g, kg) rather than US Imperial measurements.

**Q4: How do variant products handle different unit pricing measures on Shopify?**  
**A:** When selling products with multiple size options (e.g., 250g, 500g, 1kg), each variant must have its own dedicated `[unit_pricing_measure]` mapped to its unique SKU. Using a feed app like Omega Google Shopping Feed allows you to assign variant-level measures automatically via CSV.
