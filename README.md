Context

I scraped over 18,000 Pitchfork reviews (going back to January 1999). Initially, this was done to satisfy a few of my own curiosities, but I bet Kagglers can come up with some really interesting analyses!

Content

I scraped Pitchfork on the evening of Sunday, Jan 8 2016. My scraper program got a series of 503 errors on page 1480 of the reviews, so I don't have that page, but I have the rest (18,393 reviews)!

Table: reviews

reviewid (integer). Unique review identifier.
title (text). Title of reviewed release.
artist (text). Artist name (multiple artists separated by commas).
url (text). URL to pitchfork review.
score (real). Release rating, 0.0 - 10.0.
best_new_music (boolean). Release was "Best new Music", T/F.
author (text). Name of review author.
author_type (text). Author class (contributor, associate editor, etc).
pub_date (text). String publication date (YYYY-MM-DD).
pub_weekday (integer). Publication weekday (0 = Monday, 6 = Sunday).
pub_day (integer). Publication day of month.
pub_month (integer). Publication month (1 = January).
pub_year (integer). Publication year.
Table: artists

This table comes in handy when more than one artist is associated with a given reviewid.

reviewid (integer). Unique review identifier.
artist (text). Artist name.
Table: content

reviewid (integer). Unique review identifier.
content (text). Full review.
Table: genres

This table contains a mapping between reviewid and musical genres. Note: a given reviewid may have more than one (or no) genre.

reviewid (integer). Unique review identifier.
genre (text). Genre name.
Table: labels

This table contains a mapping between reviewid and record labels. Note: a given reviewid may have more than one (or no) record label.

reviewid (integer). Unique review identifier.
label (text). Record label name.
Table: years

Sometimes Pitchfork reviews albums from the previous year (usually in early January), or from the forthcoming year (usually in December). Likewise, Pitchfork often reviews reissues and lists the original release year along with the reissue year. So it's not always safe to assume that the release year is the same as the publication year.

reviewid (integer). Unique review identifier.
year (text). Release year.
