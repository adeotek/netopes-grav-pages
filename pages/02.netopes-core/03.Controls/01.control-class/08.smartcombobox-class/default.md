---
title: 'SmartComboBox'
visible: true
---

##SmartComboBox class
Class used for rendering Select2 HTML selector.


###Usage
<pre>
$var = new SmartComboBox([]);
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
- 'value_field': 
- 'display_field': 
- 'selected_value': 
- 'selected_text':
- 'allow_clear':
- 'minimum_input_length':
- 'selected_text_field': !!!
- 'label' (string|null): Label text
- 'placeholder' (string|null): Input placeholder text
- 'readonly' (bool): HTML tag **readonly** attribute value
- 'disabled' (bool): HTML tag **disabled** attribute value
- 'label_cols' (int|null) [1-12]: If Bootstrap is used, sets the relative label width using columns CSS classes
- 'cols' (int|null) [1-12]: If Bootstrap is used, sets the relative input width in columns CSS classes
- 'onchange' (string|null): Javascript script for the **onchange** HTML tag attribute
- 'paf_property' (string|null): If set to **'function:javascriptGlobalFunction'**, on post/submit via AJAX, the value will be automatically retrieved calling the Javascript function javascriptGlobalFunction() (function must be accessible in the current scope); default Javascript global function for retrieving selectd value from Select2 is GetSmartCBOValue() (e.g. 'paf_property'=>'function:GetSmartCBOValue')
- 'load_type': 
- 'data_source': 


###Important remarks

- Do not use as AJAX parameter the '**response_type**' key (internally used to establish return data format: JSON/string/...) 


###Sample code

<pre>
$smartComboBox=new SmartComboBox([
    'tag_id'=>'input_id',
    'tag_name'=>'input_name',
    'paf_property'=>'function:GetSmartCBOValue'
    'label'=>Translate::GetLabel('select2_input'),
    'placeholder'=>Translate::GetLabel('placeholder'),
    'required'=>TRUE,
    'value_field'=>'id',
    'display_field'=>'name',
    'selected_value'=>$selectedValue,
    'allow_clear'=>TRUE,
    'minimum_input_length'=>0,
    'load_type'=>'database',
    'data_source'=>[
        'ds_class'=>'DataSource\Class',
        'ds_method'=>'Method',
        'ds_params'=>['type'=>111],
    ],
]);
echo $smartComboBox->Show();
</pre>
