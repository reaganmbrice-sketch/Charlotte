S20 REACH CHECK - SITE APP
==========================

What this is
------------
A web app your surveyor installs on his Android phone. It works offline, uses
the phone's GPS and compass, keeps photos with each measured point, and sends
results to the office through the phone's share menu.

The files in this folder must be put on a website (HTTPS). Opening index.html
directly from the phone's files won't work: GPS, the compass, offline mode and
"install" all need the page to come from a web address.


Option 1: your company website (easiest if you have one)
--------------------------------------------------------
Ask whoever looks after the website to upload this whole folder to a new
address, for example:  https://www.yourcompany.co.uk/s20/
That's all. Then open that address on the phone (see "On the phone" below).


Option 2: Netlify (free, about 5 minutes, no technical knowledge)
-----------------------------------------------------------------
1. On a computer, go to  https://app.netlify.com/drop
2. Sign up for a free account if asked.
3. Drag this whole folder onto the page.
4. Netlify gives you an address like  https://something-random.netlify.app
   You can rename it under Site configuration > Change site name.
5. To update the app later, open the site in Netlify, go to Deploys and drag
   the updated folder in again.


Option 3: GitHub Pages (free)
-----------------------------
Create a repository, upload these files, then Settings > Pages > deploy from
the main branch. The address will be  https://<username>.github.io/<repo>/


On the phone
------------
1. Open the address in Chrome.
2. Tap the three-dot menu > "Add to home screen" (or "Install app"), or use
   the "Install on this phone" button at the bottom of the app.
3. Open it once with signal so it saves itself for offline use.
4. The first time he taps "Set location here", allow location.


Updating the machine dimensions
-------------------------------
The machine settings are near the top of the script in index.html, in the
block marked MACHINE SETTINGS. Keep them the same as the D block in the
SketchUp script (s20_rig.rb).

After changing any file, open sw.js and change VERSION (e.g. s20-reach-v1 to
s20-reach-v2), then upload again. Phones pick up the new version the next
time the app is opened with signal.


Data
----
Jobs, points and photos are stored on the phone only. Use "Send to the office"
before deleting a job or clearing Chrome's data.
