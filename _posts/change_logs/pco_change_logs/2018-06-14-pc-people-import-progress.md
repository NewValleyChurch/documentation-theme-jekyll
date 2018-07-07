---
title: PC People Import Progress
layout: post
permalink: 2018-06-14-pc-people-import-progress.html
comments: true
sidebar: main_sidebar
topnav: topnav
image_folder: images
document_folder: documents
categories: administration
---

#### 12:14PM

- Imported 222 records into Planning Center People updating various fields.
- Exported entire database again from People and re-loaded it into Google Sheets so it's refreshed.
- Imported CSV into Google Sheets with updated information and marked the last record edited with a blue background.
- Created some list categories and automated lists in Planning Center People.

Lists are a way to quickly build a list of people that fit a certain search criteria.  It's a bit more powerful than a simple search filter because it creates a permanent filter that regularly updates based upon the settings in each individual's record, including custom tab settings.

Lists are _not solely for the purpose of building e-mail lists_, although any given list in PCP can be synchronized to Mailchimp to create a static segment.

There is a Mailchimp list category designed specifically for lists that are intended to be synchronized with Mailchimp.  **Note: Every list created in PCP for the purpose of Mailchimp synchronization needs to contain the Opt Out criteria.**  What does this mean?  

There's an opt-out list in PCP that automatically builds a list of people who have explicitly opted out of email.  (Opting out from e-mail in mailchimp is not a 2-way synchronization, so when someone opts out, we need to update their record to reflect the same).  The opt out list in PCP is used as criteria in any list that is to become a Mailchimp static segment synchronized to PCP.  This ensures that the new list excludes people that are in the Opt Out list.