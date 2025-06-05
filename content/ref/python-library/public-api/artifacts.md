---
title: artifacts
object_type: public_apis_namespace
data_type_classification: module
---

{{< cta-button githubLink=https://github.com/wandb/wandb/blob/main/wandb/wandb/wandb/wandb/apis/public/artifacts.py >}}




# <kbd>module</kbd> `wandb.apis.public`
Public API: artifacts. 

## <kbd>function</kbd> `server_supports_artifact_collections_gql_edges`

```python
server_supports_artifact_collections_gql_edges(
    client: 'RetryingClient',
    warn: 'bool' = False
) → bool
```






---

## <kbd>class</kbd> `ArtifactTypes`




### <kbd>method</kbd> `ArtifactTypes.__init__`

```python
__init__(client: 'Client', entity: 'str', project: 'str', per_page: 'int' = 50)
```






---

### <kbd>property</kbd> ArtifactTypes.cursor





---

### <kbd>property</kbd> ArtifactTypes.length





---

### <kbd>property</kbd> ArtifactTypes.more







---

### <kbd>method</kbd> `ArtifactTypes.convert_objects`

```python
convert_objects() → list[ArtifactType]
```





---

### <kbd>method</kbd> `ArtifactTypes.update_variables`

```python
update_variables() → None
```






---

## <kbd>class</kbd> `ArtifactType`




### <kbd>method</kbd> `ArtifactType.__init__`

```python
__init__(
    client: 'Client',
    entity: 'str',
    project: 'str',
    type_name: 'str',
    attrs: 'Mapping[str, Any] | None' = None
)
```






---

### <kbd>property</kbd> ArtifactType.id





---

### <kbd>property</kbd> ArtifactType.name







---

### <kbd>method</kbd> `ArtifactType.collection`

```python
collection(name: 'str') → ArtifactCollection
```





---

### <kbd>method</kbd> `ArtifactType.collections`

```python
collections(per_page: 'int' = 50) → ArtifactCollections
```

Artifact collections. 

---

### <kbd>method</kbd> `ArtifactType.load`

```python
load() → Mapping[str, Any]
```






---

## <kbd>class</kbd> `ArtifactCollections`




### <kbd>method</kbd> `ArtifactCollections.__init__`

```python
__init__(
    client: 'Client',
    entity: 'str',
    project: 'str',
    type_name: 'str',
    per_page: 'int' = 50
)
```






---

### <kbd>property</kbd> ArtifactCollections.cursor





---

### <kbd>property</kbd> ArtifactCollections.length





---

### <kbd>property</kbd> ArtifactCollections.more







---

### <kbd>method</kbd> `ArtifactCollections.convert_objects`

```python
convert_objects() → list[ArtifactCollection]
```





---

### <kbd>method</kbd> `ArtifactCollections.update_variables`

```python
update_variables() → None
```






---

## <kbd>class</kbd> `ArtifactCollection`




### <kbd>method</kbd> `ArtifactCollection.__init__`

```python
__init__(
    client: 'Client',
    entity: 'str',
    project: 'str',
    name: 'str',
    type: 'str',
    organization: 'str | None' = None,
    attrs: 'Mapping[str, Any] | None' = None,
    is_sequence: 'bool | None' = None
)
```






---

### <kbd>property</kbd> ArtifactCollection.aliases

Artifact Collection Aliases. 

---

### <kbd>property</kbd> ArtifactCollection.created_at





---

### <kbd>property</kbd> ArtifactCollection.description

A description of the artifact collection. 

---

### <kbd>property</kbd> ArtifactCollection.id





---

### <kbd>property</kbd> ArtifactCollection.name

The name of the artifact collection. 

---

### <kbd>property</kbd> ArtifactCollection.tags

The tags associated with the artifact collection. 

---

### <kbd>property</kbd> ArtifactCollection.type

The type of the artifact collection. 



---

### <kbd>method</kbd> `ArtifactCollection.artifacts`

```python
artifacts(per_page: 'int' = 50) → Artifacts
```

Artifacts. 

---

### <kbd>method</kbd> `ArtifactCollection.change_type`

```python
change_type(new_type: 'str') → None
```

Deprecated, change type directly with `save` instead. 

---

### <kbd>method</kbd> `ArtifactCollection.delete`

```python
delete() → None
```

Delete the entire artifact collection. 

---

### <kbd>method</kbd> `ArtifactCollection.is_sequence`

```python
is_sequence() → bool
```

Return whether the artifact collection is a sequence. 

---

### <kbd>method</kbd> `ArtifactCollection.load`

```python
load()
```





---

### <kbd>method</kbd> `ArtifactCollection.save`

```python
save() → None
```

Persist any changes made to the artifact collection. 


---

## <kbd>class</kbd> `Artifacts`
An iterable collection of artifact versions associated with a project and optional filter. 

This is generally used indirectly via the `Api`.artifact_versions method. 

### <kbd>method</kbd> `Artifacts.__init__`

```python
__init__(
    client: 'Client',
    entity: 'str',
    project: 'str',
    collection_name: 'str',
    type: 'str',
    filters: 'Mapping[str, Any] | None' = None,
    order: 'str | None' = None,
    per_page: 'int' = 50,
    tags: 'str | list[str] | None' = None
)
```






---

### <kbd>property</kbd> Artifacts.cursor





---

### <kbd>property</kbd> Artifacts.length





---

### <kbd>property</kbd> Artifacts.more







---

### <kbd>method</kbd> `Artifacts.convert_objects`

```python
convert_objects() → list[Artifact]
```






---

## <kbd>class</kbd> `RunArtifacts`




### <kbd>method</kbd> `RunArtifacts.__init__`

```python
__init__(
    client: 'Client',
    run: 'Run',
    mode: "Literal['logged', 'used']" = 'logged',
    per_page: 'int' = 50
)
```






---

### <kbd>property</kbd> RunArtifacts.cursor





---

### <kbd>property</kbd> RunArtifacts.length





---

### <kbd>property</kbd> RunArtifacts.more







---

### <kbd>method</kbd> `RunArtifacts.convert_objects`

```python
convert_objects() → list[Artifact]
```






---

## <kbd>class</kbd> `ArtifactFiles`




### <kbd>method</kbd> `ArtifactFiles.__init__`

```python
__init__(
    client: 'Client',
    artifact: 'Artifact',
    names: 'Sequence[str] | None' = None,
    per_page: 'int' = 50
)
```






---

### <kbd>property</kbd> ArtifactFiles.cursor





---

### <kbd>property</kbd> ArtifactFiles.length





---

### <kbd>property</kbd> ArtifactFiles.more





---

### <kbd>property</kbd> ArtifactFiles.path







---

### <kbd>method</kbd> `ArtifactFiles.convert_objects`

```python
convert_objects() → list[public.File]
```





---

### <kbd>method</kbd> `ArtifactFiles.update_variables`

```python
update_variables() → None
```






