[Development](/development.html) >

# Stand-off Tables of Contents

Motivation:

* reading lists (e.g. here is a list of passages to read for this course)
* topical guides (e.g. here is a list of passages on this topic)
* groupings of works other than by CTS hierarchy (e.g. Apostolic Fathers, grouping of a work with a commentary)
* alternative structures placed over works (e.g. Homer "cards" or New Testament "pericopes")

In the canonical use case, these TOCs are hand-produced but they could be derived from other machine-actionable data either in the text markup itself (e.g. milestones) or external metadata. For the purposes of an MVP, I think we can assume they come as a static representation (see **Structure** below) and that we don't need to worry in the context of this epic how that representation was produced.

## Structure

At least for an MVP:

* identifer for the TOC (CITE URN?)
* title of TOC
* ordered list of:
  * item title
  * CTS URN

In the canonical use case, the CTS URNs are passages but there are use cases where they could be works or text groups or even other objects (in particular, other TOCs, for which see below).

For some cases, an optional description field for the overall TOC would be useful.

Q1: should a hierarchy be supported? The current mockups for Brill have a two-level hierarchy but (how) do we generalise that? If TOC items can be other TOCs, we can do it that way but that might involve too many clicks for some use cases.

Q2: what does it mean for the CTS URN to point to something higher than a passage? (In particular if the TOC is being accessed in a widget in the reader)

Other potential expansions on the structure:

* keywords
* scope (see below)

Both of these help with discovering of appropriate TOCs.

## Data Format

We should establish a data format for importing and (potentially) exporting the TOCs.

## Data API

We need to establish the API for retrieving the TOC data. We should consider existing collection APIs (e.g. DTS) for this sort of thing (especially if we do decide to support hierarchy and have needs for things like pagination). 

Because we want this to work both with ATLAS and a Nautilus-based Scaife, we should not make assumptions in the API about how texts themselves are served. Even if we implement the API in ATLAS or in the Django backend of the Nautilus-based Scaife, it should be treated like a separate microservice.

## User Experience

* TOCs should be displayed both as a widget and as individual pages.
* On a separate page, this gives them web addresses.
* The number of items in lists may be long as so we may need to support typeahead filtering and pagination
* In a widget there is the question of how a user decides which TOC(s) to display.
* It would be nice to support the display of multiple TOCs simulateously (potentially in multiple widgets).
* The TOCs selection could itself be a separate widget (and page).
* TOCs themselves could be grouped as a TOC (which would provide a potential solution for TOC selection)
* It would be useful (possibly as a latest step) to reverse index TOCs so the API can say which TOCs contain the passage currently being read.
* Apart from the reverse index, it might be useful to be able to scope a list to a work or textgroup (e.g. say "this TOC is relevant to Homer, or the New Testament)
* This could be achieved explicitly by library nodes having metadata indicating a TOC (of TOCs) to show for that node.

## Other Related Features / Epics / Considerations

* an entire library-like functionality could be built with this but we don't have to start with this in mind
* it would be useful if the TOCs could be used independently of the rest of Scaife for things like vocab.perseus.org
* the TOCs could (eventually) be a way to capture the results of a search or library filter
* the TOCs could (eventually) be a way to manage bookmarks too
