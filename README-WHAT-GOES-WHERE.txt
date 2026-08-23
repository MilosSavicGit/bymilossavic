WHAT GOES WHERE
================================================================================

THIS FOLDER = the  bymilossavic  repo (the website, bymilossavic.com)
--------------------------------------------------------------------------------
  index.html                     REPLACE the existing one
                                 - meta description + canonical added
                                 - link to the France page added in the
                                   "Naturist places, country by country" card
  naturist-beaches-france.html   NEW
  sitemap.xml                    REPLACE (old one listed only the homepage)

  img/                           YOU CREATE THIS - put the two cropped
                                 screenshots in it:
                                     img/naturist-france-overview.png
                                     img/naturist-france-languedoc.png
                                 Names must match exactly or the images break.

  Leave alone: CNAME, robots.txt, README.md, contact.html, privacy.html,
               terms.html, data-deletion.html


A DIFFERENT REPO —  BeachScout  (the app itself)
--------------------------------------------------------------------------------
  index.html   build 2.3.7. This is the one with the bug fix:

               A failed fetch of beaches/<cc>.json used to be cached exactly
               like a real answer. So going offline once killed that country
               for the rest of the session - Italy failed, the null was
               cached, and every later request returned it instantly without
               retrying, even after the connection came back. Only a reload
               cleared it. Now a 404 is cached (the file really is not there,
               that will not change) and a network failure is not (we never
               reached the server, so we learned nothing). Also carries the
               new title, meta description and canonical tag.

               It is in the  beachscout/  folder of the downloads, NOT here -
               do not mix the two index.html files up. This one is ~226 KB;
               the website one is ~17 KB.


AFTER UPLOADING
--------------------------------------------------------------------------------
  1. https://bymilossavic.com/naturist-beaches-france.html
     Both images should appear. Broken image = wrong filename or the img/
     folder did not upload with its structure.
  2. Click "Open the live map" - should reach milossavicgit.github.io/BeachScout/
  3. Check the homepage still looks right, and the new France link is visible
     in the naturist card.
