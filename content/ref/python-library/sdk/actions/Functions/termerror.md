---
title: termerror()
object_type: python_sdk_actions
data_type_classification: function
---

{{< cta-button githubLink=https://github.com/wandb/wandb/blob/main/wandb/wandb/wandb/wandb/errors/term.py >}}




### <kbd>function</kbd> `termerror`

```python
termerror(
    string: 'str',
    newline: 'bool' = True,
    repeat: 'bool' = True,
    prefix: 'bool' = True
) → None
```

Log an error to stderr. 

The arguments are the same as for `termlog()`. 
