# Reader Passage Syncing Use Cases


## Use Case 1.

I have a single Reader instance and I have some widget showing a table of contents for a work. When I click on an item in the table of contents, the Reader should display that item in the TOC (or the start of it)

## Use Case 2.

I have the Passage Reference widget and a single Reader instance already open on a work. When I type in a new passage reference (within the same work) the Reader should show that passage. [CURRENT PERSEUS SCAIFE DOES THIS]

## Use Case 3.

I have a single Reader instance and a search results widget. When I click on a search result, the Reader should show the passage for the selected search result. [CURRENT PERSEUS SCAIFE DOES THIS].

## Question 4.

What happens in Use Case 1 if I then paginate in the Reader? Does the TOC widget change?

## Use Case 5.

In Use Case 2, if I then paginate in the Reader, the Passage Reference widget should change to reflect that. [CURRENT PERSEUS SCAIFE DOES THIS]

## Question 6.

What happens in Use Case 3 if I then paginate in the Reader? Presumably the selected search result in the search widget becomes deselected. But what if the pagination takes one to a passage that has another search result? Are the search terms highlighted in the reader?

## Use Case 7.

I want to read a Greek work and an English translation alongside each other. When I paginate in one, I want the other to be paginated accordingly.

## Use Case 8.

I want to read a Latin work and a commentary on that work alongside each other. I want to be able to paginate around the commentary independently of what Latin passage I have open.

## Use Case 9.

As with Use Case 8 but, while I want to paginate around the commentary independently, when I paginate the Latin text, I want the commentary to jump to the appropriate spot.

## Use Case 10.

As with Use Cases 8 and 9 but if I’m reading part of the commentary talking about a particular passage in the Latin, I want to be able to jump to that passage in the Latin.

## Use Case 11.

I want to have two distinct Greek works open along with a translation of one of them and a commentary on the other. I want the Greek work with its translation to work like Use Case 7 and the other Greek work with its commentary to work like Use Cases 8, 9, 10.

## Use Case 12.

With a single Reader on a Greek text, I want to be able to click on a word and have a dictionary entry show up in a dictionary widget.

## Use Case 13.

With two Readers, one on a Greek text and another on a Latin text (regardless of whether same text and sync’d or not), I want to be able to click on either text and have the appropriate dictionary entry show up in a single dictionary widget.

## Use Case 14. [possibly YAGNI]

As with Use Case 13 but I want two dictionary widget instances, one which shows the selected Greek word and the other which shows the selected Latin word. (So clicking on a new Greek word doesn’t change the Latin word shown and vice versa)
