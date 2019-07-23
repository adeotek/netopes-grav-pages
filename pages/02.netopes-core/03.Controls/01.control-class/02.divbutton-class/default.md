---
title: DivButton
visible: true
---

##Button class
Class used for rendering HTML div buttons (&lt;div&gt;&lt;/div&gt;).


###Sample code
<pre>
$var = new DivButton([button options...]);
echo $var->Show();
</pre>


###Options list

- 'value': Button content text/HTML
- 'tooltip': Tooltip text/HTML
- 'icon': CSS class for the button icon tag (&lt;i&gt;&lt;/i&gt;) - no icon is added if is null or empty
- 'onclick': Javascript script (string) for the **onclick** HTML tag attribute


###Important remarks

- For using global application theme, use NApp::$theme->GetButton[Type]Class() method:
<pre>
$var = new Button(['class'=>NApp::$theme->GetBtnPrimaryClass('extra-css-class'),other options...]);
</pre>
You can use only buttons types defined in the global application theme (class implementing ITheme interface)