LeadHunt
A personal outreach tool for finding local businesses with bad or missing websites, drafting cold emails, and tracking who you've contacted — all from a single HTML file you host yourself.
Built for freelance web developers doing local cold outreach.

What it does

Import businesses from Google Maps with one click using a browser bookmarklet
Score their website automatically using Google's free PageSpeed API
Draft personalized cold emails based on what's wrong (no site, slow site, or general)
Find owner emails via Hunter.io (optional, free tier)
Track every lead — status, date, notes, PageSpeed score, reply rate
Export to CSV anytime as a backup


Setup
1. Host the file
This tool requires hosting to work properly. GitHub Pages is free and takes about 5 minutes.

Create a free account at github.com
Click New repository → name it leadhunt → set to Public
Upload index.html and commit
Go to Settings → Pages → Branch: main → Save
Your site will be live at https://yourusername.github.io/leadhunt


⚠️ Do not skip hosting. The Google Maps bookmarklet only works correctly when the app is served from a real URL. Running it as a local file will break the import flow.

2. Fill in your settings
Open the app and go to ⚙ Settings. Fill in:

Your name
Your city and state
Your email address
Hunter.io API key (optional — for auto-finding emails)
Default business type

These save automatically and are used in every email draft.
3. Set up the Google Maps bookmarklet

Go to the 🔖 Maps Import tab
Show your bookmarks bar: Ctrl+Shift+B (Windows) or Cmd+Shift+B (Mac)
Drag the "Send to LeadHunt" button into your bookmarks bar


You must drag the bookmarklet from your hosted URL, not a local file. The bookmarklet has your URL baked into it.


Daily workflow

Open maps.google.com
Search for a business type in your city (e.g. "plumbers Sherman TX")
Click a business so its detail panel loads on the left
Click "Send to LeadHunt" in your bookmarks bar
A new LeadHunt tab opens — click + Add to Pipeline
The site gets auto-scored immediately
Click ✉ Draft Email to preview, or 📧 Open Gmail to send
Status updates to Emailed automatically when you open Gmail
Come back and mark Replied or Closed when they respond

Repeat for 3–5 businesses a day. That's 15–25 emails a week.

Email templates
Three templates are built in and fire automatically based on the situation:
TemplateWhen it's usedNo WebsiteBusiness has no website, only a Google listing or FacebookSlow SiteWebsite scores under 50/100 on PageSpeed mobileGeneralHas a site but it looks neglected or has issues
Editing templates
Go to ⚙ Settings → Email Templates to edit any template. Changes save as you type.
Available variables:
VariableWhat it inserts{{biz}}Business name{{type}}Business type (e.g. auto repair){{city}}City and state from your settings{{score}}PageSpeed score (for slow site template){{notes}}Notes you added when importing the lead{{notes_line}}Notes formatted as a new paragraph (or blank if no notes){{name}}Your name from settings
A live preview with sample data updates as you type so you can see exactly how the email will look before sending.
To go back to the originals, click ↺ Reset to defaults.

Hunter.io (optional)
Hunter.io finds email addresses from a business domain.

Free tier: 25 domain searches per month
Add your API key in ⚙ Settings → API Keys
When you score a lead that has a website, LeadHunt will automatically look up the email too


PageSpeed scoring
Uses Google PageSpeed Insights API — completely free, no API key needed.
Scores are on a 0–100 scale (mobile performance):

0–49 🔥 — Poor. Strong pitch angle. Triggers the "Slow Site" email template.
50–74 — Needs work. General template.
75–100 — Decent. General template.


Data & privacy

All data is stored in your browser's localStorage
Nothing is sent to any server (except PageSpeed API calls to Google and Hunter.io if you use it)
Clearing browser data or switching browsers will lose your leads — export CSV regularly
To move data to a new browser, export CSV, then re-import manually


Tips for getting replies

Send Monday–Wednesday mornings — highest open rates
Keep to 20–30 emails per week max to avoid spam flags from Gmail
Add a specific note when importing (e.g. "contact form broken", "no hours listed") — {{notes_line}} will include it in the email automatically, making it feel more personal
Follow up once after 5–7 days if no reply
Expect a 2–5% reply rate — that's normal and not a reflection on your email
At 30 emails/week, that's 1–2 replies per week. Stay consistent.


Troubleshooting
Bookmarklet opens a new tab but no popup appears
The lead may have already been added. Check the Pipeline tab.
Business name comes in blank or wrong
Make sure the business detail panel is fully loaded on the left side of Maps before clicking the bookmarklet.
No website detected on import
Not all businesses list their website on Google Maps. Paste it manually in the Add Business form.
PageSpeed score says N/A
The site may be blocking the PageSpeed API, or the URL may be incorrect. Try adding https:// manually if it's missing.
Hunter.io not finding emails
Free tier is 25/month. Check your usage at hunter.io/dashboard. Some domains won't have results even with a valid key.
My leads disappeared
localStorage was cleared (browser data wipe, private mode, or different browser). Always export CSV regularly as a backup.
