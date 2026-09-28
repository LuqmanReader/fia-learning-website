REVISION HUB — HOW TO USE
==========================

FILES (keep all of these in the SAME folder — they link to each other by name)
--------------------------------------------------------------------------------
index.html            Homepage. Just a "Start" button.
hub.html              Dashboard — shows all your exams and scores. This is
                       where you edit the EXAMS list when adding a new exam.
add-exam.html         Upload tool. Turns a raw Moodle "attempt review" export
                       into a themed debrief page automatically.
fa1-mock-exam-1.html  FA1 Mock Exam 1 debrief (with explanations already written).
ma-mock-exam-1.html   Mock Exam 1 debrief (with explanations already written).


1) OPEN THE SITE
--------------------------------------------------------------------------------
Double-click index.html. Click Start. That opens hub.html, showing every
exam as a card with its score. Click any card to open its full debrief.


2) ADD A NEW EXAM ATTEMPT
--------------------------------------------------------------------------------
Step A — Export the attempt from Moodle/TYMBAFlex
  Open your finished attempt review page > right-click > Save As >
  "Webpage, HTML only" > save it somewhere you can find it.

Step B — Auto-build the basic debrief
  Open add-exam.html in your browser.
  Fill in: Subject, Exam title, Output filename.
  Upload the file you just saved.
  Click "Parse & Generate Debrief."
  Click "Download Debrief Page" — this saves a new .html file with your
  answers, the correct answers, and question text already filled in.
  Move that downloaded file into the SAME folder as the other files above.

Step C — Get detailed explanations written in (this part needs Claude)
  Come back to this chat (or start a new one) and upload the file you just
  downloaded in Step B. Ask Claude to "write the debrief explanations for
  the incorrect answers, same style as before." Claude will hand back an
  updated version of that same file — replace the one in your folder with it.

Step D — Register it on the hub
  On add-exam.html, after generating, there's a ready-made code snippet
  (subject, title, filename, score already filled in).
  Copy it. Open hub.html in a text editor. Find the EXAMS list near the
  bottom of the file (search for "var EXAMS ="). Paste your new entry in
  as one more item in that list, then save the file.
  Reload hub.html — your new exam now shows up as a card.


3) SAVING / BACKING UP YOUR DATA
--------------------------------------------------------------------------------
There's no database — every exam's data lives directly inside its own
.html file. "Saving your data" just means keeping this folder safe:
  - Keep the whole folder in a cloud-synced location (Google Drive,
    iCloud Drive, OneDrive, Dropbox) so it's backed up automatically, or
  - Zip the folder occasionally and keep a copy somewhere safe.
Do NOT lose hub.html specifically — it's the only file that remembers
which exams exist and their scores; the individual exam files are self-
contained but won't show up anywhere without an entry in hub.html.


4) IF YOU WANT IT ON A REAL WEBSITE LATER
--------------------------------------------------------------------------------
Same 5 files, drag-and-dropped into any free static host (Cloudflare
Pages, Netlify, GitHub Pages) — no changes needed to the files themselves.
