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
<fantasai> https://drafts.csswg.org/css-text-3/issues-lc-2013#issue-172

github: https://github.com/w3c/csswg-drafts/issues/2233

fantasai: We asked for i118n feedback. Wanted to check with WG as well. You have some text and at the end of the line you have whitepsace and mixed in there are bidi control characters. Does the whitespace collapse?

florian: If instead of bidi control characters you have markup with the eq. bidi commands we collapse through.

myles: Reason to not collapse is if there's a character user can see. This is not that. It should collapse.

florian: Spec says that but I don't believe anyone does that.

florian: CSS2 and CSS Text 3 says it must collapse.

fantasai: Keep spec as is and file bugs?

myles: THis is a thing we should do.

koji: WE make bidi controls follow collapsing.

astearns: Text 3 is where in process?

fantasai: LC

astearns: It'll have to be at risk if we still don't have impl.

fantasai: I'm happy for at risk.

<eae> (to clarify, in our new layout engine we do collapse through bidi control characters. the current layout engine does not)

fantasai: Mark it as at risk and if no one impl we say we want to do it this way.

astearns: Close no change?

florian: Mark at risk?

RESOLVED: Keep but mark at risk

fremy: Edge does this

fantasai: koji says Chrome will.

RESOLVED: Just keep, don't mark at risk.
```

will be converted to:

This issue was discussed in [a meeting](https://github.com/r12a/mins2issue/edit/gh-pages/README.md).

- `RESOLVED:  Keep but mark at risk`
- `RESOLVED:  Just keep, don't mark at risk.`
<details><summary>View the transcript</summary>
&lt;fantasai> <a href="https://drafts.csswg.org/css-text-3/issues-lc-2013#issue-172">https://drafts.csswg.org/css-text-3/issues-lc-2013#issue-172</a><br/>
<b>github:</b> <a href="https://github.com/w3c/csswg-drafts/issues/2233">https://github.com/w3c/csswg-drafts/issues/2233</a><br/>
<b>fantasai:</b> We asked for i118n feedback. Wanted to check with WG as well. You have some text and at the end of the line you have whitepsace and mixed in there are bidi control characters. Does the whitespace collapse?<br/>
<b>florian:</b> If instead of bidi control characters you have markup with the eq. bidi commands we collapse through.<br/>
<b>myles:</b> Reason to not collapse is if there's a character user can see. This is not that. It should collapse.<br/>
<b>florian:</b> Spec says that but I don't believe anyone does that.<br/>
<b>florian:</b> CSS2 and CSS Text 3 says it must collapse.<br/>
<b>fantasai:</b> Keep spec as is and file bugs?<br/>
<b>myles:</b> THis is a thing we should do.<br/>
<b>koji:</b> WE make bidi controls follow collapsing.<br/>
<b>astearns:</b> Text 3 is where in process?<br/>
<b>fantasai:</b> LC<br/>
<b>astearns:</b> It'll have to be at risk if we still don't have impl.<br/>
<b>fantasai:</b> I'm happy for at risk.<br/>
<b>&lt;eae&gt;</b> (to clarify, in our new layout engine we do collapse through bidi control characters. the current layout engine does not)<br/>
<b>fantasai:</b> Mark it as at risk and if no one impl we say we want to do it this way.<br/>
<b>astearns:</b> Close no change?<br/>
<b>florian:</b> Mark at risk?<br/>
<b>RESOLVED:</b> Keep but mark at risk<br/>
<b>fremy:</b> Edge does this<br/>
<b>fantasai:</b> koji says Chrome will.<br/>
<b>RESOLVED:</b> Just keep, don't mark at risk.<br/>
</details>
