---
title: Button
visible: true
---

##Button class
Class used for rendering HTML buttons (&lt;button&gt;&lt;/button&gt;).


###Usage

<pre>
$var = new Button([options...]);
echo $var->Show();
</pre>


###Options list

#####Inherited from Control class
- 'postable' (bool): Indicates if control is automatically posted/submitted via AJAX (default FALSE) 
- 'tag_id' (string|null): HTML tag **id** attribute value
- 'tag_name' (string|null): HTML tag **name** attribute value (defaults to 'tag_id')
- 'class' (string|null): HTML tag **class** attribute value (CSS class)
- 'style' (string|null): HTML tag **style** attribute value (inline CSS class)
- 'extra_tag_params' (string|null): HTML tag extra attributes
#####Own options
- 'value' (string|null): Button content text/HTML
- 'tooltip' (string|null): Tooltip text/HTML
- 'icon' (string|null): CSS class for the button icon tag (&lt;i&gt;&lt;/i&gt;) - no icon is added if is null or empty
- 'onclick' (string|null): Javascript script (string) for the **onclick** HTML tag attribute
- 'disabled' (bool): HTML tag **disabled** attribute value (all actions are removed)
- 'disabled_on_render' (bool): If TRUE, button is disabled on render, but all actions are preserved 


###Important remarks

- For using global application theme, use NApp::$theme->GetButton[Type]Class() method:
<pre>
$var = new Button(['class'=>NApp::$theme->GetBtnPrimaryClass('extra-css-class'),other options...]);
</pre>
You can use only buttons types defined in the global application theme (class implementing ITheme interface)


###Sample code

<pre>
$button=new Button([
    'value'=>Translate::GetButton('translation_tag'),
    'class'=>NApp::$theme->GetBtnDefaultClass(),
    'icon'=>'fa fa-chevron-left',
    'onclick'=>"alert('Button click!')",
]);
echo $button->Show();
</pre>
