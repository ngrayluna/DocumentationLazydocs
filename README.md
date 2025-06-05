# DocumentationLazydocsTesting

This repo exists for testing the output of the [GitHub action defined in a forked  `wandb`](https://github.com/ngrayluna/wandb/blob/main/.github/workflows/generate-api-docs.yml) using  `lazydocs` + [custom Python scripts](https://github.com/ngrayluna/generate-wandb-python-reference)

### Testing

1. Clone forked [ngrayluna/wandb](https://github.com/ngrayluna/wandb) repo.
   (I cloned `wandb/wandb` to quickly iterate GitHub action yml file defined in `wandb` repo i.e. not need access to store github secrets, etc.).
2. Run the action in `ngrayluna/wandb` [generate-api-docs.yml](https://github.com/ngrayluna/wandb/blob/main/.github/workflows/generate-api-docs.yml)

### Preview proposed changes (what is used to generate excel sheet with all APIs currently exposed)
You can preview all proposed changes using the [`lazydocs_preview_all`](https://github.com/wandb/wandb/tree/lazydocs_preview_all) branch defined in `wandb/wandb`. The PRs that make up this branch are [here (search for `is:pr is:open lazydocs` )](https://github.com/wandb/wandb/pulls?q=is%3Apr+is%3Aopen+lazydocs).

See this example preview of what this looks like: https://preview-lazydocs.docodile.pages.dev/ref/python-library/

### Summary
* Code with lazydocs + additional processing: https://github.com/ngrayluna/generate-wandb-python-reference
* Forked wandb repo for quick testing: https://github.com/ngrayluna/wandb
* GitHub action to generate the docs: https://github.com/ngrayluna/wandb/blob/main/.github/workflows/generate-api-docs.yml

###  GitHub action to do
1. Update GitHub action (`ngrayluna/wandb/.../generate-api-docs.yml`): so we can specify a specific commit SHA, release tag, or branch. Currently set to latest on `main`.
