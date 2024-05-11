# XenForo-Link-Filter

###### （Currently no Chinese Doc Tip）暂未制作简体中文版本文档，将在后续更新。  中文文档

#### refer.min.js is old version of Link Filter.For use as an external js,please use these 2 js in LinkRefer folder.

Shortly Describe: You can use your own link filter service to process all of link in your XF forum.
Eg: https://example.com will link to https://yourservice.com/?url=https://example.com
So that you can block or remind user will enter a external website or etc.

-------
### We also have an addon that can configureable at XenForo Admin CP. Download at [Releases](https://github.com/Tss-Website/XenForo-Link-Filter/releases).

## Usage:
##### As an external js:
- Put `refer.min.js` and `whitelist.js` in your server.
- Edit `whitelist.js`, you need to input urls that you dont want process by your link filter.Remember that this is an array, do not break it format or it may not work.
- Edit `refer.min.js`, you need to change ` item.href="https://api.tsfk.top/refer/?url="+encodeURIComponent(item.href) ` at the EOF to your own link filter service, and it should accept a url parameter to show the link.
- Put following content `<xf:js src="//your_js_url.com/refer.min.js" /> <xf:js src="//your_js_url.com/whitelist.js" />` in your `PAGE_CONTAINER` template.
- You are now complete all of settings.
##### As an addon:
- Configure it in your `Addons- This Addon- Options` in your XF AdminCP.

#### Note: If you choose to use addon, only have Simplified Chinese as a language support.
