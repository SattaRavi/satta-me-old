---
date: 2017-01-15T22:50:18-07:00
paging: true
title: GA Language Spam
tags: ['GA', 'Analytics']
---

Language spam as the name suggests pollutes the language dimension thereby affecting related views, metrics & reports on GA. This is similar to the common GA referrer spam and has been seen a lot since late Oct 2016.

> img

GA accepts any of the [ISO 639–2](https://www.loc.gov/standards/iso639-2/php/code_list.php) Language codes set on the browser. Even though the browser APIs expose the locale or user-language settings to be a read only, it can be tampered with before ga.js sends a beacon to the google servers.

> GIST

Once the traffic is recorded by GA it is impossible to delete or edit the data. so cleaning up the language spam takes 2 steps.

1. Block future language spam traffic.
2. Filter out historic spam data.

### 1. Block future language spam traffic

To prevent the language spam in the future we create a view filter with the below regular expression to exclude traffics that has more than 8 symbols (ISO 639–2) in the language field.

```.{8,}|\s[^s]*\s|\.|,|\!|\/```

Hit the **verify this filter** to dry run it against past weeks traffic data.

> img

### 2. Filter out historic spam data

For damage control create a segment using the same regular expression from above to exclude all language spam traffic.

The demerit is that this segment has to be applied every time a report is pulled with a date range that matches the recorded language spam date range.

> img

