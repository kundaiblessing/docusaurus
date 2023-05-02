---
sidebar_label: "vale"
sidebar_position: 5
---

# Vale

## Getting Started with Vale

![Vale Logo](./vale-logo.png)

Working with **[Vale](https://vale.sh/)** is the best automation tool for technical writers.

Vale is an open source style guide linter. It tells you exactly what’s wrong with your writing. If you already have a project that you want to use with Vale, this is a great article to follow for getting started. If you are starting from scratch and just want to test it out, please download **[this pdf](https://artisanal-pioneer-1249.ck.page/0a69a3346e)** to go over how to start a project by cloning a boilerplate from GitHub.

The code in your `vale.yaml` should be as follows:

```jsx title="src/pages/my-react-page.js"
name: Editorial Review

  # Controls when the action will run.
    on:
    # Triggers the workflow on push or pull request events but only for the main branch
    push:
        branches: [ main ]

    # Allows you to run this workflow manually from the Actions tab
    workflow_dispatch:

    jobs:
    prose:
        runs-on: ubuntu-latest
        steps:
        - name: Checkout
        uses: actions/checkout@master

        - name: Vale
        uses: errata-ai/vale-action@reviewdog
        with:
            files: vale-tutorial/

    env:
```
