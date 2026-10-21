# Signal — Analytics education website

A responsive single-page website about how analytics is useful across business/retail, education, healthcare, marketing, digital products, and public services.

## Run locally
1. Extract the ZIP.
2. Open `index.html` in a browser, or serve this folder with a local web server.
3. Try the domain cards, conversion calculator, and quiz.
4. Open browser DevTools → Console to see demo event logs.

## Connect Google Analytics 4
1. In Google Analytics, create/select a GA4 property and a Web data stream for the site.
2. Copy the Measurement ID (format `G-XXXXXXXXXX`).
3. Open `index.html` and replace `G-XXXXXXXXXX` in `GA_MEASUREMENT_ID` with your actual ID.
4. Host the site on a public domain (or a suitable hosted preview), then test it in GA4 Realtime and DebugView.

The Google Analytics library loads only after a visitor chooses “Allow analytics” in the demo consent banner. A saved preference is stored in local storage. This is a basic demonstration, not a full consent-management platform; adapt consent, privacy notice, retention, and data handling to the laws and policies applicable to your audience.

## Custom events included
- `demo_loaded`
- `domain_selected` with a `domain` parameter
- `calculator_used` with scenario values
- `calculator_input_changed` with a `field` parameter
- `quiz_answered` with question, answer, and correctness parameters
- `quiz_reset`
- Navigation and CTA click events such as `hero_explore_click` and `footer_cta_click`

In GA4, open **Reports → Engagement → Events** to review collected events after data arrives. You can mark meaningful outcomes as key events in the property if appropriate. Event collection can take time; the site does not fabricate GA data, and the dashboard figures displayed on the page are illustrative sample values.

## Privacy note
Do not collect personal, sensitive, or health information in event parameters. The healthcare section is an educational example only. Review the current Google Analytics terms and your local legal requirements before deploying.
