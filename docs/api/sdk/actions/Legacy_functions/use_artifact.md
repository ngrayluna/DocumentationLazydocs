---
title: use_artifact()
object_type: python_sdk_actions
data_type_classification: function
---

{{< cta-button githubLink=https://github.com/wandb/wandb/blob/main/wandb/wandb/wandb/wandb/sdk/lib/preinit.py >}}




### <kbd>function</kbd> `wandb.use_artifact`

```python
wandb.use_artifact(
    artifact_or_name: 'str | Artifact',
    type: 'str | None' = None,
    aliases: 'list[str] | None' = None,
    use_as: 'str | None' = None
) → Artifact
```

Declare an artifact as an input to a run. 

Call `download` or `file` on the returned object to get the contents locally. 



**Args:**
 
 - `artifact_or_name`:  (str or Artifact) An artifact name.  May be prefixed with project/ or entity/project/.  If no entity is specified in the name, the Run or API setting's entity is used.  Valid names can be in the following forms: 
            - name:version 
            - name:alias  You can also pass an Artifact object created by calling `wandb.Artifact` 
 - `type`:  (str, optional) The type of artifact to use. 
 - `aliases`:  (list, optional) Aliases to apply to this artifact 
 - `use_as`:  This argument is deprecated and does nothing. 



**Returns:**
 An `Artifact` object. 
