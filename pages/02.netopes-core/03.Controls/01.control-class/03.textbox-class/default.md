---
title: TextBox
visible: true
---

##TextBox class
Class used for rendering HTML inputs (type="text").


###Usage

<pre>
$var = new TextBox([options...]);
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
- 'uc_first' (string|null): Auto **ucfirst** input value from javascript, on change. Allowed values are: NULL/empty=original string, **first**=only first char and **all**=first char of each word
- 'auto_select' (bool): Auto select all text on input focus (default TRUE)

###Sample code

<pre>
$textBox=new TextBox([
    'tag_id'=>'input_id',
    'tag_name'=>'input_name',
    'value'=>'initial value',
    'label'=>Translate::GetLabel('Text input'),
    'readonly'=>TRUE,
    'align'=>'center',
]);
echo $textBox->Show();
</pre>