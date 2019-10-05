---
title: Button
visible: true
---

##Button class
Class used for rendering HTML buttons (&lt;button&gt;&lt;/button&gt;).


###Sample code
<pre>
$var = new Button([options...]);
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


###Example

<pre>
$button=new Button([
    'value'=>Translate::GetButton('translation_tag'),
    'class'=>NApp::$theme->GetBtnDefaultClass(),
    'icon'=>'fa fa-chevron-left',
    'onclick'=>"alert('Button click!')",
]);
echo $button->Show();
</pre>
