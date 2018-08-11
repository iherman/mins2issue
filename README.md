# mins2issue
Simple web based tool to convert parts of W3C minutes output into a form that can be dropped into a github issue.

## To use the tool:

Go to https://r12a.github.io/mins2issue/

Paste the URL of the minutes page into the box with the label `URL of meeting minutes`.

Select the lines you want in the page of minutes, and copy/paste them into the large box on the left.

Click on `Generate`.

Copy the highlighted result in the right-hand box, and paste it into a `Write` box in a GitHub issue.

The tool should place near the top a list of actions raised, and any resolutions taken.

Resolutions should be signalled in the minutes by the text `RESOLVED: ` followed by what was resolved. The actions are picked up from the standard Zakim output.

I haven't yet tried the tool with v2 of the W3C minutes generator.

## Example

The following:
```
fantasai: Two issues are rejected
fantasai: #14
<fantasai> https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14
fantasai: A request to forbid text emphasis from having only a color.
fantasai: We already allow this for border, etc.
astearns: Have they responded to rejection?
fantasai: I think he's ok with it but haven't found email.

tantek: I'm missing why we should do this.
... Border color is right answer, we already have this pattern.

RESOLVED: We reject issue 14 but will follow up.

fantasai: tab followed up, there was no response for a year
<tantek> tab's message URL?
<fantasai> https://lists.w3.org/Archives/Public/www-style/2015Nov/0355.html
<tantek> (was not linked from Xidorn's message)
<fantasai> because our archive software is terrible
<tantek> agreed resolve per Tab's response / explanation

<scribe> ACTION: Fantasai to contact Xidorn about issue #14
<trackbot> Created ACTION-14 - contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].
```

will be converted to:

This issue was discussed in [a meeting](https://lists.w3.org/Archives/Public/www-style/2017Feb/0049.html).

- `RESOLVED:  We reject issue 14 but will follow up.`
- `ACTION: contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].`
<details><summary>View the transcript</summary>
<b>fantasai:</b> Two issues are rejected<br/>
<b>fantasai:</b> #14<br/>
&lt;fantasai> <a href="https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14">https://drafts.csswg.org/css-text-decor-3/issues-cr-2013#issue-14</a><br/>
<b>fantasai:</b> A request to forbid text emphasis from having only a color.<br/>
<b>fantasai:</b> We already allow this for border, etc.<br/>
<b>astearns:</b> Have they responded to rejection?<br/>
<b>fantasai:</b> I think he's ok with it but haven't found email.<br/>
<b>tantek:</b> I'm missing why we should do this.<br/>
... Border color is right answer, we already have this pattern.<br/>
<b>RESOLVED:</b> We reject issue 14 but will follow up.<br/>
<b>fantasai:</b> tab followed up, there was no response for a year<br/>
<b>&lt;tantek&gt;</b> tab's message URL?<br/>
<b>&lt;fantasai&gt;</b> <a href="https://lists.w3.org/Archives/Public/www-style/2015Nov/0355.html">https://lists.w3.org/Archives/Public/www-style/2015Nov/0355.html</a><br/>
<b>&lt;tantek&gt;</b> (was not linked from Xidorn's message)<br/>
<b>&lt;fantasai&gt;</b> because our archive software is terrible<br/>
<b>&lt;tantek&gt;</b> agreed resolve per Tab's response / explanation<br/>
<b>&lt;scribe&gt;</b> ACTION: Fantasai to contact Xidorn about issue #14<br/>
<b>&lt;trackbot&gt;</b> Created ACTION-14 - contact Xidorn about issue #14 [on Fantasai - due 2017-08-17].<br/>
</details>