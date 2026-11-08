# RPPF Production Tracker

Mobile-friendly production output and dispatch tracker.

## Current app
- Admin login via Supabase Auth
- Product master
- Excel import (A Product Code, B Product Name, C Unit, D Batch No, F Quantity, G UOM)
- Production date selected manually during import
- Separate output record for each batch
- Manual output / previous-month carry-forward entry
- Dispatch entry without customer, destination or challan fields
- Monthly product-wise output, dispatch and balance summary

## Supabase setup
Project: `vazcuxilwqrbugcekxmn`

The app uses the public publishable key only. Do not add service-role or secret keys to this repository.

The existing database policies require the signed-in user to have `app_metadata.role = admin`. Create the user in Supabase Authentication, then assign the admin role securely in the user's **App Metadata** (not User Metadata). Never put privileged keys in this static website.

## GitHub Pages
In repository Settings > Pages, set Build and deployment source to **GitHub Actions**. The workflow in `.github/workflows/deploy.yml` deploys the site after each push to main.
