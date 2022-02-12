# poetry-workspace-plugin-build-example

### Install

- `poetry install`

For convenience, poetry is configured as a dependency, so you don't have to change your global poetry configuration.

- `poetry run poetry plugin add git+https://github.com/dszakallas/poetry-workspace-plugin.git#workspace-build`
- `poetry run poetry workspace run poetry install`

### Build:

- `poetry run poetry workspace build -f wheel`

### Check:

```
$ unzip -p workspace_b/dist/pwp_build_workspace_b-0.1.0-py3-none-any.whl pwp_build_workspace_b-0.1.0.dist-info/METADATA | cat
Metadata-Version: 2.1
Name: pwp-build-workspace-b
Version: 0.1.0
Summary: workspace b
Requires-Python: >=3.9,<4.0
Classifier: Programming Language :: Python :: 3
Classifier: Programming Language :: Python :: 3.9
Classifier: Programming Language :: Python :: 3.10
Requires-Dist: pwp-build-workspace-a (>=0.1.0,<0.2.0)
```