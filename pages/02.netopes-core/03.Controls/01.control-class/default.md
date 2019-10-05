---
title: 'Control'
visible: true
---

##Control abstract class
Most controls extend this abstract Control.


##Global options list

- 'no_label' (bool): Indicates if control is rendered without label (default FALSE) 
- 'postable' (bool): Indicates if control is automatically posted/submitted via AJAX (default TRUE) 
- 'container' (bool): Indicates if control is rendered with container (default TRUE)
- 'tag_id' (string|null): HTML tag **id** attribute value
- 'tag_name' (string|null): HTML tag **name** attribute value (defaults to 'tag_id')
- 'class' (string|null): HTML tag **class** attribute value (CSS class)
- 'style' (string|null): HTML tag **style** attribute value (inline CSS class)
- 'extra_tag_params' (string|null): HTML tag extra attributes