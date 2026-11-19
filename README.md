# TTM Kajabi Theme

Brand styles for the Tim Talks Money course area on Kajabi (academy.timtalksmoney.com).

The course pages use Kajabi's **Premier** product template. On the Growth plan the template code can't be edited, so this repo holds one stylesheet (`ttm.css`). Kajabi loads it from jsDelivr through each course's **Custom Code → Embedded Scripts** box.

Design reference: the approved mockups on the "TTM Academy – Kajabi course redesign" canvas.

## Install (once per course)

1. In Kajabi: **Products → [course] → Customize → (template) Customize → Settings → Custom Code**.
2. Paste this into **Embedded Scripts**. The part after `@` pins a version: a commit ID or a release tag (see Making changes).

   ```html
   <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/rebeccanguyen/ttm-kajabi-theme@COMMIT_OR_TAG/ttm.css">
   ```

3. Click **Preview** and check the course page and a lesson page before you click **Save**.

Also in the template settings: replace the header logo with the transparent TTM logo (white "timtalks", lime "money"), because the header is now forest green.

Courses to install on:

- [x] Investing Made Simple (Self-Paced): Premier 7.11.0
- [x] Investing Made Simple (Live), Cohort 1: Premier 7.11.0
- [x] Retirement Made Simple (Self Paced): Premier 7.11.0
- [x] Retirement Made Simple – Live, Live Cohort 1: Premier 7.10.4

Live version on courses: `39702b2ee4848f61716b9bc620f6f9a9ba2352e7`. Live version on the website template: `baeb2f0a3d695c9fb7d66a71782685869b70fb03` (19 Nov 2026).

New cohorts get their own course template, so add the tag to each new cohort's template too.

## Testing safely

IMS Self-Paced has a second, inactive template installed. Add the tag to that template first and use its **Preview** link. Members keep seeing the live template until you click **Activate**.

## Making changes

1. Edit `ttm.css` and commit.
2. Pin the new version: either copy the commit ID, or create a release on GitHub (**Releases → Draft a new release**, tag `v1.0.1`, `v1.1.0` …).
3. Update the part after `@` in each course's Embedded Scripts tag.

Pinning a commit or tag means changes only go live when you choose. Pointing at `@main` instead updates automatically, but jsDelivr caches branches for several hours.

## Login and library pages

The site uses the **Streamlined Home** website template (Encore 2.x), which is live. The stylesheet is loaded from that template's **Settings → Custom Code → CSS** box:

```css
@import url("https://cdn.jsdelivr.net/gh/rebeccanguyen/ttm-kajabi-theme@COMMIT_OR_TAG/ttm.css");
```

- The left-hand brand panel on the login page is `assets/login-panel.jpg`. To change its wording or photo, re-export the image and commit it.
- Site Details → Homepage is set to **Show the Library**, so academy.timtalksmoney.com goes to sign-in, not the template's demo homepage. Keep it that way unless a real homepage is built.
- Removed from the template: the library's demo hero, Offer Storefront and link-list sections, and the header's About & Contact menu. The /about and /contact pages still exist but nothing links to them.

## What CSS can't change on Growth

Layout structure (what appears where on the page) comes from the template code, which needs the Pro plan. 
## Brand

| Token | Hex |
|---|---|
| Beige (background) | `#f8f2e9` |
| Light green | `#d5f4d9` |
| Forest green | `#074730` |
| Green | `#039136` |
| Lime (highlights only) | `#c1ff72` |

Headings: Bricolage Grotesque 800. Body: Open Sans. Buttons: black, white text, fully rounded.
