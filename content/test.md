---
title: "Testa MarkDown"
views:
    column1:
        region: sidebar-left
        template: anax/v2/block/default
        data:
            meta:
                type: single
                route: block/om-kursrepo
    column2:
        region: sidebar-right
        template: anax/v2/block/default
        data:
            meta:
                type: single
                route: block/om-redovisa
    byline:
        region: main
        template: anax/v2/block/default
        sort: 2
        data:
            meta:
                type: single
                route: block/byline


---
Sida för att testa Markdown
=========================
Lek med olika konstruktioner.
<h1>En huvudrubrik</h1>
<h2>En underrubrik</h2>
<p style="color: blue;">En blå brödtext</p>
En vanlig brödtext
