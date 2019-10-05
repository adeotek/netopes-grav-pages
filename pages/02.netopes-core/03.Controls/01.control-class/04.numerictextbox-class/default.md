---
title: NumericTextBox
visible: true
---

##NumericTextBox class
Class used for rendering HTML inputs (type="text" allowing only numeric values).


###Usage
<pre>
$var = new NumericTextBox([options...]);
echo $var->Show();
</pre>


###Options list

#####Inherited from Control class
- 'no_label' (bool): Indicates if control is rendered without label (default FALSE) 
- 'postable' (bool): Indicates if control is automatically posted/submitted via AJAX (default TRUE) 
- 'container' (bool): Indicates if control is rendered with container (default TRUE)
- 'tag_id' (string|null): HTML tag **id** attribute value
- 'tag_name' (string|null): HTML tag **name** attribute value (defaults to 'tag_id')
- 'class' (string|null): HTML tag **class** attribute value (CSS class)
- 'style' (string|null): HTML tag **style** attribute value (inline CSS class)
- 'extra_tag_params' (string|null): HTML tag extra attributes
#####Own options
- 'value' (string|null): Input content (value attribute)
- 'label' (string|null): Label text
- 'placeholder' (string|null): Input placeholder text
- 'readonly' (bool): HTML tag **readonly** attribute value
- 'disabled' (bool): HTML tag **disabled** attribute value
- 'align' (string|null): Content alignment: left/right/center (default left) 
- 'label_cols' (int|null) [1-12]: If Bootstrap is used, sets the relative label width using columns CSS classes
- 'cols' (int|null) [1-12]: If Bootstrap is used, sets the relative input width in columns CSS classes
- 'onchange' (string|null): Javascript script for the **onchange** HTML tag attribute
- 'auto_select' (bool): Auto select all text on input focus (default TRUE)
- 'number_format' (string|null): Number formatting in custom format **'dn|ds|gs|pf'** where: dn=number of decimals, ds=decimal separator symbol, gs=group separator symbol and pf=optional string suffix
- 'paf_property' (string|null): If set to **'nvalue'**, on post/submit via AJAX, the value will be automatically converted to numeric value using the format set by **number_format** option 


###Sample code

<pre>
$numericTextBox=new NumericTextBox([
    'tag_id'=>'input_id',
    'tag_name'=>'input_name',
    'value'=>123.44,
    'label'=>Translate::GetLabel('Numeric input'),
    'readonly'=>TRUE,
    'align'=>'center',
    'number_format'=>'2|,|.| %',
    'paf_property'=>'nvalue',
]);
echo $numericTextBox->Show();
</pre>

