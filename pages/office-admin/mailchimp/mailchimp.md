---
title: "Mailchimp Overview"
keywords: Mailchimp
tags: mailchimp, lists
sidebar: main_sidebar
permalink: mailchimp.html
toc: false
categories: mailchimp
---

Mailchimp is the e-mail provider we use to send out bulk e-mails to specific segments of our Planning Center People database.

## How PCO Lists Integrate with Mailchimp

- When you sync a PCO list to Mailchimp, a `static` segment is created at Mailchimp.  If someone is already on the master mailing list, they are added to the segment, _unless_ they have unsubscribed, in which case they are not added.

- If someone in PCO is _not_ on the Mailchimp list, they will automatically be subscribed to the mailing list and will be added to the segment.

- If a list is created in PCO, and the same person is found on more than one list (example, you're a member AND you attended last year's conference) then you will be added to both segments on Mailchimp under a single subscriber instance.

- PCO does not sync Groups on Mailchimp.  Only segments.

- If a list is deleted from PCO, the corresponding segment is **not** removed from Mailchimp.  That must be done manually.  If you delete a segment from Mailchimp it does **not** remove the subscribers from PCO nor does it remove them from the Mailchimp list or any other segments they may be part of.

- From Mailchimp, you cannot look up a single subscriber to see which segments they are part of.  You must do that through PCO's list feature.

{% include links.html %}
