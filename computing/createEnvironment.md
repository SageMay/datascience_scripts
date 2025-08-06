
A .yml can be used to create an env with matching package versions (e.g. https://saturncloud.io/blog/how-to-create-a-conda-environment-based-on-a-yaml-file-a-guide-for-data-scientists/).

Creating an environment is critical for reproducibility since versions of software change and dependencies for a project can be non-obvious.

Using Bash:

`conda env create -f FOO.yml`\
`conda activate FOO`\
`conda install ipykernel`\
`python -m ipykernel install --user --name=FOO --display-name="FOO"`
