Deploy the readablelabs website to Netlify production.

Follow these steps exactly:

1. Read the Netlify auth token from: /Users/gauravyeole/Library/Preferences/netlify/config.json
   Extract the value at: users["685f2ddf066d25e633bf1be1"].auth.token

2. Zip the site files from /Users/gauravyeole/ReadableLabs/readablelabs:
   Run: zip -r /tmp/readablelabs-deploy.zip index.html yugashree.jpg

3. Upload the zip to Netlify via the API:
   - Site ID: a863ca50-c19b-478f-bb4e-d24cfc0eb0b3
   - Site name: readablelabs
   Run:
   curl -s -X POST "https://api.netlify.com/api/v1/sites/a863ca50-c19b-478f-bb4e-d24cfc0eb0b3/deploys" \
     -H "Authorization: Bearer TOKEN" \
     -H "Content-Type: application/zip" \
     --data-binary @/tmp/readablelabs-deploy.zip

4. Parse the response and confirm:
   - Deploy state (should be "uploaded" or "ready")
   - Live URL: https://readablelabs.netlify.app

5. Clean up the temp zip: rm /tmp/readablelabs-deploy.zip

6. Report success with the live URL.
