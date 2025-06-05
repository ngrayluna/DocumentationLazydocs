---
title: Settings
object_type: python_sdk_actions
data_type_classification: class
---

{{< cta-button githubLink=https://github.com/wandb/wandb/blob/main/wandb/wandb/wandb/wandb/sdk/wandb_settings.py >}}




## <kbd>class</kbd> `Settings`
Settings for the W&B SDK. 

This class manages configuration settings for the W&B SDK, ensuring type safety and validation of all settings. Settings are accessible as attributes and can be initialized programmatically, through environment variables (WANDB_ prefix), and via configuration files. 

The settings are organized into three categories: 1. Public settings: Core configuration options that users can safely modify to customize  W&B's behavior for their specific needs. 2. Internal settings: Settings prefixed with 'x_' that handle low-level SDK behavior.  These settings are primarily for internal use and debugging. While they can be modified,  they are not considered part of the public API and may change without notice in future  versions. 3. Computed settings: Read-only settings that are automatically derived from other settings or  the environment. 


---

### <kbd>property</kbd> Settings.colab_url

The URL to the Colab notebook, if running in Colab. 

---

### <kbd>property</kbd> Settings.deployment





---

### <kbd>property</kbd> Settings.files_dir

Absolute path to the local directory where the run's files are stored. 

---

### <kbd>property</kbd> Settings.is_local





---

### <kbd>property</kbd> Settings.log_dir

The directory for storing log files. 

---

### <kbd>property</kbd> Settings.log_internal

The path to the file to use for internal logs. 

---

### <kbd>property</kbd> Settings.log_symlink_internal

The path to the symlink to the internal log file of the most recent run. 

---

### <kbd>property</kbd> Settings.log_symlink_user

The path to the symlink to the user-process log file of the most recent run. 

---

### <kbd>property</kbd> Settings.log_user

The path to the file to use for user-process logs. 

---

### <kbd>property</kbd> Settings.model_extra

Get extra fields set during validation. 



**Returns:**
  A dictionary of extra fields, or `None` if `config.extra` is not set to `"allow"`. 

---

### <kbd>property</kbd> Settings.model_fields_set

Returns the set of fields that have been explicitly set on this model instance. 



**Returns:**
  A set of strings representing the fields that have been set,  i.e. that were not filled from defaults. 

---

### <kbd>property</kbd> Settings.project_url

The W&B URL where the project can be viewed. 

---

### <kbd>property</kbd> Settings.resume_fname

The path to the resume file. 

---

### <kbd>property</kbd> Settings.run_mode





---

### <kbd>property</kbd> Settings.run_url

The W&B URL where the run can be viewed. 

---

### <kbd>property</kbd> Settings.settings_workspace

The path to the workspace settings file. 

---

### <kbd>property</kbd> Settings.sweep_url

The W&B URL where the sweep can be viewed. 

---

### <kbd>property</kbd> Settings.sync_dir





---

### <kbd>property</kbd> Settings.sync_file

Path to the append-only binary transaction log file. 

---

### <kbd>property</kbd> Settings.sync_symlink_latest





---

### <kbd>property</kbd> Settings.timespec





---

### <kbd>property</kbd> Settings.wandb_dir

Full path to the wandb directory. 



---

### <kbd>classmethod</kbd> `Settings.catch_private_settings`

```python
catch_private_settings(values)
```

Check if a private field is provided and assign to the corresponding public one. 

This is a compatibility layer to handle previous versions of the settings. 

---

### <kbd>method</kbd> `Settings.to_proto`

```python
to_proto() → wandb_settings_pb2.Settings
```

Generate a protobuf representation of the settings. 

---

### <kbd>method</kbd> `Settings.update_from_dict`

```python
update_from_dict(settings: 'Dict[str, Any]') → None
```

Update settings from a dictionary. 

---

### <kbd>method</kbd> `Settings.update_from_env_vars`

```python
update_from_env_vars(environ: 'Dict[str, Any]')
```

Update settings from environment variables. 

---

### <kbd>method</kbd> `Settings.update_from_settings`

```python
update_from_settings(settings: 'Settings') → None
```

Update settings from another instance of `Settings`. 

---

### <kbd>method</kbd> `Settings.update_from_system_config_file`

```python
update_from_system_config_file()
```

Update settings from the system config file. 

---

### <kbd>method</kbd> `Settings.update_from_system_environment`

```python
update_from_system_environment()
```

Update settings from the system environment. 

---

### <kbd>method</kbd> `Settings.update_from_workspace_config_file`

```python
update_from_workspace_config_file()
```

Update settings from the workspace config file. 

---

### <kbd>classmethod</kbd> `Settings.validate_api_key`

```python
validate_api_key(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_base_url`

```python
validate_base_url(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_code_dir`

```python
validate_code_dir(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_console`

```python
validate_console(value, values)
```





---

### <kbd>classmethod</kbd> `Settings.validate_file_stream_max_line_bytes`

```python
validate_file_stream_max_line_bytes(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_fork_from`

```python
validate_fork_from(value, values) → Optional[RunMoment]
```





---

### <kbd>classmethod</kbd> `Settings.validate_http_proxy`

```python
validate_http_proxy(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_https_proxy`

```python
validate_https_proxy(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_ignore_globs`

```python
validate_ignore_globs(value)
```





---

### <kbd>method</kbd> `Settings.validate_mutual_exclusion_of_branching_args`

```python
validate_mutual_exclusion_of_branching_args() → Self
```





---

### <kbd>classmethod</kbd> `Settings.validate_program`

```python
validate_program(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_program_abspath`

```python
validate_program_abspath(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_program_relpath`

```python
validate_program_relpath(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_project`

```python
validate_project(value, values)
```





---

### <kbd>classmethod</kbd> `Settings.validate_resume`

```python
validate_resume(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_resume_from`

```python
validate_resume_from(value, values) → Optional[RunMoment]
```





---

### <kbd>classmethod</kbd> `Settings.validate_root_dir`

```python
validate_root_dir(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_run_id`

```python
validate_run_id(value, values)
```





---

### <kbd>classmethod</kbd> `Settings.validate_service_wait`

```python
validate_service_wait(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_settings_system`

```python
validate_settings_system(value)
```





---

### <kbd>method</kbd> `Settings.validate_skip_transaction_log`

```python
validate_skip_transaction_log()
```





---

### <kbd>classmethod</kbd> `Settings.validate_start_method`

```python
validate_start_method(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_stats_open_metrics_endpoints`

```python
validate_stats_open_metrics_endpoints(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_stats_open_metrics_filters`

```python
validate_stats_open_metrics_filters(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_stats_open_metrics_http_headers`

```python
validate_stats_open_metrics_http_headers(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_stats_sampling_interval`

```python
validate_stats_sampling_interval(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_sweep_id`

```python
validate_sweep_id(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_sweep_param_path`

```python
validate_sweep_param_path(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_x_executable`

```python
validate_x_executable(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_x_files_dir`

```python
validate_x_files_dir(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_x_stats_coreweave_metadata_base_url`

```python
validate_x_stats_coreweave_metadata_base_url(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_x_stats_gpu_device_ids`

```python
validate_x_stats_gpu_device_ids(value)
```





---

### <kbd>classmethod</kbd> `Settings.validate_x_stats_neuron_monitor_config_path`

```python
validate_x_stats_neuron_monitor_config_path(value)
```





