# Content Refresh & Audit Report: "How To Optimize Your Google Shopping Feed With Unit Price Measurement"

> **Mục tiêu:** Tối ưu hóa (Refresh & Enrich) bài viết kỹ thuật feed chuyên sâu, mở rộng dung lượng từ bài viết ngắn cũ (~500 từ) lên chuẩn mực SERP (~1.300–1.600 từ), cập nhật chính sách toàn cầu 2026 và bổ sung hướng dẫn gỡ lỗi Google Merchant Center.  
> **Nguyên tắc cốt lõi:** Bảo tồn tối đa cấu trúc gốc (URL slug & 2 H2 cốt lõi), cập nhật thông tin lỗi thời (fact-check tính khả dụng toàn cầu của Shopify/Google), làm giàu dữ liệu bằng bảng tính toán thực tế và lấp đầy khoảng trống xử lý lỗi từ chối feed (disapprovals).

---

## 0. Tổng quan Hiện trạng (Audit Metadata)

| Chỉ số / Thông tin | Giá trị hiện tại | Điểm chuẩn SERP (Benchmark) | Đánh giá chênh lệch (Delta) |
|:---|:---|:---|:---|
| **URL bài viết** | `https://www.omegatheme.com/blogs/how-to-optimize-google-shopping-feed-with-unit-price-measurement` | — | Trang live |
| **Nguồn nội dung audit** | `outputs/omegatheme/unit_pricing_measure/unit_pricing_measure_source.md` | — | Bản local Markdown (xuất bản từ tháng 11/2021) |
| **Primary Keyword** | `unit_pricing_measure` | — | Thuộc tính kỹ thuật Google Merchant Center |
| **Thứ hạng SERP hiện tại** | Ngoài Top 8 (đối thủ Google Support, FeedArmy, GoDataFeed đang chiếm lĩnh) | Top 1–5 Google US | Cần refresh toàn diện để lấy lại thứ hạng |
| **Mục tiêu tối ưu** | Cứu vãn bài viết suy giảm & lọt vào Top 3 Google US | Top 1–3 Google US | Tối ưu hóa chiều sâu kỹ thuật |
| **Dung lượng bài viết** | ~500 từ | ~960 – 1.400 từ (Google Support & các guide chuyên sâu) | Rất mỏng (thiếu khoảng 700–900 từ) |
| **Cấu trúc Heading** | 2 H2 / 2 H3 | 2–4 H2 / 6–8 H3 | Thiếu phần gỡ lỗi disapprovals và khối FAQ |

---

## 1. Bảng Tổng hợp Rà soát Lỗi thời & Thiếu hụt (Gap & Fact-check)

Checklist phát hiện các điểm nghẽn của bài viết so với SERP:

- [x] **Lỗi thời về dữ liệu / chính sách (Outdated Facts):** 
  - Phần mở đầu (Sapo) ghi: *"From Shopify’s statement, the unit prices are available only to stores located in Germany or France."* Thông tin này đã hoàn toàn lỗi thời! Hiện nay, Shopify đã hỗ trợ unit pricing cho toàn bộ khu vực kinh tế châu Âu (EEA), Vương quốc Anh, Thụy Sĩ, và cho phép merchant toàn cầu (kể cả US/Canada) quản lý đơn giá linh hoạt qua Metafields hoặc Feed Apps chuyên dụng.
  - Giao diện Google Merchant Center và các thông báo lỗi đã được Google cập nhật sang Merchant Center Next (2024–2026).
- [x] **Khoảng trống SERP Norm (Missing Sub-topics):** 
  - Thiếu phần giải thích lỗi từ chối feed phổ biến nhất trên Google Merchant Center: *"Invalid real number unit pricing measure"* (nhập dấu phẩy thay vì dấu chấm thập phân, hoặc viết liền không có khoảng cách hợp lệ).
  - Thiếu bảng ví dụ tính toán so sánh trực quan giữa Giá bán sản phẩm, `unit_pricing_measure` và `unit_pricing_base_measure` để người đọc hiểu bản chất phép chia.
  - Thiếu mục FAQ giải đáp các câu hỏi thường gặp khi đồng bộ variant (biến thể) trên Shopify.
- [x] **Trải nghiệm trực quan (Visual & Formatting):** 
  - Bảng "Supported units" trong bài gốc bị vỡ layout định dạng (dồn hết text vào 1 ô). Cần chuyển thành bảng Markdown đa cột chuẩn mực.

---

## 2. Ma trận Kế hoạch Hành động Từng Mục (Section-by-Section Action Plan)

Bảng chi tiết hướng dẫn sửa đổi cho từng phần của bài viết (bảo tồn nguyên vẹn cấu trúc gốc):

| Vị trí / Heading hiện tại | Nhãn hành động | Vấn đề hiện tại | Hành động chỉnh sửa chi tiết |
|:---|:---|:---|:---|
| **Title & H1: How To Optimize Your Google Shopping Feed With Unit Price Measurement** | `[KEEP]` | Tiêu đề tốt, chứa đầy đủ từ khóa và search intent tối ưu feed. | Giữ nguyên H1 và URL slug gốc. |
| **Introduction / Sapo** | `[UPDATE]` | Thông tin giới hạn *"chỉ áp dụng cho store tại Đức và Pháp"* đã lỗi thời, gây hoang mang cho merchant các thị trường khác. | Viết lại Sapo: làm rõ vai trò của `[unit_pricing_measure]` trong việc cải thiện CTR quảng cáo, cập nhật quy định bắt buộc toàn EU/UK và tính khả dụng toàn cầu. |
| **H2: What is Unit price measurement?** | `[ENRICH]` | Khái niệm giải thích đúng bản chất nhưng ví dụ lụa satin 20m còn khá sơ sài, thiếu bảng minh họa phép tính. | Bổ sung 01 Bảng ví dụ thực tế đa ngành hàng (Mỹ phẩm, Nước giải khát, Sàn gỗ, Cà phê hạt) minh họa rõ ràng công thức tính. |
| **H3: Format** | `[UPDATE]` | Bảng đơn vị hỗ trợ (Supported units) bị lỗi format gom cụm một dòng; thiếu chỉ dẫn về dấu phân cách thập phân chuẩn của Google. | Sửa lại Bảng đơn vị đo lường thành bảng 3 cột rõ ràng (Nhóm đơn vị, Đơn vị hợp lệ theo chuẩn GMC, Ví dụ chuẩn). Bổ sung lưu ý dấu chấm thập phân `.`. |
| **H3: Is it required or optional?** | `[UPDATE]` | Danh sách các quốc gia bắt buộc cần bổ sung cập nhật chỉ thị EU Price Indication Directive và quy định UK Competition and Markets Authority (CMA). | Cập nhật căn cứ pháp lý tại EU & UK; liệt kê rõ ràng các danh mục ngành hàng được hưởng lợi nhiều nhất về CTR khi hiển thị đơn giá. |
| **H3 Mới đề xuất (dưới H2 What is...): How to Fix Common Disapprovals (Invalid Real Number & Formatting Errors)** | `[FILL-GAP]` | Khoảng trống lớn so với các đối thủ kỹ thuật (#2 FeedArmy, #4 GoDataFeed): người dùng tìm kiếm từ khóa này phần lớn do gặp lỗi từ chối trong Google Merchant Center. | Bổ sung mục H3 phân tích 3 lỗi phổ biến nhất: 1) Lỗi "Invalid real number" (nhầm dấu `,` và `.`), 2) Lỗi đơn vị không được hỗ trợ, 3) Lỗi thiếu `unit_pricing_base_measure` khi đã khai báo measure. |
| **H2: How to set up the unit price with Google Shopping Feed by Omega?** | `[ENRICH]` | Các bước hướng dẫn rất chi tiết nhưng giao diện hướng dẫn cần được chú thích rõ ràng theo bản cập nhật mới nhất của ứng dụng Omega. | Bổ sung bảng checklist kiểm tra dữ liệu trước khi bấm nút "Feed Now" để đảm bảo 100% sản phẩm được duyệt trên GMC. |
| **Section: Additional guidelines** | `[ENRICH]` | Cảnh báo về hệ đo lường UK Metric vs US Imperial rất giá trị. Cần trình bày thành một Callout Box nổi bật giúp người bán xuyên biên giới (Cross-border) không bị nhầm lẫn. | Định dạng lại thành Callout box chuyên sâu về khác biệt giữa US Fluid Ounce vs UK Fluid Ounce và Gallon. |
| **H2 Mới đề xuất: Frequently Asked Questions (FAQs)** | `[FILL-GAP]` | Bài viết chưa có khối FAQ. | Bổ sung 4 câu hỏi thường gặp bám sát các thắc mắc trên diễn đàn Google Ads Community và Reddit. |

*(Ghi chú: Toàn bộ bảng hành động chỉ sử dụng đúng 4 nhãn chuẩn mực: `[KEEP]`, `[UPDATE]`, `[ENRICH]`, `[FILL-GAP]`; tuyệt đối không dùng nhãn nào khác).*

---

## 3. Nội dung Mẫu Đề xuất Sửa đổi (Draft Rewrite & Enrichment Snippets)

Cung cấp sẵn các đoạn văn hoàn chỉnh để người biên tập có thể copy/paste trực tiếp:

### Snippet 1: Viết lại Sapo loại bỏ thông tin lỗi thời `[UPDATE]`
> **Đoạn cũ:**
> *"The product price and currency are required attributes for all products. Most of our customers said that they were impressed by the products that have clear information about unit price on the shopping tab. From Shopify’s statement, the unit prices are available only to stores located in Germany or France. Does that mean only stores from Germany and France can feed the unit price field to their Google Merchant account? Not actually. But, how? Let’s dive into this!"*
>
> **Đoạn mới đề xuất (Cập nhật 2026):**
> *"When shoppers browse Google Shopping for packaged goods—such as cosmetics, bulk groceries, beverages, or flooring—total product price alone rarely tells the full story. Discerning buyers immediately compare the **unit price** (e.g., $0.75/100ml or $2.50/sq ft) to find the best value. 
> 
> Under Google Merchant Center guidelines, the `[unit_pricing_measure]` attribute allows merchants to display clear, standardized unit prices directly on Shopping ads and free listings. While unit pricing is legally mandated across the EU, UK, and Switzerland, merchants worldwide—including those in the US and Canada—can leverage this attribute to dramatically increase ad click-through rates (CTR) and build shopper trust.
> 
> In this updated 2026 guide, we'll explain how `[unit_pricing_measure]` works, the exact formatting rules required by Google, how to resolve common disapproval errors, and how to configure it effortlessly across your Shopify catalog."*

### Snippet 2: Bảng phân loại đơn vị đo lường chuẩn mực (Thay thế bảng vỡ layout) `[UPDATE]`
> Thay thế bảng tại mục **Format** bằng bảng Markdown chuẩn xác sau:
>
> | Phân nhóm đo lường | Đơn vị hợp lệ (Accepted Units) | Ví dụ định dạng chuẩn | Lưu ý quan trọng |
> |:---|:---|:---|:---|
> | **Weight (Khối lượng)** | `oz`, `lb`, `mg`, `g`, `kg` | `500g`, `2.5lb`, `1kg` | Luôn sử dụng dấu chấm `.` cho số thập phân, không dùng dấu phẩy `,`. |
> | **Volume (Metric)** | `ml`, `cl`, `l`, `cbm` | `750ml`, `1.5l` | Bắt buộc đối với các chiến dịch nhắm mục tiêu tại Anh (UK) và Liên minh Châu Âu (EU). |
> | **Volume (US Imperial)** | `floz`, `pt`, `qt`, `gal` | `16.9floz`, `1gal` | Chỉ áp dụng cho thị trường Hoa Kỳ (US). |
> | **Length (Chiều dài)** | `in`, `ft`, `yd`, `cm`, `m` | `50m`, `12ft` | Thường áp dụng cho vải vóc, cáp điện, rèm cửa. |
> | **Area (Diện tích)** | `sqft`, `sqm` | `25sqm`, `150sqft` | Phổ biến cho sàn gỗ, thảm, gạch men, giấy dán tường. |
> | **Per Unit (Số lượng)** | `ct` | `100ct`, `24ct` | Sử dụng cho viên uống, gói trà túi lọc, khẩu trang, viên tẩy rửa. |

### Snippet 3: Bảng ví dụ tính toán công thức Unit Price `[ENRICH]`
> Chèn vào dưới đoạn giải thích khái niệm tại H2:
>
> | Tên sản phẩm | Giá bán (`price`) | Khối lượng gói (`unit_pricing_measure`) | Đơn vị gốc (`unit_pricing_base_measure`) | Hiển thị thực tế trên Google Shopping (`unit_price`) |
> |:---|:---|:---|:---|:---|
> | Organic Green Tea (100 Bags) | $15.00 | `100ct` | `10ct` | **$1.50 / 10ct** |
> | Cold Pressed Olive Oil (500ml) | $12.00 | `500ml` | `100ml` | **$2.40 / 100ml** |
> | Oak Laminate Flooring (Box) | $45.00 | `25sqft` | `1sqft` | **$1.80 / 1sqft** |
> | Whole Bean Coffee (2 lb Bag) | $18.00 | `2lb` | `1lb` | **$9.00 / 1lb** |

### Snippet 4: Hướng dẫn xử lý 3 lỗi từ chối feed phổ biến nhất `[FILL-GAP]`
> Chèn mục H3 mới này vào cuối mục **What is Unit price measurement?**:
>
> ```markdown
> ### **How to Fix Common Google Merchant Center Disapprovals for Unit Price**
> 
> Submitting unit pricing incorrectly is one of the most frequent reasons for Google Merchant Center warnings. Here are the top 3 errors and how to resolve them:
> 
> 1. **"Invalid real number in attribute: unit pricing measure"**
>    - **Root Cause:** Submitting numerical values with comma separators (e.g., `1,5kg` or `1,000ml`) instead of standard periods, or using fractions (e.g., `1/2lb`).
>    - **The Fix:** Format all decimal numbers using a period: `1.5kg` or `0.5lb`. Never include thousand separators or extra spaces between digits.
> 
> 2. **"Unit pricing base measure missing denominator"**
>    - **Root Cause:** When you submit `[unit_pricing_measure]`, Google expects a clear reference point. If omitted, Google attempts to default to standard units (1kg, 100ml), which may misrepresent high-value concentrated items.
>    - **The Fix:** Always provide `[unit_pricing_base_measure]` alongside `[unit_pricing_measure]` (for instance, `unit_pricing_measure: 50ml` and `unit_pricing_base_measure: 10ml`).
> 
> 3. **"Unrecognized unit of measurement"**
>    - **Root Cause:** Submitting abbreviations not recognized in Google's taxonomy (e.g., writing `fl. oz.`, `capsules`, `pieces`, `sq. meters`, or `liters` in full text).
>    - **The Fix:** Restrict your units strictly to Google's standard enum list: use `floz` (not `fl. oz.`), `ct` (for pieces/capsules), `l` (for liters), and `sqm` (for square meters).
> ```

### Snippet 5: Khối FAQ giải đáp thắc mắc chuyên sâu `[FILL-GAP]`
> Bổ sung khối H2 FAQ vào cuối bài viết:
>
> > **Q1: Can I submit unit pricing measure for products sold in bundles or multi-packs?**  
> > **A:** Yes. For multi-packs (e.g., a pack of 6 bottles of 500ml), calculate the total volume across all units contained in the package (`3000ml` or `3l`) as the `[unit_pricing_measure]`. If sold as individual count units, use `6ct` with a base measure of `1ct`.
> >
> > **Q2: Does displaying unit price increase my Google Shopping CPC?**  
> > **A:** No. Displaying unit pricing does not increase Cost-Per-Click. In fact, by providing upfront transparency to shoppers, listings with accurate unit prices typically see higher Click-Through Rates (CTR) and better Quality Scores, which can lower effective CPCs.
> >
> > **Q3: What happens if my Shopify store is based in the US, but I sell to the UK and Germany?**  
> > **A:** Google applies regulations based on the **target country** of your shopping feed, not your business registration address. If your feed targets users in Germany or the UK, submitting `[unit_pricing_measure]` is legally required for applicable goods. You must also ensure UK feeds use Metric units (ml, g, kg) rather than US Imperial measurements.
> >
> > **Q4: How do variant products handle different unit pricing measures on Shopify?**  
> > **A:** When selling products with multiple size options (e.g., 250g, 500g, 1kg), each variant must have its own dedicated `[unit_pricing_measure]` mapped to its unique SKU. Using a feed app like Omega Google Shopping Feed allows you to assign variant-level measures automatically via CSV.

---

## 4. Checklist Triển khai On-page Sau Khi Cập nhật

- [ ] Cập nhật ngày sửa đổi (Date Modified: `2026-11-06`) trên hệ thống blog.
- [ ] Xác thực các ảnh chụp màn hình ứng dụng Omega Google Shopping Feed để đảm bảo khớp với bản cập nhật giao diện mới nhất.
- [ ] Bổ sung Schema Article và Schema FAQPage cho 4 câu hỏi thường gặp.
- [ ] Đặt link nội bộ trỏ tới bài viết liên quan về tối ưu Feed Google Shopping (`feed_management_tools` và `google_shopping_not_working`).
- [ ] Yêu cầu Re-index trên Google Search Console.
