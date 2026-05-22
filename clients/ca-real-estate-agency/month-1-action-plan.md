# Month 1 SEO Action Plan: CA Real Estate Agency

**Client:** CA Real Estate Agency  
**Site:** https://carealestateagency.com/  
**Plan date:** 2026-05-22  
**Source:** `audits/initial-seo-audit.md`  
**Scope:** Month 1 SEO Starter deliverables based on the initial audit findings. This plan does not re-run or expand the audit.

## Month 1 Objective

Month 1 should stabilize the site's SEO foundation before broader content or authority work begins. The priority is to clean the index path, fix the most visible on-page issues, protect luxury-brand trust, and set up the access and reporting needed for ongoing SEO decisions.

The most important outcome is a cleaner, more intentional set of indexable pages: core commercial pages should be easier for Google and users to understand, while test/system/thin pages should stop being submitted as search landing pages.

## SEO Starter Deliverables

### 1. Access, Measurement, And Baseline Setup

**Purpose:** Confirm what Google is seeing, establish a baseline, and create the working data sources for the next SEO sprint.

**Actions:**

- Google Search Console, GA4, WordPress admin, SEO plugin, Google Business Profile, and backlink/citation tool access will be requested and connected in a future phase.
- Until access is available, use public-facing evidence and clearly mark platform-specific findings as access-dependent.
- Once access is available, confirm the submitted sitemap status for `https://carealestateagency.com/wp-sitemap.xml`.
- Once access is available, review GSC index coverage for the URLs called out in the audit: `/rent/guesty-test/`, `/rental-checkout/`, `/author/lirim/`, amenity taxonomy pages, location taxonomy pages, and core service pages.
- Once analytics access is available, identify current organic landing pages, inquiry events, booking/request actions, and contact form performance.
- Once WordPress/admin access is available, confirm title tags, meta descriptions, indexation rules, schema settings, and XML sitemap settings can be updated.
- Capture a Month 1 baseline where data is available:
  - Organic clicks and impressions.
  - Top organic queries.
  - Top organic landing pages.
  - Indexed vs submitted pages.
  - Organic inquiries or booking-related conversions if tracking exists.

**Deliverable:** SEO baseline snapshot and access checklist, with unavailable platform data marked as pending access.

**Audit findings addressed:** Sitemap validation needed, Search Console access needed, analytics access needed, keyword mapping missing, internal linking needs full crawl, Core Web Vitals needs access.

### 2. Index Cleanup And Sitemap Hygiene

**Purpose:** Remove low-value, test, and system URLs from the index path so the sitemap only supports pages that should rank or help users.

**Actions:**

- Delete, draft, private, or return `410 Gone` for `/rent/guesty-test/`.
- Remove `/rent/guesty-test/` from XML sitemaps.
- Add `noindex` to `/rental-checkout/` and remove it from XML sitemaps.
- Noindex thin author archives, starting with `/author/lirim/`, and remove user archives from sitemap output.
- Decide which taxonomy types should be indexable:
  - Likely noindex: low-value `rental_amenity` archives unless intentionally built into search pages.
  - Likely noindex or selectively improve: broad property-type archives without unique content.
  - Keep and improve selectively: strategic rental-location pages with inventory and search demand.
- Remove noindexed taxonomy archives from XML sitemaps.
- Resubmit or refresh the sitemap in Google Search Console after access is available and changes are implemented.
- Verify the cleaned URLs are no longer submitted for indexing once Search Console access is available.

**Deliverable:** Clean indexation and sitemap configuration for obvious low-value URLs.

**Audit findings addressed:** Low-value URLs in sitemap, public test rental, indexable checkout page, crawlable thin taxonomy archives, crawlable author archive, sitemap health validation.

### 3. Core Page Metadata And Heading Fixes

**Purpose:** Give each important page a clear search target and stronger search snippet.

**Actions:**

- Add exactly one descriptive H1 to each core indexable page.
- Start with:
  - Homepage.
  - `/sell-with-us/`.
  - `/contact-us/`.
  - `/car-rental/`.
  - `/boat-rental/`.
  - `/private-chef/`.
  - `/restaurants-beach-clubs/`.
- Rewrite the homepage title tag from `CA Real Estate Agency` to a keyword-aligned title.
- Recommended homepage title:
  - `Luxury Villa Rentals & Real Estate in Saint-Martin | CA Real Estate Agency`
- Add a homepage meta description focused on luxury villa rentals, real estate, Saint-Martin, Saint-Barthelemy, Anguilla, and high-touch local guidance.
- Add unique meta descriptions to strategic indexable pages only. Do not write meta descriptions for URLs that will be noindexed.
- For priority listing pages, update title templates to include property type and location when available.
- Fix truncated or auto-generated listing meta descriptions for priority villas.

**Deliverable:** Metadata and H1 update sheet for core pages, plus implementation in WordPress/SEO plugin where access allows.

**Audit findings addressed:** Homepage has no H1, several core pages have no H1, homepage title is too generic, many pages are missing meta descriptions, listing titles miss location/intent modifiers, listing meta description quality is inconsistent.

### 4. Homepage Trust And Luxury Positioning Fixes

**Purpose:** Remove trust-damaging placeholder content and align the homepage with the boutique luxury positioning.

**Actions:**

- Replace homepage proof metrics currently showing `0%`.
- Verified proof points have not been provided yet, so do not invent numbers.
- If verified metrics become available, use specific proof such as years in business, number of villas represented, average review rating, repeat clients, or bookings supported.
- If verified metrics are not available, remove the metric block or replace it with non-quantified trust statements.
- Rewrite duplicated concierge/service copy so each service has a distinct description:
  - Boat rental.
  - Jet ski rental.
  - Private chef.
  - Restaurants and beach clubs.
  - Car rental.
- Keep the tone refined, warm, and service-led. Avoid cheap, bargain, generic, or mass-market language.
- Strengthen visible trust signals on the homepage:
  - Founder-led expertise.
  - Saint-Martin local roots.
  - Curated luxury villa portfolio.
  - High-touch support before and during the stay.
  - Testimonials using verified customer language.

**Deliverable:** Homepage SEO and trust copy updates for the highest-risk credibility issues.

**Audit findings addressed:** Homepage proof metrics show `0%`, concierge service copy is duplicated, E-E-A-T and trust signals need expansion.

### 5. Contact And Local Business Signal Improvements

**Purpose:** Make the business easier to verify and contact, supporting trust, local SEO, and conversion.

**Confirmed public contact details:**

- Phone: `+590 690 768 844`
- Email: `info@carealestateagency.com`
- Locations/service areas:
  - Saint Martin
  - Saint Barthelemy
  - Anguilla
- Site language for SEO: English only

**Actions:**

- Ensure the confirmed phone number, email address, and service areas are visible on the contact page and relevant commercial pages.
- Use English-only SEO copy and metadata unless the client later approves a separate multilingual strategy.
- Confirm NAP consistency across the website and any available citations.
- Add or link to Google Business Profile when access is available.
- Add review or testimonial source links if available.
- Add clearer contact pathways from core commercial pages to inquiry or booking actions.

**Deliverable:** Contact/local trust update recommendations and implemented contact page improvements where access allows.

**Audit findings addressed:** Contact and local business signals incomplete, E-E-A-T and trust signals need expansion, Google Business Profile and local citations need access.

### 6. Strategic Page Prioritization And Keyword Map

**Purpose:** Decide which pages should rank for which search intents before expanding content.

**Confirmed business focus:** Villa rentals and property sales.

**Confirmed geographic focus:** Saint-Martin, Saint-Barthelemy, and Anguilla.

**Actions:**

- Create a starter keyword-to-page map for:
  - Homepage.
  - Villa rental hub.
  - Property sales or real estate hub.
  - `/sell-with-us/`.
  - Priority location pages.
  - Priority concierge/service pages.
  - Priority villa/property listing templates.
- Prioritize keyword themes around:
  - Luxury villa rentals in Saint-Martin / Sint Maarten.
  - Luxury real estate in Saint-Martin.
  - Saint-Barthelemy luxury real estate and villa rental searches.
  - Anguilla luxury real estate and villa rental searches.
  - Villas in Les Terres Basses, Lowlands, Cupecoy, Marigot, and Simpson Bay.
  - Concierge services that support rental and sales inquiries, including boat rental, private chef, car rental, restaurants, and beach clubs.
- Mark each page as one of:
  - Index and optimize now.
  - Index later after content expansion.
  - Noindex.
  - Keep for users but not for SEO.
- Identify the first 3-5 pages to improve after the homepage and core service pages.

**Deliverable:** Starter keyword map and page priority list.

**Audit findings addressed:** Keyword mapping is missing, location pages have SEO potential, thin service pages need more search-intent content, internal linking strategy needs a full crawl.

### 7. Priority Location And Service Page Briefs

**Purpose:** Turn high-potential thin pages into useful landing pages instead of leaving them as weak archives or form-only pages.

**Actions:**

- Choose 1 priority location page for Month 1 improvement, likely Les Terres Basses or Saint-Martin luxury villa rentals if inventory and business priority confirm it.
- Create a content brief for the selected location page covering:
  - Search intent.
  - Recommended title, H1, and meta description.
  - Neighborhood overview.
  - Who the area is best for.
  - Beach/access notes.
  - Featured villas.
  - Internal links to relevant listings and inquiry pages.
  - FAQs.
- Choose 1 priority concierge/service page for Month 1 improvement.
- Create a content brief covering:
  - What the service includes.
  - Who it is for.
  - How booking or coordination works.
  - Areas served.
  - Local differentiators.
  - FAQs.
  - Internal links to villa rental and contact pages.

**Deliverable:** Two SEO content briefs: one location page and one concierge/service page.

**Audit findings addressed:** Location pages have SEO potential but need unique content, thin service pages need more search-intent content, concierge copy is duplicated.

### 8. Structured Data And Template Validation

**Purpose:** Determine whether schema exists after rendering and define what should be added if missing.

**Actions:**

- Use Google Rich Results Test, Schema Validator, rendered browser inspection, or Screaming Frog JavaScript rendering to validate structured data.
- Do not rely on raw HTML checks alone for final schema conclusions.
- If schema is missing or incomplete, prepare implementation requirements for:
  - `RealEstateAgent` or relevant `LocalBusiness` schema.
  - `BreadcrumbList`.
  - Listing/property structured data where eligible and supported.
  - Review/testimonial markup only if it complies with Google's structured data guidelines.
- Validate that schema matches visible page content.

**Deliverable:** Structured data validation note and implementation requirements.

**Audit findings addressed:** Schema markup could not be reliably verified, listing content is a strength, contact/local business signals incomplete.

### 9. Image Alt Text And Listing Template Quick Wins

**Purpose:** Improve accessibility, image relevance, and long-tail SEO on pages that already have strong property content.

**Actions:**

- Add descriptive alt text to meaningful homepage, service, listing, and property images.
- Keep decorative image alt attributes empty only when intentionally decorative.
- Prioritize images on:
  - Homepage.
  - `/sell-with-us/`.
  - Top rental listings.
  - Top property listings.
  - Priority location page.
- Update listing title templates where possible to include:
  - Property name.
  - Property type.
  - Bedroom count when useful.
  - Neighborhood or island.
- Add or improve breadcrumbs if missing from templates.

**Deliverable:** Image alt text quick-win updates and listing template recommendations.

**Audit findings addressed:** Image alt text incomplete, listing titles miss location/intent modifiers, listing content is a strength.

## Suggested Month 1 Timeline

### Week 1: Access, Baseline, And Index Cleanup

- Document pending access for GSC, GA4, WordPress, SEO plugin, GBP, and backlink/citation tools.
- Capture public baseline data where available.
- Confirm sitemap status with public checks, then validate in GSC when access is available.
- Remove or noindex the public test rental, checkout page, author archive, and low-value taxonomy archives where implementation access is available.
- Refresh sitemap output and confirm noindexed pages are removed from submitted sitemaps when Search Console access is available.

### Week 2: Homepage And Core Page Fixes

- Fix homepage title, H1, and meta description.
- Replace or remove `0%` proof metrics. Do not invent proof metrics.
- Rewrite duplicated homepage concierge/service copy.
- Add H1s and meta descriptions to `/sell-with-us/`, `/contact-us/`, and priority service pages.
- Add confirmed contact details and service areas where missing.

### Week 3: Keyword Map And Priority Page Briefs

- Create the starter keyword map for rentals and sales across Saint-Martin, Saint-Barthelemy, and Anguilla.
- Decide which taxonomy/location pages should be indexed, improved, or noindexed.
- Create one priority location page brief.
- Create one priority concierge/service page brief.
- Identify internal linking opportunities between homepage, rental pages, sales/property pages, location pages, service pages, and contact/inquiry paths.

### Week 4: Validation, Quick Wins, And Handoff

- Validate structured data with a rendered tool where access/tools allow.
- Add priority image alt text.
- Improve priority listing title/meta patterns.
- Review GSC after sitemap cleanup when access is available; otherwise document access blocker.
- Prepare the Month 1 handoff summary and Month 2 backlog.

## Month 1 Priority Backlog

### Must Do

1. Remove `/rent/guesty-test/` from the live SEO footprint.
2. Noindex and remove `/rental-checkout/` from XML sitemaps.
3. Noindex thin author archives and remove them from sitemap output.
4. Noindex low-value amenity taxonomy pages unless intentionally developed as landing pages.
5. Fix homepage title, H1, meta description, and `0%` proof metrics.
6. Add H1s and meta descriptions to core indexable pages.
7. Create a starter keyword map for rentals and sales across Saint-Martin, Saint-Barthelemy, and Anguilla.
8. Document pending access for GSC, GA4, WordPress, SEO plugin, Google Business Profile, and backlink/citation tools.

### Should Do

1. Rewrite duplicated concierge copy.
2. Improve contact and local business signals using the confirmed phone, email, and service areas.
3. Decide which location pages should become SEO landing pages.
4. Validate structured data with a rendered testing tool.
5. Add alt text to meaningful property and service images.

### Nice To Do If Time Allows

1. Improve priority listing title tags and meta descriptions.
2. Add breadcrumbs or breadcrumb schema if missing.
3. Draft expanded copy for the first priority location page.
4. Draft expanded copy for the first priority service page.
5. Run PageSpeed or Lighthouse checks once tool access is available.

## Month 1 Success Criteria

By the end of Month 1:

- The sitemap should no longer submit obvious test, checkout, author, or low-value thin archive URLs.
- The homepage should have a clear keyword-aligned title, one H1, a meta description, and no placeholder `0%` trust metrics.
- Core commercial pages should have one H1 and a unique meta description if they remain indexable.
- The client should have a documented starter keyword map focused on rentals and sales across Saint-Martin, Saint-Barthelemy, and Anguilla.
- The client should have a clear decision on which taxonomy/location pages are worth ranking.
- Pending access for Search Console, analytics, WordPress, SEO plugin, GBP, and backlink/citation tools should be documented until available.
- Structured data status should be validated with a rendered tool, not only raw HTML, where access/tools allow.
- A Month 2 backlog should be ready for content expansion, internal linking, schema implementation, performance improvements, and authority building.

## Client Inputs Confirmed And Open Items

### Confirmed

- Priority business focus for the next 90 days: villa rentals and property sales.
- Active geographic priorities: Saint-Martin, Saint-Barthelemy, and Anguilla.
- SEO language strategy: English only.
- Public contact details:
  - Phone: `+590 690 768 844`
  - Email: `info@carealestateagency.com`
  - Locations/service areas: Saint Martin, Saint Barthelemy, Anguilla.
- Platform access timing: Google Search Console, GA4, WordPress, SEO plugin, Google Business Profile, and backlink/citation access will be handled in the future.

### Still Needed

- Verified proof points to replace the homepage `0%` metrics. Until these are provided, remove the metric block or replace it with non-quantified trust statements.

## Month 2 Backlog Candidates

- Expand strategic location pages into true landing pages.
- Expand priority concierge/service pages with useful local search content and FAQs.
- Implement validated schema markup.
- Run a full crawl to find duplicate metadata, crawl depth issues, broken links, canonical problems, and orphan pages.
- Build internal links between location pages, listings, service pages, and inquiry pages.
- Review Core Web Vitals and page speed with PageSpeed Insights, Lighthouse, WebPageTest, or GSC.
- Audit backlink profile, local citations, Google Business Profile, and competitor link gaps.
- Develop authority-building opportunities through luxury travel directories, local partnerships, property owner relationships, destination guides, and press.
