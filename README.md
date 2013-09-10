bootstrap-disabled-tabclick
===========================

Refer to Bootstrap 3 Document. Link functionality not impacted when added .disabled to li. Here is the solution

<h1>Introduction</h1>

<i>*Notice message copied from Bootstrap 3 Document</i>
<br/>
<b>Disabled links</b>
<br/>
For any nav component (tabs, pills, or list), add .disabled for gray links and no hover effects.
Link functionality not impacted
This class will only change the &lt;a&gt;'s appearance, not its functionality. Use custom JavaScript to disable links here.

Normally, Bootstrap 3 doesn't implements the function to disable link functionality. We need to implement by ourselves. 
The following described how to manage this issue.

<h1>Requirements</h1>
1. Bootstrap 3 (Untested with < 2)
2. jQuery 1.10.2

<h1>How to</h1>
<br/>
First of all, you need to create a Bootstrap nav-tabs like this example, assign id for &lt;ul&gt; and each &lt;li&gt;, &lt;a&gt;

```html
 <ul class="nav nav-tabs" id="myTab">
   <li id="body_tabHeaderWorkDetail" class="active"><a href="#workDetail" id="body_lnkHeaderWorkDetail" data-toggle="tab">Work Detail</a></li>
   <li id="body_tabHeaderDocument"><a href="#document" id="body_lnkHeaderDocument" data-toggle="tab">Document</a></li>
   <li id="body_tabHeaderGuarantee" class="disabled"><a href="#guarantee" id="body_lnkHeaderGuarantee" data-toggle="tab">Guarantee</a></li>
   <li id="body_tabHeaderAttachFile" class="disabled"><a href="#attachFile" id="body_lnkHeaderAttachFile" data-toggle="tab">Attach File</a></li>
 </ul>
```

After you finish with this markup, just import a javascript library to your website like this

```html
<script src="/js/bootstrap-disabled-tabclick.js" type="text/javascript"></script>
```

Then the script will manage it for you. When you click to the disabled tab, script will active to your last tab automatically.
