# Blogs #

## Philosophy ##

## Blog Structure ##

Rank | Item
-----|-----
1 | Blog
2 | Page
3 | Post


This is a resource/reference file for blog environment declarations.


Environments:
  - Blog    (Entire Site)
  - Page    (Site Page)
  - Search  (Site Query)
  - Post    (Page Part)
  - Comment (Post+User-Dependent)
  - Request (Query)

Variables:
  » {block:<Object>}   (for is every <Object>)
  » {if:<Object>}      (If <Object> exists)
  » {select:<Object>}  (Selected <Object> from list)
  » {color:<Object>}   (Color of <Object>)
  » {font:<Object>}    (Font of <Object>)
  » {src:<Object>}     (Source of <Object>)
  » {stat:<Object>}    (Statistics of <Object>)
  » {text:<Container>} (Text contained within <Container>)
  

Blog:  
────────────────
- blog-head
- blog-meta
- blog-body
- blog-side
- blog-foot

  blog-head:
  - blog-title
  - blog-description
  - blog-banner
  - blog-topic
  - blog-avatar
  - blog-nav

  blog-meta:
  - author
  - og:*
  - twitter:*
  
  blog-body:
  - page
  
  blog-side:
  - left-bar
  - right-bar
  - social-links
  
  blog-foot:
  - foot-copy
  - blog-date
  - foot-links
  - foot-logo

  blog-form:
  - blog-embed
  - blog-page
  - blog-feed

Page:
────────────────
- page-head
- page-meta
- page-body
- page-foot

  page-head:
  - page-title
  - page-description

  page-meta:
  - isPost
  - isExtLink (AKA Feed)
  - isBlog

  page-body:
  - post-container
  - sidebar

  page-foot:
  - page-nav (pagination)
  - page-view

Post:  
────────────────
- post-head
- post-meta
- post-body
- post-foot

post-head:
  - post-title  (present in types: audio,chat,link,photo[photoset],text,video)
  - post-author (int-usr or ext-usr)
  - post-date   (dd-mm-[yy]yy or yyyy-mm-dd)

post-meta:
  - post-tag  (i.e. #tag, #tag or #tag #tag )
  - post-type (i.e. audio, chat, link, photo[single,panorama,photoset], quote, text, video)

post-body:
  - post-content
  - post-description (present in types: audio,chat,link,photo,quote,text,video)

post-foot:
  - post-share
  - post-reblog
  - post-like
  - post-note

post-form:
  - post-embed
  - post-page
  - post-archive

Comment:  
────────────────
- comment-head
- comment-body
- comment-foot

  comment-head:
  - comment-user
  - comment-date
  - comment-target

  comment-body:
  - comment-title
  - comment-content

  comment-foot:
  - comment-report
  - comment-share
  - comment-reblog
  - comment-like

Request:
────────────────
- request-meta
- request-body

  request-meta:
  - request-id
  - request-type  (i.e. ask, submit, edit, remove, report)
  - request-user

  request-body:
  - request-content

Search:
────────────────
- search-filter
- search-input



Social-Network:

Dribble - 
Facebook - 
Flickr / Instagram / DevianArt / - Photo/Art
Google + - 
LinkedIn - Portfolio
Kickstarter / Patreon - Fundraising/Support
Soundcloud / Spotify - Audio
Twitter - Microblog/Stream Update[RSS]
Tumblr - 
Vimeo / Youtube - Video



Images

Admittedly, it’s fairly difficult to devise a “natural” syntax for placing images into a plain text document format.

Markdown uses an image syntax that is intended to resemble the syntax for links, allowing for two styles: inline and reference.

Inline image syntax looks like this:

![Alt text](/path/to/img.jpg)

![Alt text](/path/to/img.jpg "Optional title")

That is:

    An exclamation mark: !;
    followed by a set of square brackets, containing the alt attribute text for the image;
    followed by a set of parentheses, containing the URL or path to the image, and an optional title attribute enclosed in double or single quotes.

Reference-style image syntax looks like this:

![Alt text][id]

Where “id” is the name of a defined image reference. Image references are defined using syntax identical to link references:

[id]: url/to/image  "Optional title attribute"


(This sort of entity-encoding trick will indeed fool many, if not most, address-harvesting bots, but it definitely won’t fool all of them. It’s better than nothing, but an address published in this way will probably eventually start receiving spam.)

Backslash Escapes

Markdown provides backslash escapes for the following characters:

\   backslash
`   backtick
*   asterisk
_   underscore
{}  curly braces
[]  square brackets
()  parentheses
#   hash mark
+   plus sign
-   minus sign (hyphen)
.   dot
!   exclamation mark
