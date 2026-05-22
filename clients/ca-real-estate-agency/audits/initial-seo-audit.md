# Initial SEO Audit: CA Real Estate Agency

**Site:** https://carealestateagency.com/  
**Audit date:** 2026-05-22  
**Scope:** Initial public-facing SEO audit of the homepage, sitemap, robots.txt, selected listing pages, selected service pages, and selected WordPress system/archive pages.  
**Access limitations:** No Google Search Console, GA4, server logs, CMS admin, PageSpeed Insights quota, browser rendering session, Screaming Frog crawl, or backlink tool access was available. Items that require those sources are marked **Needs access**.

## Executive Summary

CA Real Estate Agency has a strong luxury real estate positioning and several listing pages with useful property-level content. The site is crawlable at a basic level, uses HTTPS, redirects HTTP and `www` to the canonical non-`www` HTTPS domain, and exposes a WordPress XML sitemap.

The biggest SEO risks are index quality, on-page fundamentals, and trust signals. The sitemap includes low-value/system URLs such as a test rental, checkout page, author archive, and 92 amenity taxonomy pages. Many important pages are missing meta descriptions and H1s. The homepage title is too generic, has no H1, and shows placeholder proof metrics of `0%`. Structured data could not be confirmed with a rendered browser, and no JSON-LD appeared in sampled raw HTML.

Top priorities:

1. Remove or noindex low-value URLs from the index path: `/rent/guesty-test/`, `/rental-checkout/`, `/author/lirim/`, and thin taxonomy archives.
2. Fix on-page basics on core pages: unique title tags, meta descriptions, one H1, and keyword-aligned headings.
3. Replace placeholder homepage proof metrics and duplicated concierge/service copy.
4. Add or validate structured data for real estate agency, local business, listings, breadcrumbs, and reviews.
5. Use Search Console, analytics, and a full crawl to confirm indexation, organic performance, crawl errors, and duplicate/canonical issues.

## Initial Assessment

### Site Context

CA Real Estate Agency is a boutique luxury real estate and villa rental agency serving Saint-Martin/Sint Maarten, Saint-Barts, and Anguilla. The primary SEO goal is to generate qualified villa rental inquiries, booking requests, and buyer/seller leads for Caribbean luxury real estate.

Priority topics implied by the product context and site content:

- Luxury villa rentals in Saint-Martin / Sint Maarten.
- Luxury real estate in Saint-Martin, Saint-Barts, and Anguilla.
- Villas in Les Terres Basses, Lowlands, Cupecoy, Marigot, Simpson Bay, and other local areas.
- Concierge services such as car rental, boat rental, jet ski rental, restaurants, beach clubs, and private chef.
- Property sales, buyer advisory, and seller representation.

### Current State

Confirmed from public evidence:

- WordPress site.
- `robots.txt` exists and references `https://carealestateagency.com/wp-sitemap.xml`.
- XML sitemap exists and contains pages, rentals, properties, taxonomies, and one user archive.
- Homepage is indexed publicly in search results.
- Representative rental and property pages return `200` and contain unique property content.
- Important pages such as homepage, sell/contact/service pages are missing meta descriptions and H1s in sampled raw HTML.

Needs access:

- Current organic traffic baseline.
- Google Search Console index coverage, sitemap status, query data, crawl errors, and Core Web Vitals.
- GA4 conversion and landing page performance.
- Recent migration or site launch history.
- Top organic competitors and priority keywords confirmed by the business.
- Server logs or crawl stats.

### Pages Sampled

| URL | Status | Notes |
|---|---:|---|
| `https://carealestateagency.com/` | 200 | Homepage. No H1, no meta description, generic title. |
| `https://carealestateagency.com/robots.txt` | 200 | Allows crawl except `/wp-admin/`; points to WordPress sitemap. |
| `https://carealestateagency.com/wp-sitemap.xml` | 200 | Sitemap index available via direct fetch. |
| `https://carealestateagency.com/sitemap.xml` | 301 | Redirects to `wp-sitemap.xml` via direct fetch. |
| `https://carealestateagency.com/sell-with-us/` | 200 | No H1, no meta description. |
| `https://carealestateagency.com/contact-us/` | 200 | No meta description observed; contact details are thin. |
| `https://carealestateagency.com/rent/villa-sole-luce/` | 200 | Listing content present; no JSON-LD observed in raw HTML. |
| `https://carealestateagency.com/rent/villa-ellia/` | 200 | Listing content present; meta description truncates with ellipsis. |
| `https://carealestateagency.com/property/villa-madinina/` | 200 | Listing content present; no JSON-LD observed in raw HTML. |
| `https://carealestateagency.com/rent/guesty-test/` | 200 | Public test rental in sitemap. |
| `https://carealestateagency.com/rental-checkout/` | 200 | Checkout page in sitemap with `$0.00` booking content. |
| `https://carealestateagency.com/author/lirim/` | 200 | Thin author archive in sitemap. |
| `https://carealestateagency.com/rental_amenity/wireless-internet/` | 200 | Thin amenity archive in sitemap. |
| `https://carealestateagency.com/rental_location/les-terres-basses/` | 200 | Location archive with listing excerpts. |

Note: Cursor `WebFetch` returned intermittent `500` errors for several sitemap URLs, while direct HTTP checks returned `200`. Treat sitemap health as needing confirmation in Search Console and a crawler before closing the issue.

## Technical SEO Findings

### 1. Low-Value URLs Are Included in the XML Sitemap

**Issue:** The WordPress sitemap includes pages and archives that should probably not be submitted for indexing.

**Impact:** High. Sitemap inclusion tells search engines these URLs are canonical, indexable, and worth crawling. Low-value pages can waste crawl budget, dilute site quality, and create poor search snippets.

**Evidence:** The sitemap index includes:

- 14 pages.
- 17 rental listings.
- 51 property listings.
- 16 property-type taxonomy URLs.
- 8 rental-location taxonomy URLs.
- 92 rental-amenity taxonomy URLs.
- 1 user archive.

Sample low-value URLs:

- `https://carealestateagency.com/rent/guesty-test/` returns a public test listing titled `Test_Guesty Test`.
- `https://carealestateagency.com/rental-checkout/` returns checkout content with `Subtotal: $0.00 USD`, `Taxes: $0.00 USD`, and `Total: $0.00 USD`.
- `https://carealestateagency.com/author/lirim/` returns a thin author archive.
- `https://carealestateagency.com/rental_amenity/wireless-internet/` returns a thin amenity archive.

**Fix:** Remove test/system URLs from the sitemap and apply `noindex, follow` where appropriate. Delete or draft the test rental. Noindex checkout, author archives, and low-value amenity taxonomies unless they are intentionally developed as search landing pages.

**Priority:** High.

### 2. Sitemap Health Needs Search Console Validation

**Issue:** Public direct fetches returned `200` for `wp-sitemap.xml` and its child sitemaps, but the fetch tool intermittently returned `500` for sitemap URLs.

**Impact:** Medium to High. If Googlebot sees sitemap `500` errors, discovery and recrawl efficiency can suffer. If this is only a tool-specific user-agent issue, the direct SEO impact is lower.

**Evidence:** Direct HTTP checks returned `200` for:

- `https://carealestateagency.com/wp-sitemap.xml`
- `https://carealestateagency.com/wp-sitemap-posts-page-1.xml`
- `https://carealestateagency.com/wp-sitemap-posts-rental-1.xml`
- `https://carealestateagency.com/wp-sitemap-posts-property-1.xml`
- Taxonomy and user sitemap children.

Cursor `WebFetch` reported `500` on several of the same XML endpoints.

**Fix:** **Needs access** to Google Search Console sitemap report and/or an external crawler using Googlebot-like user agents. Confirm whether Google can fetch the sitemap without server errors. If errors appear, review WordPress sitemap generation, caching, CDN, security plugin, and server logs.

**Priority:** High until verified.

### 3. Public Test Rental Is Indexable

**Issue:** `/rent/guesty-test/` is public, self-canonical, and included in the rental sitemap.

**Impact:** High. A test listing undermines trust, adds thin/irrelevant content, and can be indexed for branded or rental searches.

**Evidence:** The page returns `200`, title `Test_Guesty Test – CA Real Estate Agency`, H1 `Test_Guesty Test`, no meta description, and a self-referencing canonical.

**Fix:** Delete the test rental, set it to draft/private, or return `410 Gone` if it was never meant to exist. Remove it from XML sitemaps.

**Priority:** High.

### 4. Checkout Page Is Indexable and in the Sitemap

**Issue:** `/rental-checkout/` is crawlable, self-canonical, and in the page sitemap.

**Impact:** High. Checkout pages rarely serve organic search intent and can expose confusing booking states to search engines.

**Evidence:** The page returns `200`, title `Booking Checkout – CA Real Estate Agency`, no meta description, no H1, and visible placeholder booking totals of `$0.00`.

**Fix:** Add `noindex, nofollow` or `noindex, follow` depending on internal link needs, remove it from the XML sitemap, and block it from internal navigation unless part of an active user flow.

**Priority:** High.

### 5. Thin Taxonomy Archives Are Crawlable

**Issue:** Amenity, property-type, and some location taxonomy archives are included in XML sitemaps. Many appear to be list pages with generic excerpts and no unique intro copy, metadata, or structured search intent.

**Impact:** Medium to High. Thin taxonomy archives can create index bloat and duplicate listing snippets.

**Evidence:** The sitemap includes 92 `rental_amenity` URLs, 16 `property-types` URLs, and 8 `rental_location` URLs. Sample amenity page `Wireless Internet` has no meta description and no canonical observed in raw HTML. Sample location page `Les Terres Basses` has listing excerpts and no meta description.

**Fix:** Decide which taxonomy pages are strategic SEO landing pages. For strategic location pages, add unique content, optimized metadata, internal links, and helpful local guidance. For amenity archives and low-value property-type archives, apply `noindex, follow` and remove from the sitemap.

**Priority:** High.

### 6. Author Archive Is Crawlable

**Issue:** `/author/lirim/` is included in the sitemap and returns a thin author archive.

**Impact:** Medium. Thin author pages can create low-quality indexed URLs and expose internal usernames.

**Evidence:** The page returns `200`, title `Lirim – CA Real Estate Agency`, H1 `Author: Lirim`, no meta description, and no canonical observed in raw HTML.

**Fix:** Noindex author archives if they are not part of a content strategy. Remove user sitemaps from XML sitemap output.

**Priority:** Medium.

### 7. HTTPS and Canonical Host Redirects Are Working

**Issue:** No major issue found.

**Impact:** Positive. Consistent host/protocol reduces duplicate URL risk.

**Evidence:** `http://carealestateagency.com/` returns `301` to `https://carealestateagency.com/`. `https://www.carealestateagency.com/` returns `301` to `https://carealestateagency.com/`.

**Fix:** Keep this behavior. Consider adding HSTS after confirming all subresources are HTTPS.

**Priority:** Low.

### 8. HSTS Header Not Observed

**Issue:** `Strict-Transport-Security` was not observed in sampled response headers.

**Impact:** Low to Medium. HSTS is not a ranking lever by itself, but it improves security posture and trust.

**Evidence:** Header checks for sampled URLs returned no `strict-transport-security` header.

**Fix:** After verifying the entire site and subdomains are HTTPS-safe, add an HSTS header at the server/CDN level.

**Priority:** Low.

### 9. Core Web Vitals and Page Speed Need Access

**Issue:** Core Web Vitals could not be verified.

**Impact:** Medium. The sampled homepage raw HTML was large at roughly 329 KB, and listing/service pages were also heavy in raw HTML, but real performance depends on rendered resources, JavaScript execution, image loading, caching, and CrUX field data.

**Evidence:** PageSpeed Insights API returned `429 Too Many Requests`, so no Lighthouse or CrUX report was available during this audit.

**Fix:** **Needs access** to PageSpeed Insights, Lighthouse, Chrome DevTools, Search Console Core Web Vitals, or WebPageTest. Measure mobile LCP, INP, CLS, TTFB, render-blocking resources, image payload, and JavaScript execution.

**Priority:** Medium.

### 10. Schema Markup Could Not Be Reliably Verified

**Issue:** No JSON-LD structured data appeared in sampled raw HTML, but schema detection requires rendered validation because WordPress plugins can inject JSON-LD with JavaScript.

**Impact:** Medium to High. This site is a strong candidate for `RealEstateAgent` or `LocalBusiness`, `BreadcrumbList`, listing/property structured data where eligible, and review/testimonial markup if compliant.

**Evidence:** Raw HTML checks found `0` `application/ld+json` blocks on sampled homepage, listing, property, service, taxonomy, checkout, and author pages.

**Fix:** **Needs access** to a rendered browser, Google Rich Results Test, Schema Validator, or Screaming Frog with JavaScript rendering. If schema is missing after rendered validation, implement appropriate JSON-LD.

**Priority:** Medium.

### 11. Mobile-Friendliness Needs Rendered Validation

**Issue:** Mobile rendering could not be fully verified.

**Impact:** Medium. Mobile-first indexing means mobile layout, tap targets, horizontal scrolling, and content parity matter.

**Evidence:** Sampled HTML includes a viewport tag (`width=device-width, initial-scale=1`), which is positive. Actual mobile rendering was not tested.

**Fix:** **Needs access** to a browser/mobile rendering test. Validate responsive layout, tap target sizes, search/filter usability, booking form usability, image loading, and no horizontal overflow.

**Priority:** Medium.

## International SEO & Localization Findings

### 12. Locale Strategy Is Unclear

**Issue:** The site uses `lang="en-US"` and includes English and French place/audience signals, but no alternate language URLs or hreflang annotations were confirmed.

**Impact:** Medium. The business serves Saint-Martin/Sint Maarten, Saint-Barts, Anguilla, and likely both English- and French-speaking visitors. If the site has or plans multilingual pages, hreflang and canonical strategy need to be deliberate.

**Evidence:** Sampled pages use `lang="en-US"`. Some content includes French destination names and one sampled rental excerpt in French on taxonomy pages, but no hreflang was observed in raw checks.

**Fix:** If the site is English-only, keep one canonical English version and avoid mixed-language page bodies where possible. If French pages are planned, use locale subdirectories such as `/en/` and `/fr/`, self-canonical each locale page, include reciprocal hreflang including self-references, and add `x-default`.

**Priority:** Medium if multilingual growth matters; Low if English-only is intentional.

### 13. Mixed-Language Listing Content Needs Review

**Issue:** Some listing excerpt content appears in French inside English taxonomy pages.

**Impact:** Low to Medium. Mixed-language content can weaken language targeting and search snippet clarity.

**Evidence:** `https://carealestateagency.com/rental_location/les-terres-basses/` includes an excerpt for `Villa Nuit d’Etoile` in French while the page language is `en-US`.

**Fix:** Ensure English pages use English primary content. If French content is needed, create proper French locale pages rather than mixing languages on English pages.

**Priority:** Medium.

## On-Page SEO Findings

### 14. Homepage Has No H1

**Issue:** The homepage has no H1 in sampled raw HTML.

**Impact:** High. The H1 is a major on-page clarity signal for users and search engines.

**Evidence:** Homepage extraction found `h1: []`. The visible main headline appears as an H2: `Luxury Real Estate In The Caribbean`.

**Fix:** Make the primary hero headline an H1. Consider: `Luxury Real Estate and Villa Rentals in Saint-Martin`.

**Priority:** High.

### 15. Several Core Pages Have No H1

**Issue:** Important service and lead-generation pages use H2s but no H1.

**Impact:** High. Missing H1s reduce page clarity and keyword targeting.

**Evidence:** No H1 found on sampled pages:

- Homepage.
- `/sell-with-us/`.
- `/contact-us/`.
- `/restaurants-beach-clubs/`.
- `/car-rental/`.
- `/boat-rental/`.
- `/private-chef/`.

**Fix:** Add exactly one descriptive H1 to every indexable page. Match each H1 to the page’s search intent.

**Priority:** High.

### 16. Homepage Title Tag Is Too Generic

**Issue:** The homepage title is only `CA Real Estate Agency`.

**Impact:** High. It does not communicate the primary keyword, geography, or offer in search results.

**Evidence:** Homepage title extracted as `CA Real Estate Agency`.

**Fix:** Rewrite the homepage title around the strongest search intent. Example: `Luxury Villa Rentals & Real Estate in Saint-Martin | CA Real Estate Agency`.

**Priority:** High.

### 17. Many Pages Are Missing Meta Descriptions

**Issue:** Several important pages have no meta description.

**Impact:** Medium. Meta descriptions do not directly determine rankings, but they influence SERP click-through and message control.

**Evidence:** No meta description found on sampled pages:

- Homepage.
- `/sell-with-us/`.
- `/contact-us/`.
- `/rental-checkout/`.
- `/rent/guesty-test/`.
- `/author/lirim/`.
- `/rental_amenity/wireless-internet/`.
- `/rental_location/les-terres-basses/`.
- Concierge/service pages such as `/car-rental/`, `/boat-rental/`, `/private-chef/`, and `/restaurants-beach-clubs/`.

**Fix:** Add unique meta descriptions to all strategic indexable pages. Do not spend time writing meta descriptions for pages that should be noindexed.

**Priority:** High.

### 18. Listing Titles Are Brand-Only and Miss Location/Intent Modifiers

**Issue:** Listing title tags follow a simple `Property Name – CA Real Estate Agency` format.

**Impact:** Medium. Property pages can capture long-tail searches if titles include property type and location.

**Evidence:** Sample titles:

- `Villa Sole Luce – CA Real Estate Agency`
- `Villa Ellia – CA Real Estate Agency`
- `Villa Madinina – CA Real Estate Agency`

**Fix:** Use richer title patterns, such as `Villa Sole Luce | 4-Bed Luxury Villa in Les Terres Basses, Saint-Martin`.

**Priority:** Medium.

### 19. Meta Description Quality Is Inconsistent on Listings

**Issue:** Some listing meta descriptions are good, but at least one sampled description is truncated with an ellipsis.

**Impact:** Medium. Truncated or auto-generated descriptions can reduce snippet quality.

**Evidence:** `Villa Ellia` meta description ends with `A perfect Caribbean retreat…`.

**Fix:** Write controlled descriptions of roughly 150-160 characters for priority listings, emphasizing bedrooms, location, pool/view, and target guest.

**Priority:** Medium.

### 20. Image Alt Text Is Incomplete

**Issue:** Sampled pages include images with empty or missing alt text.

**Impact:** Medium. Image alt text supports accessibility, image search, and topical relevance, especially for villa/property pages.

**Evidence:** Raw HTML image checks found:

- Homepage: 12 images, 4 empty/missing alt attributes.
- `/sell-with-us/`: 4 images, 2 empty/missing alt attributes.
- Listing/property samples: 7 images each, 2 empty/missing alt attributes each.

**Fix:** Add descriptive alt text for meaningful property, villa, and service images. Decorative images can remain empty if intentionally marked as decorative.

**Priority:** Medium.

### 21. Internal Linking Strategy Needs a Full Crawl

**Issue:** Internal link coverage could not be fully assessed from the sample.

**Impact:** Medium. Important listing, location, and service pages need clear pathways from the homepage and hub pages.

**Evidence:** Homepage links to selected listings and service pages. Sitemap contains many additional URLs that require crawl-depth analysis.

**Fix:** **Needs access** to a full crawl. Map click depth from homepage to all priority pages, identify orphan pages, and add contextual links between homepage, rental hub, property hub, location pages, listing pages, and concierge service pages.

**Priority:** Medium.

### 22. Keyword Mapping Is Missing

**Issue:** There is no visible keyword map tying pages to primary search intents.

**Impact:** Medium. Without keyword mapping, pages may cannibalize each other or miss valuable local search terms.

**Evidence:** Public pages target broad terms like luxury real estate, rentals, villa pages, and location archives, but search intent ownership is not clearly structured.

**Fix:** **Needs access** to keyword research and Search Console data. Create a map for homepage, rental hub, sales/property hub, location pages, listing pages, and concierge pages.

**Priority:** Medium.

## Content Findings

### 23. Homepage Proof Metrics Show `0%`

**Issue:** The homepage displays trust metrics as `0%`.

**Impact:** High. Placeholder proof damages credibility, especially for luxury clients making high-value booking or purchase decisions.

**Evidence:** Homepage includes:

- `Listings Closed Successfully 0%`
- `Satisfied Clients Worldwide 0%`
- `Repeat and Referral Business 0%`
- `Concierge Service Satisfaction 0%`

**Fix:** Replace with verified numbers, remove the metric block, or use non-quantified proof until real metrics are available.

**Priority:** High.

### 24. Concierge Service Copy Is Duplicated

**Issue:** Several service descriptions repeat the same boat-rental copy.

**Impact:** Medium to High. Duplicate or irrelevant copy reduces quality and trust, especially on high-intent service pages.

**Evidence:** Homepage blocks for Boat Rental, Jet Ski Rental, and Private Chef repeat similar copy about boat rental and seaside excursions.

**Fix:** Write unique service copy for each concierge offer. Include what is offered, ideal guest use case, how booking works, and local differentiators.

**Priority:** High.

### 25. Thin Service Pages Need More Search-Intent Content

**Issue:** Concierge/service pages appear structurally thin and mostly form-led.

**Impact:** Medium. These pages may not deserve to rank for local service queries without more useful content.

**Evidence:** Sampled service pages have no meta descriptions and no H1. They primarily include a service heading and inquiry form.

**Fix:** For services worth ranking, add 500-900 words of useful content, FAQs, service details, areas served, images, trust signals, and internal links. For services not intended for organic acquisition, keep them indexable only if needed for users, or noindex if thin.

**Priority:** Medium.

### 26. Location Pages Have SEO Potential but Need Unique Content

**Issue:** Location taxonomy pages list properties but lack unique local guidance and metadata.

**Impact:** Medium to High. Location pages could rank for searches like `Les Terres Basses villa rentals`, but only if they become true landing pages.

**Evidence:** `Les Terres Basses` page lists villas with excerpts but no meta description and no apparent unique introductory content.

**Fix:** Build strategic location pages for areas with inventory and search demand. Add neighborhood overview, who it is best for, beach/access notes, featured villas, FAQs, internal links, and listing filters.

**Priority:** High.

### 27. Listing Content Is a Strength

**Issue:** No issue; this is an opportunity.

**Impact:** Positive. Sample rental/property pages contain meaningful descriptions, location context, amenities, and booking details.

**Evidence:** `Villa Sole Luce`, `Villa Ellia`, and `Villa Madinina` each include detailed descriptions, neighborhood/transit/access sections or property details.

**Fix:** Build on this strength with better titles, schema, image alt text, internal links, breadcrumbs, and nearby-location linking.

**Priority:** Medium.

### 28. E-E-A-T and Trust Signals Need Expansion

**Issue:** The site has some testimonials and founder positioning, but trust content could be stronger for high-value real estate decisions.

**Impact:** Medium. Luxury real estate and villa rentals require strong trust, local expertise, and proof.

**Evidence:** Homepage includes testimonials and a founder narrative, but public proof metrics are placeholders and contact details are limited in the sampled contact page.

**Fix:** Add verified founder/team credentials, licensing/market expertise where applicable, review sources, number of villas represented, years of experience, press mentions, guest service details, and clear contact information.

**Priority:** Medium.

### 29. Contact and Local Business Signals Are Incomplete

**Issue:** Contact page shows phone and locations, but email support appears as a heading without a visible email in fetched text.

**Impact:** Medium. Local SEO and trust benefit from consistent NAP, visible contact details, and local business corroboration.

**Evidence:** Contact page includes phone `+590 690 768 844` and locations `Saint Martin`, `Saint Barthelemy`, `Anguilla`; no email address was visible in fetched content.

**Fix:** Add complete visible contact details, office/service area details, embedded map where appropriate, Google Business Profile link, social/review links, and consistent NAP across the site and citations.

**Priority:** Medium.

## Authority & Links Findings

### 30. Backlink Profile Needs Access

**Issue:** Authority and link profile could not be audited from public page fetches alone.

**Impact:** Medium to High. Real estate and travel SERPs can be competitive, and backlinks/local citations matter.

**Evidence:** No Ahrefs, Semrush, Moz, Majestic, Google Search Console links report, or citation audit access was available.

**Fix:** **Needs access** to backlink data. Review referring domains, anchor text, lost links, toxic/spam patterns, competitor link gaps, local citations, travel directory listings, and partner links.

**Priority:** Medium.

### 31. Google Business Profile and Local Citations Need Access

**Issue:** Local visibility could not be verified.

**Impact:** Medium. For a local/boutique real estate agency, Google Business Profile, local reviews, and citation consistency can materially affect discovery.

**Evidence:** No GBP dashboard or citation tool access was available.

**Fix:** **Needs access** to Google Business Profile and citation data. Confirm categories, service areas, photos, reviews, posts, UTM-tagged website link, NAP consistency, and local landing page alignment.

**Priority:** Medium.

## Prioritized Action Plan

### Critical Fixes

1. Delete, draft, or `410` `/rent/guesty-test/`; remove it from sitemaps.
2. Noindex and remove `/rental-checkout/` from XML sitemaps.
3. Noindex and remove the thin author archive from XML sitemaps.
4. Decide which taxonomy archives should rank; noindex low-value amenity archives and remove them from sitemaps.
5. Confirm sitemap accessibility in Google Search Console because public tools showed inconsistent behavior.

### High-Impact Improvements

1. Add one H1 to every indexable core page, starting with homepage, contact, sell-with-us, and concierge/service pages.
2. Rewrite homepage title and add a homepage meta description targeting luxury villa rentals and real estate in Saint-Martin.
3. Add unique meta descriptions to all strategic indexable pages.
4. Replace homepage `0%` proof metrics with verified proof or remove the block.
5. Rewrite duplicated concierge copy and expand priority service pages.
6. Build strategic location landing pages for key areas such as Les Terres Basses, Lowlands, Cupecoy, Marigot, Simpson Bay, Saint-Barts, and Anguilla where inventory and business priorities justify it.

### Quick Wins

1. Add descriptive alt text to property and service images.
2. Improve listing title tags with property type and location modifiers.
3. Fix truncated listing meta descriptions.
4. Add visible email/contact details to the contact page if appropriate.
5. Add contextual internal links from listing pages to location pages, service pages, and contact/inquiry pages.

### Long-Term Recommendations

1. Create a keyword map for homepage, rental hub, property hub, location pages, service pages, and listing templates.
2. Validate and implement structured data with rendered testing.
3. Run a full crawl with Screaming Frog or Sitebulb to identify duplicates, redirect chains, missing metadata, orphan pages, canonical issues, broken links, image issues, and crawl depth.
4. Use Search Console to compare submitted vs. indexed URLs and identify pages Google excludes as duplicate, crawled not indexed, discovered not indexed, soft 404, or alternate canonical.
5. Build authority through local citations, travel/luxury directories, partner links, property owner partnerships, press, and destination content.

## Needs Access Checklist

- Google Search Console: index coverage, sitemap status, queries, pages, Core Web Vitals, crawl stats, links.
- GA4 or analytics platform: organic landing pages, conversions, assisted conversions, engagement, booking/inquiry funnel.
- CMS/WordPress admin: sitemap settings, SEO plugin settings, noindex controls, title/meta templates, schema settings.
- Rendered browser or Rich Results Test: structured data validation.
- PageSpeed Insights/WebPageTest/Lighthouse: mobile performance and Core Web Vitals.
- Screaming Frog/Sitebulb crawl: full technical/on-page crawl.
- Backlink/citation tool: authority, local citations, competitor link gaps.
- Google Business Profile: local SEO configuration, reviews, categories, service areas, photos, posts.

## Suggested First 2-Week SEO Sprint

1. Clean the index path: remove or noindex test, checkout, author, and low-value taxonomy URLs.
2. Update sitemap output and resubmit in Google Search Console.
3. Fix homepage title, H1, meta description, proof metrics, and duplicated service copy.
4. Add H1s and meta descriptions to contact, sell-with-us, and priority service pages.
5. Run a full crawl and Search Console review to produce the next, evidence-complete SEO backlog.

