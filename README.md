# diff-includes
This is an action inspired by [netlify/actions/diff-includes](https://github.com/netlify/actions/tree/master/diff-includes) to prevent synchronous actions if changes happen in a specified folder.

## Usage
Usage information for individual commands can be found in their respective directories.

```yml
on: push
name: Publish docs if changed
jobs:
  checkChangesInDocs:
    name: Check changes in docs
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@master
    - name: Check changes in stories
      uses: open-sauced/diff-includes
      with:
        args: docs
```
