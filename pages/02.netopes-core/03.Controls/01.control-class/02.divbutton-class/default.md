---
title: DivButton
visible: true
---

##DivButton class
Class used for rendering HTML div buttons (&lt;div&gt;&lt;/div&gt;).


###Usage

<pre>
$var = new DivButton([options...]);
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


###Important remarks

- For using global application theme, use NApp::$theme->GetButton[Type]Class() method:
<pre>
$var = new Button(['class'=>NApp::$theme->GetBtnPrimaryClass('extra-css-class'),other options...]);
</pre>
You can use only buttons types defined in the global application theme (class implementing ITheme interface)


###Example

<pre>
$button=new DivButton([
    'value'=>Translate::GetButton('translation_tag'),
    'class'=>NApp::$theme->GetBtnDefaultClass(),
    'icon'=>'fa fa-chevron-left',
    'onclick'=>"alert('DivButton click!')",
]);
echo DivButton->Show();
</pre>